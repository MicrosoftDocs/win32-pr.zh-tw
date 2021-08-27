---
title: 啟用安全性
description: 啟用安全性
ms.assetid: 0c13d473-a9f9-40b5-951b-731eab736fe6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be436997889edd14704d5fa7646db689bba405825c1e8bcf9d021ea850ae70f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048906"
---
# <a name="activation-security"></a>啟用安全性

啟用安全性 (也稱為啟動安全性) 有助於控制可以啟動伺服器的人員。 「服務控制管理員」會自動套用「啟用安全性」 (特定電腦的 SCM) 。 當收到來自用戶端的要求以啟始物件 (如 [實例建立](instance-creation-helper-functions.md) 協助程式函式中所述) ，SCM 會根據儲存在其登錄中的啟用安全性資訊來檢查要求。 也會檢查是否有相同電腦啟用 (啟用安全性。 ) 

判斷用戶端的身分識別時，啟用會檢查用戶端呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)時所設定的遮蓋旗標。 如果 (針對動態或靜態的掩蓋) 設定了遮蓋旗標，則會使用執行緒權杖（如果有的話）來判斷用戶端的身分識別。 如果未設定任何掩蓋，則會使用進程權杖，而不是執行緒 token。

如需啟用安全性的詳細資訊，請參閱 [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) 和 [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 中的安全性](security-in-com.md)
</dt> </dl>

 

 