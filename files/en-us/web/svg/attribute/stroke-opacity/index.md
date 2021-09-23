---
title: stroke-opacity
slug: Web/SVG/Attribute/stroke-opacity
tags:
  - SVG
  - SVG Attribute
browser-compat: svg.attributes.presentation.stroke-opacity
---
<div>{{SVGRef}}</div>

<p>The <strong><code>stroke-opacity</code></strong> attribute is a presentation attribute defining the opacity of the paint server (<em>color</em>, <em>gradient</em>, <em>pattern</em>, etc) applied to the stroke of a shape.</p>

<div class="note"><p><strong>Note:</strong> As a presentation attribute <code>stroke-opacity</code> can be used as a CSS property.</p></div>

<p>You can use this attribute with the following SVG elements:</p>

<ul>
  <li>{{SVGElement('altGlyph')}}</li>
  <li>{{SVGElement('circle')}}</li>
  <li>{{SVGElement('ellipse')}}</li>
  <li>{{SVGElement('path')}}</li>
  <li>{{SVGElement('line')}}</li>
  <li>{{SVGElement('polygon')}}</li>
  <li>{{SVGElement('polyline')}}</li>
  <li>{{SVGElement('rect')}}</li>
  <li>{{SVGElement('text')}}</li>
  <li>{{SVGElement('textPath')}}</li>
  <li>{{SVGElement('tref')}}</li>
  <li>{{SVGElement('tspan')}}</li>
</ul>

<h2>Example</h2>

<pre class="brush: css hidden">html,body,svg { height:100% }</pre>

<pre class="brush: html">&lt;svg viewBox="0 0 40 10" xmlns="http://www.w3.org/2000/svg"&gt;
  &lt;!-- Default stroke opacity: 1 --&gt;
  &lt;circle cx="5" cy="5" r="4" stroke="green" /&gt;

  &lt;!-- Stroke opacity as a number --&gt;
  &lt;circle cx="15" cy="5" r="4" stroke="green"
          stroke-opacity="0.7" /&gt;

  &lt;!-- Stroke opacity as a percentage --&gt;
  &lt;circle cx="25" cy="5" r="4" stroke="green"
          stroke-opacity="50%" /&gt;

  &lt;!-- Stroke opacity as a CSS property --&gt;
  &lt;circle cx="35" cy="5" r="4" stroke="green"
          style="stroke-opacity: .3;" /&gt;
&lt;/svg&gt;</pre>

<p>{{EmbedLiveSample("Example", '100%', 150)}}</p>

<h2 id="Usage_notes">Usage notes</h2>

<table class="properties">
 <tbody>
  <tr>
   <th scope="row">Value</th>
   <td><code>[0-1]</code> | <strong><a href="/en-US/docs/Web/SVG/Content_type#paint">&lt;percentage&gt;</a></strong></td>
  </tr>
  <tr>
   <th scope="row">Default value</th>
   <td><code>1</code></td>
  </tr>
  <tr>
   <th scope="row">Animatable</th>
   <td>Yes</td>
  </tr>
 </tbody>
</table>

<div class="note"><p><strong>Note:</strong> SVG2 introduces percentage values for <code>stroke-opacity</code>, however, it is not widely supported yet (<em>See <a href="#browser_compatibility">Browser compatibility</a> below</em>) as a consequence, it is best practices to set opacity with a value in the range <code>[0-1]</code>.</p></div>

<p>It's important to know that the stroke partially covers the fill of a shape, so a stroke with an opacity different than <code>1</code> will partially show the fill underneath. To avoid this effect, it is possible to apply a global opacity with the {{SVGAttr('opacity')}} attribute or to put the stroke behind the fill with the {{SVGAttr('paint-order')}} attribute.</p>

<h2 id="Browser_compatibility">Browser compatibility</h2>

<p>{{Compat}}</p>

<h2 id="Specifications">Specifications</h2>

<table class="no-markdown">
 <thead>
  <tr>
   <th scope="col">Specification</th>
   <th scope="col">Status</th>
   <th scope="col">Comment</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{SpecName("SVG2", "painting.html#StrokeOpacityProperty", "stroke-opacity")}}</td>
   <td>{{Spec2("SVG2")}}</td>
   <td>Definition for shapes and texts</td>
  </tr>
  <tr>
   <td>{{SpecName("SVG1.1", "painting.html#StrokeOpacityProperty", "stroke-opacity")}}</td>
   <td>{{Spec2("SVG1.1")}}</td>
   <td>Initial definition for shapes and texts</td>
  </tr>
 </tbody>
</table>