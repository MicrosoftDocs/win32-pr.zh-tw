---
title: DirectComposition 的最佳作法
description: 本主題說明使用 Microsoft DirectComposition 的最佳作法。
ms.assetid: D3A1ECD4-9358-44B9-8A84-7D901219D5CD
keywords:
- DirectComposition 的最佳作法
- DirectComposition 的建議做法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0d19b82b188105c7914e89282c08b12dd4bdc4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683007"
---
# <a name="best-practices-for-directcomposition"></a>DirectComposition 的最佳作法

> [!NOTE]
> 針對 Windows 10 上的應用程式，我們建議使用 DirectComposition，而不是使用。 如需詳細資訊，請參閱 [使用視覺分層將您的桌面應用程式現代化](/windows/uwp/composition/visual-layer-in-desktop-apps)。

本主題說明使用 Microsoft DirectComposition 的最佳作法。

-   [最佳做法](#best-practices-for-directcomposition)
-   [安全性考量](#security-considerations)
-   [相關主題](#related-topics)

## <a name="best-practices"></a>最佳作法

下表提供使用 Microsoft DirectComposition 視覺效果的建議作法。



| 作法                                                                                                                                                                                                                                                        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 建立 DirectComposition 裝置之後，請呼叫 [**IDCompositionDevice：： CheckDeviceState**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-checkdevicestate) 方法以回應每個 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息，以確保裝置仍然有效。<br/> | 如果 Microsoft DirectX Graphic Infrastructure (DXGI) 裝置遺失，與 DXGI 裝置相關聯的 DirectComposition 裝置也會遺失。 當偵測到遺失的裝置時，DirectComposition 會將 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息傳送到所有視窗。 呼叫 [**CheckDeviceState**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-checkdevicestate) 以回應每個 **WM \_ 油漆** 訊息，可讓您判斷 DirectComposition 裝置物件是否仍然有效，如果不是，則採取步驟來復原內容。 <br/> 如需詳細資訊，請參閱 [裝置物件](basic-concepts.md)。<br/> |
| 只建立組合或動畫所需的視覺效果數目，並在 DirectComposition 完成使用後立即終結視覺效果。<br/>                                                                                            | DirectComposition 使用圖形處理器 (GPU) ，也就是您的應用程式與其他應用程式和作業系統共用的資源。 這種作法可確保所有應用程式和作業系統都會收到足夠的 GPU 資源。<br/> 如需詳細資訊，請參閱 [視覺效果](basic-concepts.md)。<br/>                                                                                                                                                                                                                                                                     |
| 請勿將透明度設為0% 來隱藏視覺效果;相反地，請從視覺化樹狀結構移除視覺效果。<br/>                                                                                                                                                          | 將不透明度設定為0% 需要的系統資源比從視覺化樹狀結構中移除更多。<br/> 如需詳細資訊，請參閱 [不透明度](effects.md) 和 [視覺化樹狀結構](basic-concepts.md)。<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| 請勿將空白 (零大小的空白) 裁剪矩形套用至視覺效果，以隱藏視覺效果。 請改為從視覺化樹狀結構移除視覺效果。 <br/>                                                                                                                 | 從視覺化樹狀結構移除視覺效果，可提供比套用空白剪輯矩形更好的效能。<br/> 如需詳細資訊，請參閱 [裁剪](clipping.md)。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 如果不需要剪切矩形，例如包含視覺效果整個點陣圖內容的剪輯矩形，請勿將剪輯矩形套用至視覺效果。<br/>                                                                                       | 不必要的剪輯矩形會危害系統效能。<br/> 如需詳細資訊，請參閱 [裁剪](clipping.md)。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 如果您需要大型的單一色彩點陣圖，請建立較小的點陣圖介面，然後套用尺規轉換，而不是建立完整大小的表面。 <br/>                                                                                                | 將縮放轉換套用至較小的介面時，所使用的系統資源比全尺寸介面少。<br/> 如需詳細資訊，請參閱 [點陣圖物件](bitmap-surfaces.md) 和 [轉換](transforms.md)。<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| 避免將3D 轉換套用至視覺化樹狀結構的多個層級，例如父代及其子代 (s) 。 <br/>                                                                                                                                        | 將3D 轉換套用至視覺化樹狀結構的多個層級可能會產生非預期的結果，因為3D 轉換不會在樹狀結構中相乘。 例如，在子系上 y 軸的90度旋轉，以及圍繞父代 y 軸的90度旋轉，會導致兩個視覺效果都旋轉到 nothing。<br/> 如需詳細資訊，請參閱[效果](effects.md)。<br/>                                                                                                                                                                                                     |



 

## <a name="security-considerations"></a>安全性考量

下列文章提供撰寫安全 c + + 程式碼的指引。

-   [C + + 的安全性最佳作法](/cpp/security/security-best-practices-for-cpp?view=vs-2019)
-   [適用于應用程式的模式 & 實務安全性指引](/previous-versions/msp-n-p/ff650760(v=pandp.10))

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何使用 DirectComposition](how-to-use-directcomposition.md)
</dt> </dl>

 

