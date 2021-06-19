---
title: 使用 Image 元素
description: 本文說明如何使用 VML 中的 Image 元素，這是 Windows Internet Explorer 9 所淘汰的功能。
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- 網路研討會，image 元素
- 設計網頁、影像元素
- Vector Markup Language (VML) 、image 元素
- VML (Vector Markup Language) ，image 元素
- 向量圖形、image 元素
- 影像元素
- VML 元素、影像
- VML 圖形、image 元素
- Vector Markup Language (VML) ，裁剪屬性屬性
- VML (Vector Markup Language) ，裁剪屬性屬性
- 向量圖形，裁剪屬性屬性
- VML 圖形，裁剪屬性屬性
- 裁剪屬性屬性
- Vector Markup Language (VML) 、增益屬性屬性
- VML (Vector Markup Language) ，增益屬性屬性
- 向量圖形，增益屬性屬性
- VML 圖形，增益屬性屬性
- 增益屬性屬性
- Vector Markup Language (VML) 、對比
- VML (Vector Markup Language) ，對比
- 向量圖形，對比
- VML 圖形，對比
- Vector Markup Language (VML) ，blacklevel 屬性屬性
- VML (Vector Markup Language) ，blacklevel 屬性屬性
- 向量圖形，blacklevel 屬性屬性
- VML 圖形，blacklevel 屬性屬性
- blacklevel 屬性屬性
- Vector Markup Language (VML) 、亮度
- VML (Vector Markup Language) 、亮度
- 向量圖形，亮度
- VML 圖形，亮度
- Vector Markup Language (VML) 、灰階屬性屬性
- VML (Vector Markup Language) 、灰階屬性屬性
- 向量圖形、灰階屬性屬性
- VML 圖形，灰階屬性屬性
- 灰階屬性屬性
- Vector Markup Language (VML) 、gamma 屬性屬性
- VML (Vector Markup Language) ，gamma 屬性屬性
- 向量圖形、gamma 屬性屬性
- VML 圖形、gamma 屬性屬性
- gamma 屬性屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572acef76afc42e02f476ca1825ef2541f596380
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407801"
---
# <a name="using-the-image-element"></a><span data-ttu-id="cfb34-144">使用 Image 元素</span><span class="sxs-lookup"><span data-stu-id="cfb34-144">Using the Image Element</span></span>

<span data-ttu-id="cfb34-145">本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。</span><span class="sxs-lookup"><span data-stu-id="cfb34-145">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cfb34-146">依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。</span><span class="sxs-lookup"><span data-stu-id="cfb34-146">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cfb34-147">從2011年12月起，本主題已封存。</span><span class="sxs-lookup"><span data-stu-id="cfb34-147">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cfb34-148">因此，它不會再主動維護。</span><span class="sxs-lookup"><span data-stu-id="cfb34-148">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cfb34-149">如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。</span><span class="sxs-lookup"><span data-stu-id="cfb34-149">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cfb34-150">如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。</span><span class="sxs-lookup"><span data-stu-id="cfb34-150">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cfb34-151">使用 `<image>`</span><span class="sxs-lookup"><span data-stu-id="cfb34-151">Using `<image>`</span></span>

<span data-ttu-id="cfb34-152">在本主題中，我們將說明如何使用 `<image>` 元素來顯示具有各種特殊效果的圖片。</span><span class="sxs-lookup"><span data-stu-id="cfb34-152">In this topic, we will illustrate how to use the `<image>` element to display pictures with various special effects.</span></span>

<span data-ttu-id="cfb34-153">如果您想要顯示從外部來源載入的圖片，通常會使用 `<img>` HTML 中提供的元素，然後將 **src** 屬性屬性指向影像檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="cfb34-153">If you wanted to display a picture that was loaded from an external source, you would usually use the `<img>` element provided in HTML, and then point the **src** property attribute to the location of the image file.</span></span>

