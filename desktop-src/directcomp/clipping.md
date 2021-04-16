---
title: '裁剪 (DirectComposition) '
description: 本主題說明 Microsoft DirectComposition 剪輯視覺效果的支援。
ms.assetid: B6E0D8F5-B6B9-40CC-B079-850AC8F2D538
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4feb537dfb41053dd1099eca7f122b3284dce95
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383794"
---
# <a name="clipping-directcomposition"></a>裁剪 (DirectComposition) 

> [!NOTE]
> 針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。 如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。

裁剪會提供一種方式，藉由將視覺效果或樹狀結構的呈現限制為特定的矩形區域，來只顯示部分的視覺效果或視覺化樹狀結構。 本主題說明 Microsoft DirectComposition 剪輯視覺效果的支援。 它包含下列各節：

-   [裁剪矩形](#clip-rectangle)
-   [剪輯物件](#clip-object)
-   [動畫裁剪矩形](#animated-clip-rectangle)
-   [相關主題](#related-topics)

## <a name="clip-rectangle"></a>裁剪矩形

視覺物件具有剪輯屬性，可定義視覺效果點陣圖內容中的矩形區域或 *裁剪矩形*。 當視覺效果轉譯至螢幕時，只會在螢幕上繪製剪輯矩形內的點陣圖內容部分，而在裁剪矩形外部延伸的內容則會裁剪 (不會) 繪製出來。 依預設，[剪輯] 屬性包含所有點陣圖內容。

視覺效果的剪輯屬性會套用至所有子系和附屬視覺效果。 換句話說，落在父系剪輯矩形界限外的任何子系或子代內容也會被裁剪。

DirectComposition 會在套用 OffsetX、OffsetY 和2D 轉換屬性之前套用剪輯屬性，但在套用效果和3D 轉換屬性之後。 這表示2D 轉換、OffsetX 和 OffsetY 將會影響視覺內容和剪輯矩形。 而3D 轉換和效果將不會套用至剪輯矩形。

例如，套用位移或2D 轉換時，剪輯矩形會受到轉換矩陣的影響。 因此，新增位移和2D 旋轉 (45 度) 以及圓角剪輯矩形將會產生下列結果：

![顯示2d 轉換在裁剪矩形上之效果的圖表。](images/clipping2dtransform.png)

在剪切矩形中套用「3D 轉換」時，剪輯矩形不會受到轉換矩陣的影響。 即使在 Z 軸上套用旋轉 (實際上與先前的範例) 相同，下圖也是結果：

![圖表顯示3d 轉換不會影響矩形剪輯 (視覺效果在剪輯) 內旋轉。](images/clipping3dtransform.png)

請注意，在剪輯內旋轉的視覺效果是因為3D 矩陣不會套用至剪輯本身。

如果 [剪輯] 屬性設定為空白矩形，則會完全裁剪視覺效果;也就是說，視覺效果包含在視覺化樹狀結構中，但不會轉譯任何事物。 如果您不想要在組合中包含特定的視覺效果，請從視覺化樹狀結構中移除該視覺效果，而不是設定空白的剪輯矩形。 移除視覺效果會提高效能。

您可以使用 [**IDCompositionVisual：： SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) 方法來設定視覺效果的剪輯屬性。 這個方法包含多載，可讓您將剪輯屬性的值設定為靜態矩形或剪輯物件。 如果您不需要在視覺效果的存留期內變更剪輯矩形的維度，請使用靜態矩形。 如果您需要變更維度或以動畫顯示剪輯矩形，請使用剪輯物件。

## <a name="clip-object"></a>剪輯物件

剪輯物件是元件物件模型， (COM) 物件，代表剪輯矩形。 您可以使用 [**IDCompositionDevice：： CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) 方法建立剪輯物件，然後使用物件的 [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) 介面來設定物件的屬性。 新建立的剪輯物件具有左方和頂端屬性的最小可能值，以及右邊和底部屬性的最大可能值，有效地使其成為無作業的剪輯物件。 換句話說，物件代表的是包含視覺效果整個點陣圖內容的剪輯矩形。

剪輯物件包含一組屬性，可讓您指定剪輯物件的圓角。 屬性可讓您設定剪切物件每個角落的 x 半徑和 y 半徑。

## <a name="animated-clip-rectangle"></a>動畫裁剪矩形

您可以藉由將動畫物件套用至剪輯物件的左邊、頂端、右邊和底部屬性，以動畫顯示剪輯矩形。 使用 [**IDCompositionVisual：： SetClip (IDCompositionClip)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) 多載方法，以將動畫裁剪矩形套用至視覺效果的剪輯屬性。

如需動畫物件的詳細資訊，請參閱 [動畫](animation.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectComposition 概念](directcomposition-concepts.md)
</dt> <dt>

[如何使用矩形剪輯物件裁剪](how-to--set-the-clip-rectangle-for-a-visual.md)
</dt> </dl>

 

 
