---
title: DWM 縮圖總覽
description: 桌面視窗管理員 (DWM) 可顯示應用程式視窗的縮圖表示。
ms.assetid: 6d71fcda-0cf0-463c-8c60-0415109d154f
keywords:
- 桌面視窗管理員 (DWM) 、縮圖
- DWM (桌面視窗管理員) 、縮圖
- 桌面視窗管理員 (DWM) 、縮圖關聯性
- DWM (桌面視窗管理員) 、縮圖關聯性
- 縮圖
- 縮圖關聯性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b333d84496828c451ff6e0eb7dbf3a86f91d629623d9939f66e874cfa82ee47d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279764"
---
# <a name="dwm-thumbnail-overview"></a>DWM 縮圖總覽

桌面視窗管理員 (DWM) 可顯示應用程式視窗的縮圖表示。 這些不是視窗的靜態快照集，而是縮圖來源視窗與接收即時縮圖轉譯之目的地視窗上的位置之間的動態、固定連接。 這可讓您快速查看執行中的應用程式，方法是將滑鼠停留在工作列上的應用程式上，或使用 ALT 鍵的按鍵手勢來查看並快速切換至應用程式。

下圖說明當您將滑鼠停留在工作列上的應用程式上時，所看到的 Windows Vista 即時縮圖。

![顯示將滑鼠停留在工作列上的應用程式上時，所看到的 D W 圖的螢幕擷取畫面。](images/dwm-livethumbnail.png)

下圖說明 DWM 啟用的 Windows Vista 翻轉 (ALT-TAB) 。

![啟用 dwm 的 alt 鍵的螢幕擷取畫面](images/dwm-flip.png)

> [!Note]  
> DWM 縮圖不會讓開發人員建立應用程式，例如 Windows Vista Flip3D (WINKEY]) 功能。 縮圖會直接轉譯至2D 中的目的地視窗。

 

## <a name="dwm-thumbnail-relationships"></a>DWM 縮圖關聯性

若要在您的應用程式中顯示縮圖，您必須先建立來源視窗與目的地視窗之間的關聯性。 這是藉由呼叫 [**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) 函數來完成。

[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) 不會轉譯目的地視窗上的縮圖，而只會建立關聯性並提供縮圖控制碼。 在設定了 [**DWM \_ 縮圖 \_ 屬性**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) 並呼叫 [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) 函式之後，會轉譯縮圖。 後續的 **DwmUpdateThumbnailProperties** 呼叫會以一組新的屬性來更新縮圖。 DWM 也提供 helper 函數 [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) ，以從縮圖取得來源視窗的大小。

若要結束縮圖的關聯性，請呼叫 [**DwmUnregisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) 函數。

下列範例示範如何使用 Windows desktop 建立 releationship，並將它顯示在應用程式中。


```
HRESULT hr = S_OK;
HTHUMBNAIL thumbnail = NULL;

// Register the thumbnail
hr = DwmRegisterThumbnail(hwnd, FindWindow(_T("Progman"), NULL), &thumbnail);
if (SUCCEEDED(hr))
{
    // Specify the destination rectangle size
    RECT dest = {0,50,100,150};

    // Set the thumbnail properties for use
    DWM_THUMBNAIL_PROPERTIES dskThumbProps;
    dskThumbProps.dwFlags = DWM_TNP_SOURCECLIENTAREAONLY | DWM_TNP_VISIBLE | DWM_TNP_OPACITY | DWM_TNP_RECTDESTINATION;
    dskThumbProps.fSourceClientAreaOnly = FALSE; 
    dskThumbProps.fVisible = TRUE;
    dskThumbProps.opacity = (255 * 70)/100;
    dskThumbProps.rcDestination = dest;

    // Display the thumbnail
    hr = DwmUpdateThumbnailProperties(thumbnail,&dskThumbProps);
    if (SUCCEEDED(hr))
    {
        // ...
    }
}
return hr;
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[桌面視窗管理員概觀](dwm-overview.md)
</dt> <dt>

[Enable and Control DWM Composition (啟用並控制 DWM 組合)](composition-ovw.md)
</dt> <dt>

[效能考慮和最佳作法](bestpractices-ovw.md)
</dt> </dl>

 

 




