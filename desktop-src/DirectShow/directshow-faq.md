---
description: DirectShow 常見問題
ms.assetid: 198758b9-025a-44af-958c-9ddea8cbb12d
title: DirectShow 常見問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d0959c4abb24509edd9c26d111e80a5af221d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510110"
---
# <a name="directshow-faq"></a>DirectShow 常見問題

本文將回答有關 Microsoft DirectShow 的許多常見問題。

**DirectShow 支援哪些作業系統？**

DirectShow 適用于所有支援的 Windows 版本。

**我需要使用 DirectShow 進行程式設計的 COM 知識有多高？**

針對應用程式開發，您必須瞭解使用 COM 物件的基本概念：如何將它們具現化、存取它們所公開的介面，以及管理這些介面的參考計數。 篩選開發需要更多的 COM 知識。

**DirectShow 支援哪些格式？**

請參閱 [DirectShow 中支援的格式](supported-formats-in-directshow.md)。

**有 (HCL) 的 DirectShow 硬體相容性清單嗎？**

不會。 DirectShow 使用 Microsoft DirectDraw 和 Microsoft DirectSound 硬體功能（如果有的話）。 當沒有特殊硬體可用時，DirectShow 會使用 GDI 來繪製影片，並使用 **waveOut** \* 多媒體 api 來播放音訊。

**我可以使用哪些語言來撰寫 DirectShow 應用程式？**

DirectShow 主要是針對 c + + 開發所設計。 您可以透過 Visual Basic 6.0 來公開 DirectShow API 的小型子集合;不過，這項功能已被取代。

**您是否可以透過受控碼來存取 DirectShow？**

Microsoft 目前沒有任何計畫可實行受控的 DirectShow API。

**我需要什麼編譯器才能進行 DirectShow 開發？**

只要編譯器的環境已正確設定，任何能夠產生元件物件模型 (COM) 物件的編譯器都應可運作。

**DirectShow 與 Microsoft DirectX 有何關聯？**

在內部，當硬體支援時，DirectShow 會使用 DirectSound 和 DirectDraw。 影片轉譯器和覆迭混音器篩選器會使用 DirectDraw 3 和 DirectDraw 5 的表面。 影片混用轉譯器 7 (Windows XP 只) 使用 DirectDraw 7 表面。 影片混合轉譯器9和增強型影片轉譯器會使用最新的 Microsoft Direct3D Api。 您不需要使用其他 DirectX Api 來撰寫 DirectShow 應用程式，雖然可以將它們合併。

**DirectShow 與 Microsoft ActiveMovie 有何關聯？**

ActiveMovie 是 DirectShow 的原始名稱。 詞彙 ActiveMovie 已不再使用。

**GraphEdit 公用程式是否有原始程式碼可供使用？可以轉散發 GraphEdit 嗎？**

否，來源無法使用，而且 Graphedt.exe 無法轉散發。

**DMOs 更換 DirectShow 篩選嗎？**

Microsoft DirectX Media 物件 (DMOs) 可用於 DirectShow 應用程式。 針對編碼器、解碼器和效果，建議您撰寫一則，而非 DirectShow 篩選。  (注意：如果您想要在您的解碼器中使用 DirectX Video 加速，您必須將它實作為篩選器。 ) 基於其他用途，DirectShow 篩選器可能更適合。 如需 DMOs 的詳細資訊，請參閱 [DirectX 媒體物件](directx-media-objects.md)。

**我要使用 Windows Media Player 來播放 AVI 格式檔案。我可以聽到音訊，但似乎沒有任何影片，而只是看到黑色。怎麼了？**

檔案可能是以您系統上不存在的編解碼器編碼。 雖然 AVI 檔案格式很常見，但您可以使用許多不同的壓縮格式來建立 AVI 檔案 (編解碼器) 。 如果您嘗試播放的 AVI 檔案使用不支援的編解碼器，您可能會聽到音訊元件，但影片會顯示為黑色畫面，或螢幕內容將保持不變。

> [!Note]  
> 如果您的系統上沒有編解碼器，Windows Media Player 通常會嘗試下載並安裝它。

 

**如何? 建立我的應用程式？我需要哪些程式庫和標頭檔？**

請參閱 [設定組建環境](setting-up-the-build-environment.md)。

**GraphEdit 會顯示許多未記載的篩選準則。這些篩選準則為何？**

GraphEdit 會列舉在您的系統上的篩選準則類別中註冊的所有篩選準則。 這可能包括由協力廠商應用程式安裝的篩選，或其他 Microsoft 技術（例如 Windows Media 或 NetMeeting）所安裝的篩選。 此外，某些 DirectShow 篩選器可作為編解碼器或硬體裝置的包裝函式，每個編解碼器或裝置會顯示為不同的篩選準則。 Microsoft h.264 Video 編解碼器是由 NetMeeting 使用，且在 DirectShow 中已不再受支援。 如需詳細資訊，請參閱 [列舉裝置和篩選器](enumerating-devices-and-filters.md)。

