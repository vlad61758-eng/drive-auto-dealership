Documentation for "DRIVE Auto Dealership" Website Template

Welcome! This guide provides clear, step-by-step instructions for editing and finalizing your premium "DRIVE Auto Dealership" template before handing it over to the end client.

All necessary modifications are contained within the index.html file.

1. Content and Branding Customization

These steps focus on replacing mock data with the client's actual information.

1.1. Color Scheme Adjustment (Gold Accent)

To change the core gold accent color to another brand color (e.g., red or silver), you need to modify only one line in the <script> section within the <head>:

Locate:

'accent-gold': '#ffbf00', /* Gold accent */


Action: Replace #ffbf00 (the HEX code for gold) with the new desired HEX color code. This single change applies the new accent color to all buttons, headings, and design elements across the site.

1.2. Updating Text and Headings

Title: Change the text in the <title> tag to reflect the client's dealership name.

Hero Section: Update the main headline (<h1>) and the sub-paragraph (<p>) with the client's unique marketing message.

Services Section: Customize the titles and descriptions within the three service cards (Flexible Financing, Certified Service & Repair, etc.).

1.3. Featured Models Section (Inventory Cards)

Each car card must be updated with current inventory data:

Placeholder Images: Replace the URL in the <img> tag with the actual photo URLs of the client's vehicles.

<img src="[https://placehold.co/600x400/262d3a/FFFFFF?text=Sports+Sedan](https://placehold.co/600x400/262d3a/FFFFFF?text=Sports+Sedan)" 
     alt="Sports Sedan" 
     class="w-full h-48 object-cover object-center">


Data: Update the model name, performance description, price, and status (New/Pre-Owned):

<h3 class="text-xl font-bold mb-2 text-accent-gold">Sportiva S-500</h3>
<p class="text-gray-400 mb-4 text-sm">High performance and flawless style. 0-60 mph in 4.0 seconds.</p>
<span class="text-2xl font-extrabold text-white">$95,000</span>


2. Finalization and Client Handoff

These steps ensure the website is fully owned by the client and professional for final delivery.

2.1. Removing Developer Attribution in the Footer

To make the site "clean" for the client, your developer note must be removed from the visible footer. Your professional attribution in the HTML comments remains, validating your authorship.

Locate the line in the <footer> section:

<!-- Custom Attribution Line (Client instructions: REMOVE this line or replace with client's business name after sale) -->
<p class="mt-1 text-sm text-accent-gold">--- REMOVE THIS LINE OR REPLACE WITH CLIENT'S NAME ---</p>


Action: Delete this entire <p> block.

2.2. Connecting the Contact Form (CRITICAL)

The "Get in Touch" form currently only simulates a successful submission (for demonstration). For a real client, it must send actual emails.

Recommended Method: Using Formspree or FormSubmit

The client must register with a service (like Formspree) and obtain a unique submission URL (e.g., https://formspree.io/f/xyza123).

Locate the <form> tag in the #contact section in index.html.

Action: Remove the onsubmit="handleFormSubmit(event)" attribute from the <form> tag.

Add the action attribute with the client's URL and method="POST":

<form id="contact-form" method="POST" action="[CLIENT'S FORMSPREE URL HERE]">
    <!-- All form fields remain unchanged -->
    ...
</form>


Action: After the action attribute is added, you can also safely delete the entire <script> tag at the very end of the file, as the external service will handle the form logic.
