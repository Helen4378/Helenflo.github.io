from reportlab.pdfgen import canvas

file_path = "/mnt/data/Fiverr_Resume.pdf"
c = canvas.Canvas(file_path)

# Starting coordinates
x = 40
y = 800

text = [
"Ej Charles — Fiverr Resume",
"",
"SUMMARY:",
"Highly skilled eCommerce and digital strategy specialist with expertise in niche selection, Shopify",
"store creation, product positioning, and conversion optimization. Strong research abilities with a",
"proven understanding of competitive markets, keyword strategies, and consumer psychology.",
"",
"CORE SKILLS:",
"• Shopify Store Setup & Optimization",
"• Branding, Store Identity & Conversion Systems",
"• Market, Niche & Product Research",
"• SEO, Buyer Intent Keywords & Review Mining",
"• Product Bundling & High-Value Positioning",
"• Competitor & Pricing Analysis",
"• High-Converting Product Descriptions",
"• Upsell, AOV & Retention Systems",
"",
"SERVICES OFFERED:",
"• Complete Shopify Store Build",
"• Niche Research & Category Strategy",
"• Product Bundling Architecture",
"• SEO & Competitor Market Breakdown",
"• High-Converting Description Writing",
"• Store UX/UI Trust Optimization",
"• Supplier Research (Untapped Products)",
"",
"STRENGTHS:",
"• Fast execution & strategic thinking",
"• Ability to identify underserved profitable niches",
"• Creates high perceived value for premium pricing",
"• Focused on scalable long-term eCommerce success",
"",
"GUARANTEE:",
"I don’t deliver random stores — I deliver strategy-based online businesses built from proven",
"customer psychology, market demand, and optimized product positioning."
]

for line in text:
    c.drawString(x, y, line)
    y -= 16
    if y < 50:
        c.showPage()
        y = 800

c.save()

file_path
