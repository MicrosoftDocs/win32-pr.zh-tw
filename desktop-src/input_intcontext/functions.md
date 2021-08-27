---
title: 互動內容函數
description: 本節中的主題提供互動內容函數的參考規格。
ms.assetid: 0F34F181-D92C-4B08-9F1D-62379D4A2B15
keywords:
- 使用者互動
- input
- 指標
- 觸控
- 滑鼠
- 手寫筆
- 手寫筆
ms.topic: article
ms.date: 02/06/2020
ms.openlocfilehash: 5f0769aa5b9b097b23206c0515bd32552a59969404e72bbfcf26973d5d4f3de6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758334"
---
# <a name="interaction-context-functions"></a>互動內容函數

本節中的主題提供 [互動內容](interaction-context-portal.md) 函數的參考規格。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|---|---|
| [**AddPointerInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-addpointerinteractioncontext)<br/> | 在 [互動內容](interaction-context-portal.md) 物件所處理的指標集合中包含指定的指標。 <br/> |
| [**BufferPointerPacketsInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-bufferpointerpacketsinteractioncontext)<br/> | 將單一輸入指標的歷程記錄加入至 [互動內容](interaction-context-portal.md) 物件的緩衝區。<br/> |
| [**CreateInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-createinteractioncontext)<br/> | 建立並初始化 [互動內容](interaction-context-portal.md) 物件。<br/> |
| [**DestroyInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-destroyinteractioncontext)<br/> | 終結指定的 [互動內容](interaction-context-portal.md) 物件。<br/> |
| [**GetCrossSlideParameterInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getcrossslideparameterinteractioncontext)<br/> | 取得跨幻燈片互動行為。 <br/> |
| [**GetInertiaParameterInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getinertiaparameterinteractioncontext)<br/> | 取得操作 (轉換、旋轉、縮放) 的慣性行為。 <br/> |
| [**GetInteractionConfigurationInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getinteractionconfigurationinteractioncontext)<br/> | 取得 [互動內容](interaction-context-portal.md) 物件的互動設定狀態。<br/> |
| [**GetMouseWheelParameterInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getmousewheelparameterinteractioncontext)<br/> | 取得 [互動內容](interaction-context-portal.md) 物件的滑鼠滾輪狀態。 <br/> |
| [**GetPropertyInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getpropertyinteractioncontext)<br/> | 取得 [互動內容](interaction-context-portal.md) 物件屬性。<br/> |
| [**GetStateInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getstateinteractioncontext)<br/> | 取得目前的 [互動內容](interaction-context-portal.md) 狀態，以及內容將回到閒置狀態的時間。 <br/> |
| [**ProcessBufferedPacketsInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processbufferedpacketsinteractioncontext)<br/> | 在指標輸入框架的結尾處理緩衝的封包。<br/> |
| [**ProcessInertiaInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processinertiainteractioncontext)<br/> | 將計時器輸入傳送至 [互動內容](interaction-context-portal.md) 物件，以進行慣性處理。<br/> |
| [**ProcessPointerFramesInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processpointerframesinteractioncontext)<br/> | 處理一組指標輸入框架。<br/> |
| [**RegisterOutputCallbackInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-registeroutputcallbackinteractioncontext)<br/> | 註冊回呼，以接收來自 [互動內容](interaction-context-portal.md) 物件的互動事件。<br/> |
| [**RemovePointerInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-removepointerinteractioncontext)<br/> | 從 [互動內容](interaction-context-portal.md) 物件所處理的指標集合中移除指定的指標。 <br/> |
| [**ResetInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-resetinteractioncontext)<br/> | 將 [**互動狀態**](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state)、互動設定和所有參數重設為其初始狀態。 未通知即會取消目前的互動。 <br/> [互動內容](interaction-context-portal.md) 必須在下次使用之前重新設定。<br/> |
| [**SetCrossSlideParametersInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setcrossslideparametersinteractioncontext)<br/> | 設定跨幻燈片互動。 <br/> |
| [**SetInertiaParameterInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setinertiaparameterinteractioncontext)<br/> | 設定在取得連絡人之後，操作 (轉譯、旋轉、縮放) 的慣性行為。 <br/> | [**SetInteractionConfigurationInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setinteractionconfigurationinteractioncontext)<br/> | 設定 [互動內容](interaction-context-portal.md) 物件來處理指定的操作。<br/> |
| [**SetMouseWheelParameterInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setmousewheelparameterinteractioncontext)<br/> | 設定滑鼠滾輪輸入的參數值。 <br/> |
| [**SetPivotInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setpivotinteractioncontext)<br/> | 使用單一輸入指標，設定中央點以及來自中心點的 pivot 半徑，以進行旋轉操作。 <br/> |
| [**SetPropertyInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setpropertyinteractioncontext)<br/> | 設定 [互動內容](interaction-context-portal.md) 物件屬性。<br/> |
| [**StopInteractionCoNtext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)<br/> | 將 [**互動狀態**](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state) 設定為 [互動 \_ 狀態閒置] \_ ，並保持所有互動設定和參數保持不變。 系統會取消目前的互動，並視需要傳送通知。<br/> 在下一次使用之前，不需要重新設定[互動內容](interaction-context-portal.md)。<br/> |

## <a name="related-topics"></a>相關主題

[互動內容參考](interaction-context-reference.md)
