---
description: 結合影片捕獲和預覽
ms.assetid: bffc1900-be05-4d7e-ab8d-3177365aeb7a
title: 結合影片捕獲和預覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d1a3dd3df30bd13aa6fdae7e39894941071df8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467555"
---
# <a name="combining-video-capture-and-preview"></a>結合影片捕獲和預覽

前幾節說明如何將影片捕獲到各種不同的檔案格式。 [預覽影片](previewing-video.md)一節說明如何建立即時預覽圖形。 不過，許多應用程式必須同時進行這兩項作業。 若要建立合併的預覽和檔案撰寫圖形，只要對 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)進行兩個呼叫即可：


```C++
// Render the preview stream to the video renderer.
hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap, 
    NULL, NULL);

// Render the capture stream to the mux.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap, 
    NULL, pMux);
```



在此程式碼中，[Capture Graph Builder] 會隱藏一些詳細資料：

-   如果捕捉篩選具有預覽 pin 或影片埠 pin，加上捕捉釘選， [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法就會直接轉譯這兩個針腳，如下圖所示。

    ![捕獲和預覽圖形](images/vidcap04.png)

-   如果篩選準則只有一個捕捉 pin，則「捕獲圖形產生器」會使用 [智慧型](smart-tee-filter.md) 指標篩選器來分割 capture 資料流程。 下圖顯示具有智慧型 t 的圖形。

    ![使用智慧型 t a 濾波器來捕捉和預覽圖形](images/vidcap05.png)

智慧型指標篩選器具有 capture 釘選和預覽 pin。 它會從 capture 篩選器取得單一影片串流，並將其分割成兩個串流，一個用於捕獲，另一個用於預覽。 為了維持捕獲 pin 的輸送量，預覽 pin 會視需要卸載畫面格。 它也會在傳遞之前，從每個樣本中去除時間戳記，原因是「 [DirectShow 影片捕獲篩選](directshow-video-capture-filters.md)」主題中所討論的原因。

雖然智慧型 t 會分割資料流程，但它並不會實際複製影片資料。 相反地，它會使用共用緩衝區的自訂媒體範例物件。 這些範例會標示為「唯讀」，以確保下游篩選不會寫入資料。

如果您的 capture graph 有預覽視窗，則有幾件事可能會導致篩選圖形管理員停止整個圖形，包括 capture 資料流程：

-   鎖定電腦。
-   在屬於網域成員的電腦上按 CTRL + ALT + DELETE。
-   執行全螢幕 Direct3D 應用程式，例如遊戲或螢幕保護裝置程式。
-   切換監視器或變更顯示器解析度。
-   執行程式，讓 Windows 顯示 (UAC) 對話方塊中的 [使用者帳戶控制]。  (Windows Vista 或更新版本。 ) 
-   正在執行全螢幕 DOS 視窗。

這些事件中的任何一項可能都會中斷捕捉會話，可能會導致資料遺失。  (以下是內部發生的情況：影片轉譯器會遺失所需的 Direct3D 或 DirectDraw 資源。 在復原這些資源的過程中，影片轉譯器必須重新連接上游篩選器，導致篩選圖形管理員停止圖形。 ) 

此問題有兩個可能的解決辦法如下：

-   請勿包含預覽資料流程。 不過，請注意，當 capture 裝置有影片埠 pin 時， [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法會自動新增預覽視窗。 請參閱檔案 [捕捉中的影片埠 pin](video-port-pins-in-file-capture.md)。
-   使用串流緩衝區引擎，將預覽資料流程傳送至另一個進程中的圖形。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將影片捕獲至檔案](capturing-video-to-a-file.md)
</dt> </dl>

 

 