**我在以程式設計方式建立自訂圖形時遇到問題。**

首先，嘗試使用 GraphEdit 來建立篩選圖形。 這項工具可讓您快速模擬許多可能性。 GraphEdit 在嘗試以原始程式碼建立之前，一律是測試圖形的絕佳位置。

如需有關圖形建立的詳細資訊，請參閱下列文章：

-   [建立篩選圖形](building-the-filter-graph.md)
-   [列舉篩選圖形中的物件](enumerating-objects-in-a-filter-graph.md)

**如何偵測指定電腦上是否已安裝 DirectShow？**

呼叫 **CoCreateInstance** 以建立篩選圖形管理員的實例。 如果此呼叫成功，則會在電腦上安裝 DirectShow。 下列程式碼示範如何執行這項作業：


```C++
IGraphBuilder *pGraph;

HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void **) &pGraph);
```



**如何? 變更篩選器的設定，而不顯示內容頁嗎？**

大部分的篩選器會公開一或多個介面來設定篩選準則的屬性。 請參閱 [參考] 頁面中有問題的篩選。  (查看 [DirectShow 篩選器](directshow-filters.md)。 ) 

**我可以使用 GraphEdit 來測試篩選嗎？**

當您正在開發篩選器時，GraphEdit 可協助您將篩選之間的連接視覺化。 它也可以提供篩選功能的快速測試。 但是，它並不是健全的測試平臺。

**篩選準則會在哪個特殊許可權環形執行？**

篩選準則會在 ring 3 執行，不過某些篩選器會控制在 ring 0 執行的串流裝置。 如需詳細資訊，請參閱 [硬體裝置如何參與篩選圖形](how-hardware-devices-participate-in-the-filter-graph.md)。

**我是否需要使用內核偵錯工具？**

這取決於您的特定專案。 安裝 DirectX 偵錯工具執行時間程式庫表示您會安裝 debug 驅動程式和其他核心模式元件，如果您的應用程式在其中一個元件中造成 debug assert，則您的電腦將會自動重新開機，除非您已將內核偵錯工具附加至您的進程。

**當我在偵錯工具中執行應用程式時，它會當機。**

當應用程式附加至偵錯工具時，某些解碼器設計為無法運作。 嘗試在偵錯工具外執行應用程式。

**定義 \_ GUID 宏的運作方式為何？**

**定義 \_ guid** 宏可解決在 `extern` 原始程式碼中宣告 GUID 值參考的問題。 例如，假設您的專案有三個原始程式檔： Src1 .cpp、Src2 收取 .cpp 和 Src3 .cpp，而這三個檔案都使用您已定義的特定 GUID 值。 您必須在專案中明確定義 GUID 值一次，而其他原始程式檔必須宣告 `extern` 它的參考。 使用 **DEFINE \_ GUID** 宏，您可以使用相同的標頭檔來進行這兩種用途。 在您的標頭檔中，宣告 GUID，如下所示：


```C++
DEFINE_GUID(CLSID_MyObject, 
0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



 (在此範例中為零，請放入實際的 GUID 值。 ) 您可以使用 Guidgen.exe 公用程式來建立新的 GUID，並將其貼入 **定義 \_ guid** 格式的標頭檔中。 在每個參考 GUID 的原始程式檔中包含此標頭檔。 在剛好一個原始程式檔中，將標頭檔 Initguid 包含在標頭檔之前。 例如：


```C++
// Src1.cpp
#include <initguid.h>
#include "MyGuids.h"

// Src2.cpp
#include "MyGuids.h"

// Src3.cpp
#include "MyGuids.h"
```



無論 Initguid .h 標頭檔不包含在內， **DEFINE \_ guid** 宏都會建立 `extern` guid 值的參考。 包含 Initguid .h 標頭檔時，會重新定義 **定義 \_ guid** 宏，讓 **定義 \_ guid** 建立 guid 的定義宣告。

如果您沒有在任何來源檔案中包含 Initguid，您將會收到「無法解析的外部符號」連結錯誤。 如果您在相同的 GUID 中包含 Initguid 兩次，您將會收到編譯錯誤「重新定義;多重初始化」。 若要解決這些錯誤，請確定 Initguid 只包含一次。 此外，請勿在先行編譯標頭檔中包含 Initguid，因為在效果中，先行編譯標頭檔會包含在每個原始程式檔中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow 簡介](introduction-to-directshow.md)
</dt> </dl>

 

 



