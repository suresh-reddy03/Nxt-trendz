<!-- README Start -->
<h1 align="center">🛍 Nxt Trendz - Complete E-Commerce React App</h1>

<p align="center">
  A full-fledged e-commerce application built using React.js that includes user authentication, product listing, product details, and complete cart features with dynamic state management using React Context.
</p>

<hr/>

<h2>🔐 Login Functionality</h2>
<ul>
  <li>Authenticated login for Prime and Non-Prime users</li>
  <li>Routes like <code>/products</code>, <code>/cart</code>, and <code>/products/:id</code> are protected and require login</li>
  <li>Credentials for testing:
    <ul>
      <li>Prime User: <code>username: rahul</code>, <code>password: rahul@2021</code></li>
      <li>Non-Prime User: <code>username: raja</code>, <code>password: raja@2021</code></li>
    </ul>
  </li>
</ul>

<h2>🛒 Product Listing Features</h2>
<ul>
  <li>Authenticated users can access <code>/products</code> route</li>
  <li>Each product includes image, title, brand, price, rating, and review count</li>
  <li>Clicking a product navigates to <code>/products/:id</code> route</li>
</ul>

<h2>📦 Specific Product Details</h2>
<ul>
  <li>Fetches product data using API: <code>https://apis.ccbp.in/products/:id</code></li>
  <li>Displays product image, title, description, brand, price, availability, rating, and total reviews</li>
  <li>Includes quantity control using plus (<code>BsPlusSquare</code>) and minus (<code>BsDashSquare</code>) buttons</li>
  <li>Similar products displayed below with alt text as <code>similar product {title}</code></li>
  <li>Loader displayed using:
    <pre><code>
&lt;div data-testid="loader"&gt;
  &lt;Loader type="ThreeDots" color="#0b69ff" height={80} width={80} /&gt;
&lt;/div&gt;
    </code></pre>
  </li>
  <li>If API fails, failure view is shown with a <strong>Continue Shopping</strong> button linking to <code>/products</code></li>
</ul>

<h2>🛒 Cart Features</h2>
<ul>
  <li>Only authenticated users can access <code>/cart</code></li>
  <li>Handles adding the same product multiple times — quantity increases, cart count remains constant</li>
  <li>Displays cart summary with total items and total amount</li>
  <li>Each item has plus/minus buttons (<code>data-testid="plus"</code>, <code>data-testid="minus"</code>) to update quantity</li>
  <li>If quantity becomes 0 via minus, item is removed</li>
  <li>Remove button (with icon <code>AiFillCloseCircle</code>) removes individual item</li>
  <li><strong>Remove All</strong> button clears entire cart and shows empty cart view</li>
  <li>CartContext includes:
    <ul>
      <li><code>cartList</code></li>
      <li><code>addCartItem</code></li>
      <li><code>removeCartItem</code></li>
      <li><code>incrementCartItemQuantity</code></li>
      <li><code>decrementCartItemQuantity</code></li>
      <li><code>removeAllCartItems</code></li>
    </ul>
  </li>
</ul>

<h2>🔁 Routing Paths</h2>
<ul>
  <li><code>/</code> → Home</li>
  <li><code>/login</code> → Login</li>
  <li><code>/products</code> → Product Listing</li>
  <li><code>/products/:id</code> → Product Details</li>
  <li><code>/cart</code> → Cart</li>
</ul>

<h2>🎨 UI Guidelines</h2>
<ul>
  <li>Responsive for all breakpoints: Extra Small to Extra Large</li>
  <li>Use of consistent <code>Roboto</code> font</li>
  <li>Color Palette:
    <ul>
      <li>#0b69ff, #171f46, #616e7c, #ffffff</li>
    </ul>
  </li>
  <li>Image Alt Attributes:
    <ul>
      <li>Product Details: <code>alt="product"</code></li>
      <li>Similar Product: <code>alt="similar product {title}"</code></li>
      <li>Cart Item Image: <code>alt="{title}"</code></li>
    </ul>
  </li>
</ul>

<h2>📁 Component Directory</h2>
<ul>
  <li><code>src/components/LoginForm</code></li>
  <li><code>src/components/Products</code></li>
  <li><code>src/components/ProductItemDetails</code></li>
  <li><code>src/components/SimilarProductItem</code></li>
  <li><code>src/components/ProductCard</code></li>
  <li><code>src/components/Cart</code></li>
  <li><code>src/components/CartItem</code></li>
  <li><code>src/components/CartSummary</code></li>
</ul>

<h2>⚙ Setup & Start</h2>
<pre><code>
npm install
npm start
</code></pre>

<h2>📸 Preview</h2>
<p align="center">
  <img src="https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-product-details-output-v0.gif" alt="Product Details Demo" width="70%">
  <br/><br/>
  <video width="70%" controls autoplay muted loop>
    <source src="https://assets.ccbp.in/frontend/content/react-js/nxt-trendz-cart-features-output.mp4" type="video/mp4" />
  </video>
</p>

<!-- README End -->