<span data-ttu-id="cfb34-154">或者，您也可以使用 `<image>` VML 中提供的元素。</span><span class="sxs-lookup"><span data-stu-id="cfb34-154">Alternatively you can use the `<image>` element provided in VML.</span></span> <span data-ttu-id="cfb34-155">當您使用專案時 `<image>` ，您只能建立一個影像檔案，然後藉由改變專案的屬性屬性，以不同的方式來顯示影像 `<image>` 。</span><span class="sxs-lookup"><span data-stu-id="cfb34-155">When you use the `<image>` element, you can create only one image file and then display the image differently by altering the property attributes of the `<image>` element.</span></span> <span data-ttu-id="cfb34-156">此外，專案也會 `<image>` 提供幾個特殊效果，您只需要使用 `<img>` HTML 的元素（例如 [裁剪](#crop)、 [對比](#contrast)、 [亮度](#brightness)、 [gamma](#gamma)和 [灰階](#grayscale)）就能達到這個目的。</span><span class="sxs-lookup"><span data-stu-id="cfb34-156">Also, the `<image>` element provides several special effects that you can't do by simply using the `<img>` element of HTML, such as [cropping](#crop), [contrast](#contrast), [brightness](#brightness), [gamma](#gamma), and [grayscale](#grayscale).</span></span>

<span data-ttu-id="cfb34-157">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="cfb34-157">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="crop"></a><span data-ttu-id="cfb34-158">裁切</span><span class="sxs-lookup"><span data-stu-id="cfb34-158">crop</span></span>

<span data-ttu-id="cfb34-159">您可以使用專案的 **cropbottom**、 **croptop**、 **cropleft** 和 **cropright** 屬性屬性， `<image>` 顯示從相同影像檔裁剪的不同圖片。</span><span class="sxs-lookup"><span data-stu-id="cfb34-159">You can use the **cropbottom**, **croptop**, **cropleft**, and **cropright** property attributes of the `<image>` element to display different pictures that are cropped from the same image file.</span></span>

<span data-ttu-id="cfb34-160">這些裁剪屬性的值代表從圖片邊緣剪下的百分比。</span><span class="sxs-lookup"><span data-stu-id="cfb34-160">The value of these crop attributes represents the percentage cut from the edge of the picture.</span></span> <span data-ttu-id="cfb34-161">值可以是介於0到1之間的任何數位。</span><span class="sxs-lookup"><span data-stu-id="cfb34-161">The value can be any number between 0 to 1.</span></span> <span data-ttu-id="cfb34-162">根據預設，值會設定為0，表示沒有從邊緣裁剪。</span><span class="sxs-lookup"><span data-stu-id="cfb34-162">By default, the value is set to 0, indicating no crop from the edge.</span></span> <span data-ttu-id="cfb34-163">值0.1 表示從邊緣裁剪10%，值0.15 表示從邊緣裁剪15%，依此類推。</span><span class="sxs-lookup"><span data-stu-id="cfb34-163">The value 0.1 indicates a cropping of 10 percent from the edge, The value 0.15 indicates a cropping of 15 percent from the edge, and so on.</span></span>

<span data-ttu-id="cfb34-164">例如，若要顯示全部從相同影像檔案裁剪的五張圖片，您可以使用專案 `<image>` 並指定不同的裁剪值，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="cfb34-164">For example, to display five pictures that are all cropped from the same image file, you can use the `<image>` element and specify different crop values, as shown in the following VML representation:</span></span>

![image1.jpg (5770 個位元組) ](images/image1.jpg)![image1 \-2.jpg (1969 個位元組) ](images/image1-2.jpg)![image1 \-3.jpg (1148 個位元組) ](images/image1-3.jpg)![image1 \-4.jpg (1686 個位元組) ](images/image1-4.jpg)![image1 \-5.jpg (1364 個位元組) ](images/image1-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:85pt;height:64pt' src="image1.jpg"
cropbottom="0.2" cropright="0.15"/>
<v:image style='width:50pt;height:44pt' src="image1.jpg"
cropbottom="0.45" cropleft="0.5"/>
<v:image style='width:80pt;height:56pt' src="image1.jpg"
croptop="0.3" cropright="0.2"/>
<v:image style='width:70pt;height:48pt' src="image1.jpg"
croptop="0.4" cropleft="0.3"/>
```





<span data-ttu-id="cfb34-170">第一個影像 `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` 沒有任何裁剪值。</span><span class="sxs-lookup"><span data-stu-id="cfb34-170">The first image, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />`, doesn't have any crop value.</span></span> <span data-ttu-id="cfb34-171">因此，100% 的原始影像會依80點以100點的大小顯示。</span><span class="sxs-lookup"><span data-stu-id="cfb34-171">Therefore, 100 percent of the original image is displayed at a size of 100 points by 80 points.</span></span>

<span data-ttu-id="cfb34-172">第二個影像 `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` 有一些裁剪值。</span><span class="sxs-lookup"><span data-stu-id="cfb34-172">The second image, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>`, has some crop values.</span></span> <span data-ttu-id="cfb34-173">`cropbottom="0.2"` 指出將從底部裁剪20% 的圖片; `cropright="0.15"` 指出將從右邊緣裁剪15% 的圖片。</span><span class="sxs-lookup"><span data-stu-id="cfb34-173">`cropbottom="0.2"` indicates that 20 percent of the picture will be cropped from the bottom; `cropright="0.15"` indicates that 15 percent of the picture will be cropped from the right edge.</span></span> <span data-ttu-id="cfb34-174">剩餘的圖片接著會以85點的大小顯示64點。</span><span class="sxs-lookup"><span data-stu-id="cfb34-174">The remaining picture is then displayed at a size of 85 points by 64 points.</span></span>

<span data-ttu-id="cfb34-175">同樣地，第三個、第四個和第五個影像有一些裁剪值。</span><span class="sxs-lookup"><span data-stu-id="cfb34-175">Similarly the third, fourth, and fifth images have some crop values.</span></span> <span data-ttu-id="cfb34-176">原始圖片會根據裁剪值裁剪，然後根據寬度和高度的值來顯示。</span><span class="sxs-lookup"><span data-stu-id="cfb34-176">The original picture is cropped according to the crop values, and is then displayed according to the value of width and height.</span></span>

<span data-ttu-id="cfb34-177">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="cfb34-177">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="contrast"></a><span data-ttu-id="cfb34-178">對比</span><span class="sxs-lookup"><span data-stu-id="cfb34-178">contrast</span></span>

<span data-ttu-id="cfb34-179">您可以使用專案的 [ **增益** ] 屬性屬性 `<image>` ，顯示具有不同對比設定的各種圖片。</span><span class="sxs-lookup"><span data-stu-id="cfb34-179">You can use the **gain** property attribute of the `<image>` element to display various pictures that have different contrast settings.</span></span>

<span data-ttu-id="cfb34-180">**增益** 屬性屬性的值可以是任何數位。</span><span class="sxs-lookup"><span data-stu-id="cfb34-180">The value of the **gain** property attribute can be any number.</span></span> <span data-ttu-id="cfb34-181">根據預設，此值為1，表示使用與原始影像相同的對比。</span><span class="sxs-lookup"><span data-stu-id="cfb34-181">By default, the value is 1, indicating the use of the same contrast as the original image.</span></span> <span data-ttu-id="cfb34-182">0值表示無對比。</span><span class="sxs-lookup"><span data-stu-id="cfb34-182">The value 0 indicates no contrast.</span></span> <span data-ttu-id="cfb34-183">數位愈大，對比愈高。</span><span class="sxs-lookup"><span data-stu-id="cfb34-183">The larger the number, the higher the contrast.</span></span>

<span data-ttu-id="cfb34-184">例如，若要顯示具有不同對比設定的五張圖片，可以使用 `<image>` 元素並為 **增益** 屬性屬性設定不同的值，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="cfb34-184">For example, to display five pictures that have different contrast settings, you can use the `<image>` element and set a different value for the **gain** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 個位元組) ](images/image1.jpg)![image2 \-2.jpg (270 個位元組) ](images/image2-2.jpg)![image2 \-3.jpg (1919 個位元組) ](images/image2-3.jpg)![image2 \-4.jpg (3143 個位元組) ](images/image2-4.jpg)![image2 \-5.jpg (1724 個位元組) ](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





<span data-ttu-id="cfb34-190">當 **增益** 屬性屬性設定為0時，整個影像都會變成灰色，因為沒有任何對比。</span><span class="sxs-lookup"><span data-stu-id="cfb34-190">When the **gain** property attribute is set to 0, the entire image becomes gray because there is no contrast.</span></span> <span data-ttu-id="cfb34-191">當 **增益** 屬性屬性設定為3，而不是設定為0.5 時，對比會更明顯。</span><span class="sxs-lookup"><span data-stu-id="cfb34-191">The contrast is more noticeable when the **gain** property attribute is set to 3 than when it is set to 0.5.</span></span> <span data-ttu-id="cfb34-192">當 **增益** 屬性屬性設定為負數值（例如-0.4）時，就會反轉對比。</span><span class="sxs-lookup"><span data-stu-id="cfb34-192">The contrast is reversed when the **gain** property attribute is set to a negative value such as -0.4.</span></span>

<span data-ttu-id="cfb34-193">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="cfb34-193">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="brightness"></a><span data-ttu-id="cfb34-194">亮度</span><span class="sxs-lookup"><span data-stu-id="cfb34-194">brightness</span></span>

<span data-ttu-id="cfb34-195">您可以使用專案的 **blacklevel** 屬性屬性 `<image>` 來顯示各種不同的亮度設定的圖片。</span><span class="sxs-lookup"><span data-stu-id="cfb34-195">You can use the **blacklevel** property attribute of the `<image>` element to display various pictures that have different brightness settings.</span></span>

<span data-ttu-id="cfb34-196">**Blacklevel** 屬性屬性的值可以是介於0到1之間的任何值。</span><span class="sxs-lookup"><span data-stu-id="cfb34-196">The value of the **blacklevel** property attribute can be any value between 0 to 1.</span></span> <span data-ttu-id="cfb34-197">根據預設，此值為0，表示保留原始影像中的亮度等級。</span><span class="sxs-lookup"><span data-stu-id="cfb34-197">By default, the value is 0, indicating that the level of brightness in the original image is preserved.</span></span> <span data-ttu-id="cfb34-198">值1表示最高層級的亮度。</span><span class="sxs-lookup"><span data-stu-id="cfb34-198">The value 1 indicates the highest level of brightness.</span></span>

<span data-ttu-id="cfb34-199">例如，若要顯示具有不同亮度設定的五張圖片，可以使用 `<image>` 元素並為 **blacklevel** 屬性屬性設定不同的值，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="cfb34-199">For example, to display five pictures that have different brightness settings, you can use the `<image>` element and set a different value for the **blacklevel** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 個位元組) ](images/image1.jpg)![image3 \-2.jpg (2579 個位元組) ](images/image3-2.jpg)![image3 \-3.jpg (2330 個位元組) ](images/image3-3.jpg)![image3 \-4.jpg (2727 個位元組) ](images/image3-4.jpg)![image3 \-5.jpg (2435 個位元組) ](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





<span data-ttu-id="cfb34-205">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="cfb34-205">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="grayscale"></a><span data-ttu-id="cfb34-206">灰階</span><span class="sxs-lookup"><span data-stu-id="cfb34-206">grayscale</span></span>

<span data-ttu-id="cfb34-207">您可以使用專案的 [ **灰階** ] 屬性屬性 `<image>` 來顯示包含或不含灰階的圖片。</span><span class="sxs-lookup"><span data-stu-id="cfb34-207">You can use the **grayscale** property attribute of the `<image>` element to display pictures with or without grayscale.</span></span>

<span data-ttu-id="cfb34-208">**灰階** 屬性屬性的值可以是 true 或 false。</span><span class="sxs-lookup"><span data-stu-id="cfb34-208">The value of the **grayscale** property attribute can be either true or false.</span></span> <span data-ttu-id="cfb34-209">依預設，此值會設為 false，因此影像將會以色彩顯示。</span><span class="sxs-lookup"><span data-stu-id="cfb34-209">By default, the value is set to false so that the image will be displayed in color.</span></span> <span data-ttu-id="cfb34-210">如果值設定為 true，則影像會以灰階顯示。</span><span class="sxs-lookup"><span data-stu-id="cfb34-210">If the value is set to true, the image will be displayed in grayscale.</span></span>

<span data-ttu-id="cfb34-211">例如，如下圖所示，第一個影像會使用灰階屬性的預設設定 (false)  (`<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ) 。</span><span class="sxs-lookup"><span data-stu-id="cfb34-211">For example, as shown in the following picture, the first image uses the default setting (false)of the grayscale attribute (`<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span></span> <span data-ttu-id="cfb34-212">因此，圖片會以色彩顯示。</span><span class="sxs-lookup"><span data-stu-id="cfb34-212">Therefore, the picture is displayed in color.</span></span>

<span data-ttu-id="cfb34-213">第二個影像會將 [灰階] 屬性設定為 [true] (`<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ) 。</span><span class="sxs-lookup"><span data-stu-id="cfb34-213">The second image sets the grayscale attribute to true (`<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span></span> <span data-ttu-id="cfb34-214">因此，圖片會以灰階顯示，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="cfb34-214">Therefore, the picture is displayed in grayscale, as shown in the following VML representation:</span></span>

![image1.jpg (5770 個位元組) ](images/image1.jpg)![image4.jpg \-2.jpg (2138 個位元組) ](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





<span data-ttu-id="cfb34-217">[![回到 ](images/top.gif) 頂端回到頁首](#top)</span><span class="sxs-lookup"><span data-stu-id="cfb34-217">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="gamma"></a><span data-ttu-id="cfb34-218">gamma</span><span class="sxs-lookup"><span data-stu-id="cfb34-218">gamma</span></span>

<span data-ttu-id="cfb34-219">您可以使用專案的 **gamma** 屬性屬性 `<image>` 來顯示具有不同 gamma 設定的圖片。</span><span class="sxs-lookup"><span data-stu-id="cfb34-219">You can use the **gamma** property attribute of the `<image>` element to display pictures that have different gamma settings.</span></span>

<span data-ttu-id="cfb34-220">Gamma 屬性屬性的值可以是介於0和1之間的任何值。</span><span class="sxs-lookup"><span data-stu-id="cfb34-220">The value of the gamma property attribute can be any value between 0 and 1.</span></span> <span data-ttu-id="cfb34-221">依預設，此值設定為1。</span><span class="sxs-lookup"><span data-stu-id="cfb34-221">By default, the value is set to 1.</span></span>

<span data-ttu-id="cfb34-222">例如，若要顯示三張具有不同 gamma 設定的圖片，您可以使用 `<image>` 元素並設定不同的 **gamma** 屬性屬性值，如下列 VML 標記法所示：</span><span class="sxs-lookup"><span data-stu-id="cfb34-222">For example, to display three pictures that have different gamma settings, you can use the `<image>` element and set a different value of the **gamma** property attribute, as shown in the following VML representation:</span></span>

![image5 \-1.jpg (2714 個位元組) ](images/image5-1.jpg)![image5 \-2.jpg (2729 個位元組) ](images/image5-2.jpg)![image5 \-3.jpg (2726 個位元組) ](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





<span data-ttu-id="cfb34-226">如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858408) 。</span><span class="sxs-lookup"><span data-stu-id="cfb34-226">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span></span>

 

 