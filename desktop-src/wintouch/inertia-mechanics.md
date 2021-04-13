---
title: 慣性機制
description: 慣性機制
ms.assetid: 188b6936-b36e-4e57-9118-8b61ed134c17
keywords:
- Windows Touch，慣性
- Windows Touch，平滑動畫
- Windows Touch，彈性邊界
- 慣性，機制
- 慣性，計算基本概念
- 慣性，物理總覽
- 慣性，平滑動畫
- 慣性、彈性邊界
- 平滑動畫
- 彈性邊界
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be79b27900c6921c972710e7e922ab42b834afc1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300360"
---
# <a name="inertia-mechanics"></a>慣性機制

慣性可用來執行計算，以製作物件移動的動畫，並在併入 Windows Touch 的應用程式中啟用一般可用性支援。 本節將說明慣性啟用的下列功能。

-   慣性物理的簡短總覽。
-   使用速度與減速屬性來平滑物件動畫。
-   使用置換屬性平滑物件動畫。
-   使用彈性範圍從螢幕邊緣跳動。

## <a name="inertia-physics-overview"></a>慣性物理總覽

慣性處理器會使用簡單的物理模型，其中包含位置、減速值和初始速度。 時間是用來做為模型的動態輸入，以判斷正在取代之物件的目前位置。 下圖和公式概述用來計算物件位置的物理模型。

![圖例顯示用來計算物件位置的圖形和公式](images/velocity.png)

在用來計算目前位置 (x) 的公式中，初始速度 (v) 會乘以經過的時間 () ，並減少 (d) 次時間平方的最小速度。 這會導致物件的速度變得更順暢。 在上圖中，最左邊的第一個 () 的曲線部分，因為目前的速度是初始速度，所以物件很快就會移動。 在最後的 (最右邊) 部分的曲線，物件已完全停止，因為它的速度是0。 X 速度、y 速度和旋轉速度的物件速度計算，全都使用此公式來進行計算。

慣性處理器所使用的所有距離都是相對的。 如果您想要使用螢幕座標，請將螢幕座標傳遞給操作 (或慣性) 處理器;如果您想要使用絕對座標，請將這些座標傳遞到您所使用的處理器。 無論您使用的值為何，操作處理器都會使用毫秒的時鐘刻度來處理時間。 您可以使用 [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime) 方法，或透過呼叫來使用預設的時間 [**戳，將**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)這些值直接傳遞至慣性處理器。

## <a name="smooth-object-animation-using-the-velocity-and-deceleration-properties"></a>使用速度與減速屬性平滑物件動畫

您可以藉由設定慣性處理器介面中的速度和減速值，然後呼叫 [**進程**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)，來啟用平滑動畫。 呼叫 **進程** 將會觸發物件操作，而該操作接著應該會造成 UI 更新。 傳遞至慣性處理器的物件速度值通常會在完成時從操作處理器取得。 您的減速值會取決於您想要讓物件成為動畫的時間長度，以及您用來計算的單位。 因為這些值是相依的，有時您必須從 maniplation 處理器調整輸入速度，並使用任意值來因應速度。 下列值一般適用于您要將 centipixel 值從 [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) 結構的 x 和 y 屬性傳遞至操作處理器的各種案例。



| 狀況    | 屬性 Set                                                                       | 減速值 | 典型的速度輸入調整                                  | 備註                                                                                 |
|-------------|------------------------------------------------------------------------------------|--------------------|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| 翻譯 | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0.003 f             | 無。                                                           | 使用此值將會導致使用觸控輸入時的較長距離動畫。    |
| 翻譯 | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0.001 f             | 1/20 個觸控輸入的初始速度，無滑鼠輸入 | 使用這個值時，會在第二個指定的一般速度輸入周圍建立動畫。      |
| 翻譯 | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0.5 f               | 無                                                            | 使用這個值可讓您在大型的 Windows Touch 顯示器上自然覺得動畫。   |
| 旋轉    | [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0.000015 f          | 弧度已轉換為度。                                   | 使用此值會在使用觸控輸入時產生較長的旋轉動畫。      |
| 旋轉    | [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0.00001 f           | 1/40th 觸控輸入的旋轉差異，無滑鼠輸入   | 這個值是以弧度為單位，因此您必須使用極小的減速和速度值。 |
| 旋轉    | [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0.000005 f          | 無                                                            | 此值對於大型的 Windows Touch 顯示有自然的感覺。                        |



 

## <a name="smooth-object-animation-using-the-desired-displacement-property"></a>使用所需的置換屬性來平滑物件動畫

在某些情況下，您不會想要使用使用者的輸入來取代物件，但您仍然想要物件在螢幕上流暢地產生動畫。 在這種情況下，您可以使用慣性處理器中的置換屬性，讓處理器計算在畫面上移動物件的初始速度。

## <a name="controlling-object-position-using-elastic-bounds"></a>使用彈性界限控制物件位置

當您的物件是在螢幕上移動之後，您通常會想要在它離開使用者的觀點之前先將它停止。 慣性處理器會透過界限和彈性邊界屬性來啟用此功能。 下圖說明一般應用程式中的各種界限和邊界屬性。

![顯示界限和彈性 margin 屬性的螢幕擷取畫面](images/elastic-illustrated.png)

您可以為您的應用程式設定左、上、右、下限和彈性邊界，而慣性處理器將會處理在界限內保持 UI 元素的位置。 當物件達到彈性邊界時，它會變慢，直到到達界限為止。 它永遠不會在慣性期間保留該邊界，但仍會移動到物件的垂直慣性元件減速至0為止。 在圖例中，會將圓形朝左邊的彈性界限進行取代。 實心箭號會顯示操作的方向;實心圓圈是物件的初始位置;實心箭號是在圓形達到彈性邊界之前所做的變更;虛線箭號會顯示慣性處理器在達到邊界之後操作圓形的位置;而且虛線圓形會顯示物件停止的位置。

> [!Note]  
> 設定邊界屬性會向外移動界限。 例如，如果您的頂端界限設定為50，然後將最高彈性的邊界設定為10，則您的最上層界限將會有效地變成40。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[處理非受控碼中的慣性](handling-inertia-in-unmanaged-code.md)
</dt> <dt>

[慣性](getting-started-with-inertia.md)
</dt> <dt>

[操作](getting-started-with-manipulations.md)
</dt> </dl>

 

 




