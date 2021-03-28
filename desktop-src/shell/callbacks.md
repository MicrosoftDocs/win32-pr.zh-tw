---
description: 本節說明 Windows Shell 回呼函數。
title: Shell 回呼函數
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 617a73d9-e3e6-4def-a5b2-557faa7b03c0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4f6ae93437caa740c8c1349690b7e1452a032491
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386120"
---
# <a name="shell-callback-functions"></a>Shell 回呼函數

本節說明 Windows Shell 回呼函數。

## <a name="in-this-section"></a>本節內容



| 主題                                                                     | 描述                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))<br/>                      | 指定應用程式定義的回呼函式，這個函式用來傳送訊息，以及處理來自的訊息，以回應 [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera)的呼叫所顯示的 **流覽** 對話方塊。<br/> |
| [*FMExtensionProc*](fmextensionproc.md)<br/>                       | 指定由檔案管理員呼叫的應用程式定義回呼函式，以與檔案管理員延伸模組進行通訊。<br/>                                                                                            |
| [*MRUCMPPROC*](mrucmpproc.md)<br/>                                 | 用來判斷專案是否存在於最近使用的 (MRU) 清單中。<br/>                                                                                                                                   |
| [**PAPPSTATE \_ 變更 \_ 常式**](/windows/desktop/api/appnotify/nc-appnotify-pappstate_change_routine)<br/> | 指定應用程式定義的回呼函式，此函式會在應用程式進入或離開暫停狀態時通知應用程式。<br/>                                                                                            |
| [**SUBCLASSPROC**](/windows/win32/api/commctrl/nc-commctrl-subclassproc)<br/>                  | 定義 [**RemoveWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) 和 [**SetWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass)所使用之回呼函式的原型。<br/>                                                   |
| [**FM 取消 \_ 刪除 \_ 進程**](undeletefile.md)<br/>                     | 當使用者選擇 [檔案] 功能表中的 [取消 **刪除** ] 命令時，指定 **由 [檔** 管理器] 呼叫的應用程式定義回呼函數。<br/>                                                                   |



 

 

 
