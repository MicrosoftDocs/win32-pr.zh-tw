---
description: 本主題列出撰寫 Direct3D 應用程式時可能遇到的常見問題類別，以及如何防止這些問題。
ms.assetid: 27b87f0f-7118-4252-b6e8-6ea18a9399e4
title: '疑難排解 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 637ac4b43e8947a6011e35ae9a36db7829ed47fd4d5740f93778116e4ee8f9ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044076"
---
# <a name="troubleshooting-direct3d-9"></a>疑難排解 (Direct3D 9) 

本主題列出撰寫 Direct3D 應用程式時可能遇到的常見問題類別，以及如何防止這些問題。

## <a name="device-creation"></a>裝置建立

如果您的應用程式在裝置建立期間失敗，請檢查是否有下列常見的錯誤。

-   請務必檢查裝置的功能，特別是轉譯的深度。
-   檢查錯誤碼。 \_一律可以 D3DERR OUTOFVIDEOMEMORY。
-   使用 (Dll) 的偵錯工具 DirectX 動態連結程式庫，並在偵錯工具下查看輸出訊息。

## <a name="using-lit-vertices"></a>使用亮頂點

使用亮頂點的應用程式應該將 D3DRS \_ 光源轉譯狀態設為 **FALSE**，以停用 Direct3D 光源引擎。 根據預設，當啟用光源時，系統會將不含一般向量的任何頂點色彩設定為 0 (黑色) ，即使輸入頂點包含非零的色彩值也是如此。 由於頂點的本質不會包含頂點標準，因此，如果已啟用光源引擎，則在轉譯期間傳遞給 Direct3D 的任何色彩資訊都會遺失。

很明顯地，頂點色彩對執行它自己光源的任何應用程式都很重要。 若要防止系統強加預設值，請務必將 D3DRS \_ 光源設定為 **FALSE**。

如果您的應用程式執行，但未顯示任何內容，請檢查是否有下列常見的錯誤。

-   確定您的三角形不是退化的。
-   確定您的三角形未挑選。
-   請確定您的轉換在內部保持一致。
-   請檢查 [視口] 設定，以確定可以看見您的三角形。

## <a name="debugging"></a>偵錯

對 Direct3D 應用程式進行偵錯工具可能是一項挑戰。 除了檢查所有傳回值之外，您還可以嘗試下列技巧，這是 Direct3D 程式設計中特別重要的建議，其相依于非常不同的硬體。

-   切換至 debug Dll。
-   強制軟體專用裝置，即使可用，仍關閉硬體加速。
-   強制表面進入系統記憶體。
-   建立在視窗中執行的選項，讓您可以使用整合式偵錯工具。

這份清單中的第二個和第三個選項可協助您避免 Win16 鎖定，否則可能會導致偵錯工具停止回應。

此外，請嘗試新增下列專案以 Win.ini。


```
[Direct3D] 
debug=3 
[DirectDraw] 
debug=3 
```



## <a name="borland-floating-point-initialization"></a>Borland Floating-Point 初始化

Borland 的編譯器會以與 Direct3D 不相容的方式來報告浮點例外狀況。 若要解決這個問題，請包含 \_ matherr 例外狀況處理常式，如下所示：


```
// Borland floating point initialization 
#include <math.h>
#include <float.h>

void initfp(void)
{
    // Disable floating point exceptions
    _control87(MCW_EM,MCW_EM);
}

int _matherr(struct _exception  *e)
{
    e;               // Dummy reference to catch the warning
    return 1;        // Error has been handled
}
```



## <a name="parameter-validation"></a>參數驗證

基於效能的考慮，Direct3D 立即模式執行時間的 debug 版會執行比零售版本更多的參數驗證，這有時不會執行任何驗證。 這可讓應用程式使用較慢的偵錯工具執行時間元件來執行健全的偵錯工具，然後再使用更快速的零售版本來微調效能和最終發行版本。

雖然有幾個 Direct3D 立即模式方法會限制它們可接受的值，但通常只會檢查並強制執行 Direct3D 立即模式執行時間的偵錯工具版本的限制。 應用程式必須符合這些限制，在零售版 Direct3D 上執行時可能會發生無法預期且不想要的結果。 例如， [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 方法可接受參數 (PrimitiveCount) ，指出方法將會轉譯的基本專案數目。 方法只能接受0到 D3DMAXNUMPRIMITIVES 之間的值。 在 Direct3D 的 debug 版中，如果您傳遞超過 D3DMAXNUMPRIMITIVES 的基本專案，方法會正常失敗、將錯誤訊息列印到錯誤記錄檔，並將錯誤值傳回給您的應用程式。 相反地，如果您的應用程式在執行時間的零售版本上執行時，會產生相同的錯誤，則行為會是未定義的。 基於效能的考慮，方法不會驗證參數，因而導致無法預期的行為，而且在不正確情況下，會產生完全的狀況。 在某些情況下，呼叫可能會運作，而在其他情況下，可能會導致 Direct3D 中的記憶體錯誤。 如果不正確呼叫一致地使用特定的硬體設定和 DirectX 版本，則不保證它會繼續在其他硬體上運作，或使用較新的 DirectX 版本。

如果您的應用程式在執行零售 Direct3D 執行時間檔案時遇到未相關的失敗，請針對偵錯工具版本進行測試，並仔細查看您的應用程式傳遞無效參數的案例。 使用 DirectX 控制台小程式，視需要切換至偵錯工具執行時間，然後選取 [在 D3DError 時中斷] 選項。 此選項會強制執行時間使用 Windows DebugBreak 方法，以強制應用程式在偵測到應用程式錯誤時停止。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計提示](programming-tips.md)
</dt> </dl>

 

 
