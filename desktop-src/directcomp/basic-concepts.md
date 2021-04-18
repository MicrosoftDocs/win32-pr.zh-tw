---
title: " (DirectComposition 的基本概念) "
description: 本主題概要說明 Microsoft DirectComposition 的基本概念。
ms.assetid: F442BDCA-C913-4438-BFFA-D3F28B68EE85
keywords:
- DirectComposition 概念
- DirectComposition 基本概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0550dc12cb0dcc5262701658d8e3883ee1ce8d82
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104565485"
---
# <a name="basic-concepts"></a>基本概念

> [!NOTE]
> 針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。 如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。

本主題概要說明 Microsoft DirectComposition 的基本概念。 它包含下列區段：

-   [Composition](#composition-target-window)
-   [視覺效果](#visuals)
    -   [視覺化樹狀結構](#visual-tree)
    -   [視覺物件的屬性](#properties-of-a-visual-object)
-   [裝置物件](#device-object)
-   [撰寫目標視窗](#composition-target-window)
-   [交易式撰寫](#transactional-composition)
    -   [批次處理](#batching)
    -   [同步處理](#synchronization)
    -   [跨裝置的視覺化樹狀結構](#cross-device-visual-trees)
-   [相關主題](#related-topics)

## <a name="composition"></a>Composition

DirectComposition 會將 *組合* 定義為點陣圖的集合，這些點陣圖會透過套用各種轉換、效果和動畫來產生應用程式 UI 中的視覺效果結果來結合和操作。 DirectComposition 僅適用于點陣圖內容;它不支援向量或文字。 DirectComposition 不提供點陣圖內容。 相反地，它會提供可讓使用者使用 D2D、DXGI 或上傳自己的材質內容來繪製的介面。

DirectComposition 應用程式會建立兩組物件來組成場景：組合在一起的點陣圖，以及定義點陣圖之間空間關聯性的視覺效果。 如需 DirectComposition 所支援點陣圖物件的詳細資訊，請參閱 [點陣圖物件](bitmap-surfaces.md)。

## <a name="visuals"></a>視覺效果

*視覺效果* (或 *視覺物件*) 是 DirectComposition 的基本元素。 它們是您用來在應用程式 UI 中建立組合和動畫的基本組建區塊。

在程式設計術語中，視覺效果是具有一組屬性的物件，並公開用來設定屬性值的介面。 視覺效果的 [內容] 屬性會將特定點陣圖與視覺效果建立關聯，而其他屬性則會控制 DirectComposition 在轉譯至螢幕時的位置和操作視覺效果。

如需詳細資訊，請參閱 [視覺效果的屬性](#properties-of-a-visual-object)。

### <a name="visual-tree"></a>視覺化樹狀結構

DirectComposition 會從名為 *視覺化樹狀* 結構的視覺化物件階層式集合建立組合。 樹狀結構根目錄的視覺效果稱為 *根視覺* 效果，而且可以有一或多 *個子視覺效果* 與其相關聯。 子視覺效果可以有自己的一或多個子視覺效果。 任何有相關聯子視覺效果的視覺效果稱為 *父視覺* 效果，而且共用相同父系的所有子視覺效果都稱為「 *同級視覺效果*」。 特定視覺效果及其所有子系和附屬視覺效果都稱為 *視覺化子樹*。

樹狀結構中的視覺位置可協助您決定其螢幕位置，以及相對於組合中其他視覺效果的迭置順序。 根視覺效果的位置相對於轉譯轉譯之目標視窗的工作區左上角。 所有子視覺效果都是相對於其父項視覺效果 (的左上角，或是 TransformParent 屬性) 所指定的視覺效果，而且一律會以迭置順序出現在其父系的前方。

下圖顯示視覺效果的組合，以及用來產生組合的視覺化樹狀結構結構。 Visual 1 是根視覺效果，也是子視覺效果2和3的父系，也就是同級視覺效果。 Visual 3 有其本身的兩個子視覺效果，也就是視覺效果4和5。 視覺效果三至5組成的視覺效果子樹。

![視覺效果和對應的視覺化樹狀結構的組合](images/visuals-and-corresponding-tree.png)

父視覺效果會維護其子視覺效果的排序清單。 當同級視覺效果的位置，使其彼此重迭時，DirectComposition 會根據其在父視覺效果的子清單中出現的順序，來設定同級的迭置順序。 稍後在清單中的同級會放置在清單中稍早出現的所有兄弟前面。 下圖顯示重迭子視覺效果的迭置順序。

![重迭子視覺效果的迭置順序](images/overlapping-child-visuals.png)

### <a name="properties-of-a-visual-object"></a>視覺物件的屬性

視覺物件會公開一組屬性，可讓您設定視覺效果的點陣圖內容，以及控制 DirectComposition 的位置和操作視覺內容。 下列各節將詳細說明每個屬性。

-   [內容屬性](#content-property)
-   [剪輯屬性](#clip-property)
-   [BorderMode 屬性](#bordermode-property)
-   [BitmapInterpolationMode 屬性](#bitmapinterpolationmode-property)
-   [CompositeMode 屬性](#compositemode-property)
-   [OffsetX 和 OffsetY 屬性](#offsetx-and-offsety-properties)
-   [Effect 屬性](#effect-property)
-   [Transform 屬性](#transform-property)
-   [TransformParent 屬性](#transformparent-property)

### <a name="content-property"></a>內容屬性

視覺效果的 Content 屬性會指定與視覺效果相關聯的點陣圖內容。 這是當您在組合中包含視覺效果時，DirectComposition 所使用的點陣圖。

您可以藉由呼叫 [**IDCompositionVisual：： SetContent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcontent) 方法來設定視覺效果的 Content 屬性。

如需 DirectComposition 所支援點陣圖內容類型的詳細資訊，請參閱 [點陣圖物件](bitmap-surfaces.md)。

### <a name="clip-property"></a>剪輯屬性

視覺效果的 [剪輯] 屬性會指定一個矩形區域，稱為 *裁剪區域* (或 *裁剪矩形*) 。 轉譯視覺效果時，只會顯示落在裁剪區域內的視覺效果部分，而在裁剪區域外部延伸的任何內容則會被裁剪 (也就是不會顯示) 。 DirectComposition 支援具有圓角或方框的裁剪區域。

您可以藉由呼叫 [**IDCompositionVisual：： SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) 方法來設定視覺效果的剪輯屬性。

如需詳細資訊，請參閱 [裁剪](clipping.md)。

### <a name="bordermode-property"></a>BorderMode 屬性

BorderMode 屬性會指定如何撰寫與此視覺效果相關聯的點陣圖和剪輯邊緣，或在子樹中的視覺效果中使用視覺效果。

框線模式會影響點陣圖的邊緣在轉換點陣圖時的組成方式，讓邊緣不會與整數座標組齊軸。 它也會影響在具有圓角的剪輯角落以及已轉換之剪輯邊緣的內容裁剪方式，讓邊緣與整數座標不對齊軸。

如需詳細資訊，請參閱 [**IDCompositionVisual：： SetBorderMode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setbordermode)。

### <a name="bitmapinterpolationmode-property"></a>BitmapInterpolationMode 屬性

BitmapInterpolationMode 屬性會告知 DirectComposition 如何在轉換點陣圖時撰寫點陣圖，讓點陣圖中的圖元與螢幕上的圖元之間沒有一對一的對應關係。

您可以藉由呼叫 [**IDCompositionVisual：： SetBitmapInterpolationMode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setbitmapinterpolationmode) 方法來設定視覺效果的 BitmapInterpolationMode 屬性。

### <a name="compositemode-property"></a>CompositeMode 屬性

CompositeMode 屬性會指示 DirectComposition 如何 blend 視覺效果的點陣圖內容與轉譯目標。 如需支援的複合模式的描述，請參閱 [**DCOMPOSITION \_ 複合 \_ 模式**](/windows/desktop/api/DcompTypes/ne-dcomptypes-dcomposition_composite_mode)。

您可以藉由呼叫 [**IDCompositionVisual：： SetCompositeMode**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setcompositemode) 方法來設定視覺效果的 CompositeMode 屬性。

### <a name="offsetx-and-offsety-properties"></a>OffsetX 和 OffsetY 屬性

OffsetX 和 OffsetY 屬性會指示 DirectComposition 要以水準和垂直方式放置視覺效果的位置。 它們會定義二維固定位置，而視覺效果的所有轉換和效果都會從這個位置計算。

針對根視覺效果，OffsetX 和 OffsetY 屬性會定義相對於主控視覺效果的視窗左上角之點的 x 座標和 y 座標。 針對子視覺效果，座標是相對於父代的左上角，如果指定了 [TransformParent 屬性](#transformparent-property) ，則為指定之視覺效果的左上角。 轉譯視覺效果時，會將視覺效果左上角的位置與指定的座標相符。

您可以藉由呼叫 [**IDCompositionVisual：： SetOffsetX**](/previous-versions/windows/desktop/legacy/hh449126(v=vs.85)) 和 [**SetOffsetY**](/previous-versions/windows/desktop/legacy/hh449131(v=vs.85)) 方法來設定視覺效果的 OffsetX 和 OffsetY 屬性。

### <a name="effect-property"></a>Effect 屬性

[效果] 屬性可讓您指定效果或效果群組，以修改視覺效果及其子樹的組成方式。 例如，您可以指定控制視覺效果不透明度的效果，並以各種方式混合視覺效果與另一個點陣圖，並將透視圖轉換套用至視覺效果。

您可以藉由呼叫 [**IDCompositionVisual：： SetEffect**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-seteffect) 方法來設定視覺效果的效果屬性。

如需詳細資訊，請參閱[效果](effects.md)。

### <a name="transform-property"></a>Transform 屬性

轉換屬性會指定二維 (2D) 轉換或2D 轉換的群組，以便 DirectComposition 在視覺效果上執行。 轉換 (或轉換) 是一種作業，可修改視覺效果相對於其父代的座標系統，或是相對於 [TransformParent 屬性](#transformparent-property)所指定的視覺效果。 您可以使用轉換來改變視覺效果的位置、大小或本質，方法是將它移到另一個位置， (轉譯) ，使其變得更大或更小 (調整) 、將它轉換 (旋轉) 、扭曲圖形 (扭曲) 等等。

您可以藉由呼叫 [**IDCompositionVisual：： SetTransform**](/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)) 方法來設定視覺效果的轉換屬性。

如需詳細資訊，請參閱[轉換](transforms.md)。

### <a name="transformparent-property"></a>TransformParent 屬性

視覺效果的座標系統是由 OffsetX、OffsetY 和 Transform 屬性修改。 一般來說，這些屬性會定義視覺效果相對於其直屬父系的座標系統。 若要使用父系以外的某些視覺作為子視覺效果座標系統的基礎，請使用 TransformParent 屬性，將不同的視覺效果指定為「父系」，以供轉換之用。

您可以藉由呼叫 [**IDCompositionVisual：： SetTransformParent**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransformparent) 方法來設定視覺效果的 TransformParent 屬性。

## <a name="device-object"></a>裝置物件

若要使用 DirectComposition，您必須建立和操作 (COM) 物件的各種元件物件模型。 您需要建立的第一個物件是 DirectComposition *裝置物件* ，因為它是用來建立組合中所有其他物件的 factory。

您可以藉由呼叫 [**DCompositionCreateDevice**](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice) 函式來建立裝置物件，該函式會傳回 [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) 介面指標。 這個介面會公開一組方法，您可以用來建立視覺物件、剪輯物件、動畫物件、轉換物件、效果物件等等。

裝置物件除了做為建立其他物件的 factory 之外，還提供另一個用途。 它會公開稱為 [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) 的方法，此方法會將視覺化樹狀結構傳遞至 DirectComposition 進行處理。 如需詳細資訊，請參閱 [交易式組合](#transactional-composition)。

請記住，雖然您可以在應用程式中建立裝置物件的多個實例，但您在特定組合中使用的所有物件都必須由相同的裝置物件建立，但有一個例外：您可以在相同的視覺化樹狀結構中結合來自不同裝置物件的視覺物件。 當您這樣做時，DirectComposition 會如往常般將視覺化樹狀結構視為一樣，只不過樹狀結構中特定視覺物件的變更只會在建立視覺物件的裝置物件上呼叫 [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) 方法時才會生效。

從相同視覺化樹狀結構中的不同裝置使用視覺效果的能力，可讓多個執行緒建立和操作單一視覺化樹狀結構，同時維護兩個獨立的裝置，可用來以非同步方式認可變更。 如需詳細資訊，請參閱 [跨裝置的視覺化樹狀](#cross-device-visual-trees)結構。

## <a name="composition-target-window"></a>撰寫目標視窗

視覺化樹狀結構必須系結至視窗，您才能在畫面上顯示任何樹狀結構的視覺效果。 稱為「 *撰寫目標」視窗* 的視窗可以是最上層視窗或子視窗。 此外，撰寫目標視窗可以是分層視窗;也就是說，它可以有 [**WS \_ EX \_ 分層**](/windows/desktop/winmsg/extended-window-styles) 視窗樣式。

DirectComposition 可讓應用程式將最多兩個視覺樹狀結構系結至每個視窗。 視覺化樹狀結構包含一個是以視窗本身為基礎，但在所有視窗的子視窗後方，另一個則是在視窗頂端和子視窗上方組成的。 換句話說，每個視窗都有四個概念層，而且所有圖層都會裁剪至目標視窗的可見區域。 下圖顯示視窗的四個概念層。

![視窗的概念層](images/directcomposition-layers.png)

## <a name="transactional-composition"></a>交易式撰寫

DirectComposition 會使用交易式模型，在此模型中，您會建立一組批次的視覺效果變更，然後「認可」設定為 DirectComposition，以便一次處理所有的變更。 您可以修改相同的 DirectComposition 視覺物件，並認可任何次數的變更。 當桌面視窗管理員 (DWM) 收取批次時，它會挑選所有暫止的批次，並依認可的順序將它們套用至下一個框架。

單一認可內的所有變更都保證會套用至單一框架。 因為 DWM 會針對每個畫面格收集一次批次，所以您只能針對每個畫面格修改任何特定的物件。 修改不同物件的後續認可也可能套用至目前的框架，但 DirectComposition 並不保證這些變更會發生在相同的框架中。

[**IDCompositionSurface：： BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)和 [**IDCompositionSurface：： EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)方法可讓您同步處理轉譯更新與視覺效果更新。 例如，您可以呼叫 **IDCompositionSurface：： BeginDraw**、更新視覺效果的 OffsetX 和剪輯屬性、呼叫 [**IDCompositionDevice：： Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)、使用 Microsoft DirectX 繪製內容，然後呼叫 **IDCompositionSurface：： EndDraw**。 在此情況下，Microsoft DirectComposition 可確保同時更新點陣圖內容和視覺屬性。

### <a name="batching"></a>批次處理

您可以在相同的框架內，針對相同的視覺效果或多項不同視覺效果的變更，認可多個變更。 在相同的框架內對相同的視覺效果進行多項變更時，請記住下列幾點：

-   如果您對視覺效果的相同屬性進行多項變更，則只會套用最後一個變更。 例如，如果您將不透明度設定為0，然後設定為0.5，最後到1.0，則只會將不透明度1.0 套用至視覺效果。
-   如果您變更相同視覺效果的多個屬性，DirectComposition 會先將變更套用至視覺效果，再套用至任何子視覺效果。 屬性會依下列順序套用，而不論您指定的順序為何：

    1.  Offset
    2.  轉換
    3.  裁剪
    4.  效果

    下圖顯示將這四個屬性套用至視覺效果的結果。

    ![將全部四個屬性套用至視覺效果的結果](images/order-of-properties.png)

    請記住，所有變更會一次套用至相同框架內容中的視覺效果。 這表示，從使用者的觀點來看，視覺效果的變更會立即發生。

-   針對 [轉換] 屬性，您可以使用 [**IDCompositionDevice：： CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) 來建立一組要套用至視覺效果的轉換。 DirectComposition 會依照您指定的順序套用轉換。
-   針對 [效果] 屬性，您可以使用 [**IDCompositionEffectGroup**](/windows/win32/api/dcomp/nn-dcomp-idcompositioneffectgroup) 來套用一組效果。 DirectComposition 會依照您指定的順序套用效果。 此外，在套用目前視覺效果中的所有3D 轉換之後，3D 透視轉換會導致視覺化樹狀結構的簡維化。 這有助於確保產生的視覺效果盡可能接近3D。

### <a name="synchronization"></a>同步處理

您的應用程式可以同時從多個執行緒呼叫 DirectComposition。 執行順序可保證順序調用，但不能用於並行呼叫。 例如，如果執行緒 A 修改了視覺效果，而執行緒 B 同時認可該批次，則不會定義該視覺效果變更是否包含在認可的批次中，或是否要啟動新的批次。 另一方面，如果您的應用程式使用其他同步處理機制來確保在另一個方法之前呼叫，DirectComposition 會接受呼叫順序，並處理這些呼叫的方式，就好像這兩個呼叫都是從單一執行緒的順序發出。

### <a name="cross-device-visual-trees"></a>跨裝置的視覺化樹狀結構

DirectComposition 物件不是執行緒系結;您可以使用多個執行緒來修改相同的物件集。 不過，共用相同的裝置物件時，請注意下列問題。

-   這兩個執行緒都必須能夠呼叫 [**IDCompositionDevice：： Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)。 如果只有一個執行緒呼叫 **IDCompositionDevice：： Commit**，另一個執行緒無法將其任何變更認可至 DirectComposition。
-   當某個執行緒呼叫 [**IDCompositionDevice：： Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) 時，如果另一個執行緒仍進行的變更要成為相同交易的一部分，交易行為可能會遺失。

如果您需要將多個同時交易認可至 DirectComposition，您必須使用多個裝置物件，可能來自多個執行緒。 在此案例中，兩個裝置物件會共用相同的視覺化樹狀結構，而每個裝置物件會認可自己的交易。

下圖顯示由兩個裝置物件共用的視覺化樹狀結構。 視覺效果1、2、4和5是由一或多個裝置所擁有，但 visual 3 會由這兩個裝置共用，因此可用於將兩個子樹狀結構連接至單一、較大的視覺化樹狀結構。 共用視覺化樹狀結構可讓您以非同步方式從兩個不同的執行緒操作兩個裝置。

![由兩個裝置共用的視覺化樹狀結構](images/shared-visual-tree-1.png)

若要說明在兩個裝置之間共用視覺樹狀結構的實用性，請考慮啟用低延遲觸控輸入的架構。 架構可以使用兩個執行緒，一個處理大部分的 UI 工作，另一個則是專門用來處理觸控輸入事件的執行緒。 觸控執行緒會根據使用者輸入手勢來更新特定視覺效果的轉換。 藉由更新轉換，觸控執行緒可以讓該視覺效果底下的整個子樹遵循使用者的手指、在使用者執行多點觸控手勢等情況下擴大或縮小。 UI 執行緒會保留大部分組合樹狀結構的擁有權，而觸控執行緒只擁有標記為非同步觸控回應的幾個視覺效果。 下圖顯示這類組合樹狀結構的簡化版本：

![ui 執行緒和觸控執行緒之間共用的視覺化樹狀結構](images/shared-visual-tree-2.png)

一般而言，UI 執行緒只會修改它所擁有的視覺效果，而觸控執行緒只會修改共用視覺效果。 唯一的例外狀況是建立或終結已啟用觸控的子樹。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IDCompositionSurface::BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)
</dt> <dt>

[**IDCompositionSurface::EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)
</dt> <dt>

[**IDCompositonDevice：： Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)
</dt> <dt>

[DirectComposition 概念](directcomposition-concepts.md)
</dt> </dl>

 

 