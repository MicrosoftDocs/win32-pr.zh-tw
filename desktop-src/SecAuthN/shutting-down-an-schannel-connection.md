---
description: 關閉 Schannel 連接
ms.assetid: 7081ba1f-df3c-41b4-96da-24d44e74d714
title: 關閉 Schannel 連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb700c8ac896d0e64b82b25371ea67cc343d8297c95445ca4126c5718d8024a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918057"
---
# <a name="shutting-down-an-schannel-connection"></a>關閉 Schannel 連接

當用戶端或伺服器完成連線時，必須將其關閉。 另一方則必須辨識關機並刪除連接。

**關閉 Schannel 連接**

1.  呼叫 [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) 函式，並指定 SCHANNEL \_ SHUTDOWN 控制項標記。
2.  從 ApplyControlToken 收到 SEC \_ E \_ OK 傳回值之後 [](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken)，請)  (用戶端上呼叫 [**InitializeSecurityCoNtext (schannel**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) ，) 或 [**AcceptSecurityCoNtext (schannel**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext))  (伺服器) 函式，傳入空的緩衝區。
3.  繼續進行，直到函式傳回每秒的 \_ \_ 內容 \_ 過期，或秒 \_ E \_ 確定連接已關閉。
4.  將最終輸出資訊（如果有的話）傳送給遠端方。
5.  呼叫 [**DeleteSecurityCoNtext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) 以釋放連接所保留的資源。

## <a name="recognizing-a-shutdown"></a>辨識關機

[**DecryptMessage (Schannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage)函式會傳回 \_ \_ \_ 當訊息寄件者關閉連線時，我內容已過期的秒數。 收到此傳回值之後，請依照本主題稍早所述的程式來關閉 Schannel 連接。

 

 
