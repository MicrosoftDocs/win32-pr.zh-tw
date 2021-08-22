---
description: 視安裝程式傳遞給處理常式的訊息類型參數中提供的按鈕類型而定， (UI) 處理常式的外部使用者介面可以傳回任意數目的值給 Windows Installer。
ms.assetid: a918082d-709d-4b4f-ae3b-5f16ed0ca910
title: 從外部消費者介面處理常式傳回值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b4ba5edcd87b0d4f324762f840c117425b322ea03d1dd15e103c05bcf12352
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626078"
---
# <a name="returning-values-from-an-external-user-interface-handler"></a>從外部消費者介面處理常式傳回值

視安裝程式傳遞給處理常式的訊息類型參數中提供的按鈕類型而定， (UI) 處理常式的外部使用者介面可以傳回任意數目的值給 Windows Installer。

外部 UI 處理常式可以在任何時間都傳回值–1和0，因為這些值與按鈕類型無關。 傳回值-1 表示外部 UI 處理常式發生內部錯誤。 傳回值0表示外部 UI 處理常式尚未處理安裝程式訊息，而且安裝程式必須改為處理訊息。

對於不包含按鈕類型的訊息（例如 INSTALLMESSAGE \_ ACTIONDATA 和 INSTALLMESSAGE \_ 進度），傳回 IDCANCEL 會取消安裝。 傳回 IDOK 會通知安裝程式，訊息是由外部 UI 處理常式所處理。

其餘的傳回值（如下所述）與訊息類型所包含的按鈕類型直接相關。



| 外部 UI 傳回值 | 意義                                                                                                |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| IDOK                     | 使用者已按下 [ **確定]** 按鈕。 已瞭解訊息資訊。                     |
| IDCANCEL                 | 已按下 [ **取消** ] 按鈕。 取消安裝。                                            |
| IDABORT                  | 已按下 [ **中止** ] 按鈕。 中止安裝。                                              |
| IDRETRY                  | 已按下 [ **重試** ] 按鈕。 請重試此動作。                                                |
| IDIGNORE                 | 已按下 [ **忽略** ] 按鈕。 忽略錯誤並繼續。                                      |
| IDYES                    | 已按下 [ **是]** 按鈕。 肯定回應，繼續目前的事件順序。   |
| IDNO                     | 未按下 [ **否** ] 按鈕。 負值回應不會繼續目前的事件順序。 |



 

例如，如果外部 UI 處理常式傳送了具有 MB \_ ABORTRETRYIGNORE 訊息方塊樣式旗標的訊息，則外部 ui 處理常式可能會傳回下列其中一個值：

-   – 1 (外部 UI 處理常式的錯誤) 
-   0 (不會在外部 UI 處理常式中採取任何動作，讓 Windows Installer 處理它) 
-   已按下 IDABORT (**中止** 按鈕) 
-   已按下 IDRETRY (**重試** 按鈕) 
-   IDIGNORE (**略** 過已按下的按鈕) 

 

 



