---
description: 通知函數
ms.assetid: 44f69e05-1f08-48da-abb7-7e0a96c0cd26
title: 通知函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84e5ca0bbcd9f2f184abd312fe15d4923e5cf14b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115217"
---
# <a name="notification-functions"></a>通知函數



| 一般函數                                                                  | 包裝函式方法                            | 備註                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdiplusNotificationHook (OUT ULONG \_ PTR \* token) <br/> | 未由包裝函式方法呼叫。<br/> | [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup)函式會在其 output 參數中傳回 (，) [**GdiplusStartupOutput**](/windows/desktop/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput)結構的指標。 結構的其中一個成員是通知攔截函式的指標，該函式與 GdiplusNotificationHook 具有相同的簽章。<br/> 您可以透過兩種方式呼叫通知攔截函式;您可以使用 [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) 所傳回的指標，也可以呼叫 GdiplusNotificationHook。 事實上，GdiplusNotificationHook 只會確認您已隱藏背景執行緒，然後呼叫 **GdiplusStartup** 所傳回的通知攔截函式。<br/> Token 參數接收的識別碼，您稍後應該將該識別碼傳遞給通知解除傳送函式的對應呼叫。<br/>                                                                                                                                         |
| VOID WINGDIPAPI GdiplusNotificationUnhook (ULONG \_ PTR token) <br/>         | 未由包裝函式方法呼叫。<br/> | [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup)函式會在其 output 參數中傳回 (，) [**GdiplusStartupOutput**](/windows/desktop/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupoutput)結構的指標。 結構的其中一個成員是通知解除連結函式的指標，該函式具有與 GdiplusNotificationUnhook 相同的簽章。<br/> 您可以透過兩種方式呼叫通知解除解除的函式;您可以使用 [**GdiplusStartup**](/windows/desktop/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) 所傳回的指標，也可以呼叫 GdiplusNotificationUnhook。 事實上，GdiplusNotificationUnhook 只會確認您已隱藏背景執行緒，然後呼叫 **GdiplusStartup** 所傳回的通知解除的函式。<br/> 當您呼叫通知解除傳送函式時，請將您先前從對應呼叫所收到的權杖傳遞給通知攔截函式。 如果您沒有這麼做，則會在進程結束之前，不會清除資源流失。<br/> |



 

 

 




