---
title: AVICap 回呼函式
description: AVICap 回呼函式
ms.assetid: d238a238-9702-4ba6-92bd-5ef1605b4983
keywords:
- AVICap 類別，回呼函數
- AVICap 回呼函式，關於
- WM_CAP_SET_CALLBACK_CAPCONTROL 訊息
- WM_CAP_SET_CALLBACK_ERROR 訊息
- WM_CAP_SET_CALLBACK_FRAME 訊息
- WM_CAP_SET_CALLBACK_STATUS 訊息
- WM_CAP_SET_CALLBACK_VIDEOSTREAM 訊息
- WM_CAP_SET_CALLBACK_WAVESTREAM 訊息
- WM_CAP_SET_CALLBACK_YIELD 訊息
- capSetCallbackOnCapControl 宏
- capSetCallbackOnErrormacro
- capSetCallbackOnFrame 宏
- capSetCallbackOnStatus 宏
- capSetCallbackOnVideoStream 宏
- capSetCallbackOnWaveStream 宏
- capSetCallbackOnYield 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9edf96a6ff5b359acb6ef6d6a302b798742ffb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932547"
---
# <a name="avicap-callback-functions"></a>AVICap 回呼函式

您的應用程式可以使用捕捉視窗註冊回呼函式，讓它在狀態變更、發生錯誤、當影片畫面格和音訊緩衝區可供使用，以及在串流捕獲期間產生時，通知您的應用程式。 下列訊息會設定回呼函數。



| 訊息                                                                        | 描述                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CAP \_ 設定 \_ 回呼 \_ CAPCONTROL**](wm-cap-set-callback-capcontrol.md)   | 指定應用程式中呼叫的回呼函式，以提供對開始和結束的精確控制。 您也可以使用 [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) 宏來傳送此訊息。                   |
| [**WM \_ CAP \_ 設定 \_ 回呼 \_ 錯誤**](wm-cap-set-callback-error.md)             | 指定在發生錯誤時呼叫的應用程式中的回呼函數。 您也可以使用 [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) 宏來傳送此訊息。                                                           |
| [**WM \_ CAP \_ 設定 \_ 回呼 \_ 框架**](wm-cap-set-callback-frame.md)             | 指定在捕獲預覽框架時呼叫的應用程式中的回呼函數。 您也可以使用 [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) 宏來傳送此訊息。                                               |
| [**WM \_ CAP \_ 設定 \_ 回呼 \_ 狀態**](wm-cap-set-callback-status.md)           | 指定當狀態變更時所呼叫之應用程式中的回呼函數。 您也可以使用 [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) 宏來傳送此訊息。                                                      |
| [**WM \_ CAP \_ 設定 \_ 回呼 \_ M**](wm-cap-set-callback-videostream.md) | 指定當新的影片緩衝區變成可用時，在串流處理期間呼叫的應用程式中所呼叫的回呼函式。 您也可以使用 [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) 宏來傳送此訊息。 |
| [**WM \_ CAP \_ 設定 \_ 回呼 \_ WAVESTREAM**](wm-cap-set-callback-wavestream.md)   | 指定當新的音訊緩衝區變成可用時，在串流處理期間呼叫的應用程式中的回呼函式。 您也可以使用 [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) 宏來傳送此訊息。   |
| [**WM \_ CAP \_ 設定 \_ 回呼 \_ YIELD**](wm-cap-set-callback-yield.md)             | 指定在串流捕獲期間產生的應用程式中所呼叫的回呼函數。 您也可以使用 [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) 宏來傳送此訊息。                                         |



 

下列主題描述不同的回呼函式、傳送至函式的通知，以及其使用方式。

 

 




