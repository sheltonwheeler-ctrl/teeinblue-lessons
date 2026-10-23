# Teeinblue, the Hard Way: Lessons From Building a Store Full of Personalized Products

*Written by a print-on-demand seller and his AI assistant, after rebuilding a whole store's worth of personalized products (Shopify + Printful + Teeinblue). Every lesson below cost us real hours. Steal them all — that's the point.*

## 1. Saving an artwork does NOT update your store. Click "Update Campaign."

This is the big one. You can edit an artwork, save it, see it perfect in the editor — and your live storefront will keep showing the OLD version, because artwork saves do not push to the storefront embed. After **any** artwork or personalization change: save the artwork, then open the connected campaign and click **Update Campaign**, then verify on the live product page. We lost hours to a round-photo crop that was "set" the whole time and simply never pushed.

## 2. On masked mockups, layer ORDER is everything

If a mockup uses an "Outside mask" to clip your design to the product's shape (bowls, mugs, anything curved), the mask layer must sit **above** the artwork layer in the mockup. If the artwork is on top, the mask clips nothing and the preview renders your design as a flat strip floating across the screen — even when every placement number (size, top, left) matches a working campaign exactly. When a preview looks like a strip, check the mockup's layer order before touching any numbers.

## 3. The "Default text" field PRINTS. Leave it empty.

In a text layer's settings, "Default text (only for preview)" sounds harmless. It is not: if it contains text, a customer who leaves that field blank can receive a product printed with your default word on it. Rule: every text layer's Default text stays **empty**, prefill stays **off** — and prove it by generating a test print file with the fields left blank. The print file must show no text at all. (We found a live campaign whose default field contained a sample name. That was a customer complaint waiting to happen.)

## 4. Turn on "Set minimum size" for photo uploads

Customers will upload tiny, blurry photos and then blame the print. Teeinblue's photo upload layers have a **Set minimum size** option: uploads below your minimum get stopped with a "image is too small, please upload a bigger image" warning. Set it for every photo product, sized to the print area — about 300 DPI worth of pixels for small items (an ornament at ~3.3 inches ≈ 1000×1000 px), about 150 DPI for large items (a 16×20 canvas ≈ 2400×3000 px). Don't set large-format minimums so high that a normal phone photo can't pass.

## 5. Check effective DPI before you build, not after

For every graphic in an artwork, divide the file's pixels by the inches it will occupy at print size. Under 300 DPI, stop and remake the graphic — do not build on it and hope. Low-resolution source art is the #1 silent quality killer in personalized products.

## 6. Photo product traps

- **"Photo Reposition" strands uploads small** in a corner at their natural size. For fill-the-whole-product photos, use **Photo Cropper** so the customer's photo scales to fill the layer.
- **Round products need "Crop into a custom shape"** with a solid-black shape PNG (e.g., a filled circle), or uploads render as rectangles spilling outside the disc.
- **Verify photo personalizers only with a busy-background photo.** A plain-background test photo can make a broken, unclipped render LOOK correct. Your ugliest couch photo is the best test file you own.
- Customers can pan/zoom inside the crop step; after confirming, there's no repositioning — "Recustomize image" reopens the cropper.

## 7. Text layer traps

- A text layer's box must fit **inside** the canvas and the paragraph alignment must be **centered** (unless a design truly needs otherwise). The renderer shrinks text to fit the BOX, not the canvas — an off-canvas or misaligned box makes short text vanish and long text clip.
- Prove every personalizer with BOTH a short string and a max-length string before calling it done.

## 8. Build personalized products the right way around

Print-on-demand provider (e.g., Printful) should supply only a **blank shell** — product + variants + a clear/transparent placeholder — synced to your store. The real design lives in the personalizer, in **separate layers** (background, artwork, each text line on its own layer), because the personalizer's generated file is what actually prints. Anything set only on the provider side (like a background fill color) does NOT merge into the personalizer's print file — bake backgrounds into the artwork itself. And set your provider store to **manual order confirmation** so a synced order can't auto-print the un-personalized placeholder design before you've swapped in the customer's personalized file.

## 9. Collaborator access: trim it

If a support team asks for Shopify collaborator access, read the permission list before approving. The standard request may include things a support team does not need — like charging credit cards or managing store settings. Shopify lets you edit the role before accepting: products, themes, and apps are plenty for personalizer support. Also note: logging out can reset role edits you made on a pending request — re-check the role contents before you accept.

---

*If even one of these saves you a night, it did its job. — a seller who learned them all the expensive way*
