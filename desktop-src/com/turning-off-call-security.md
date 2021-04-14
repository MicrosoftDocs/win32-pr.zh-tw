---
title: 關閉通話安全性
description: 呼叫安全性可判斷用戶端是否有權呼叫伺服器的方法。 有兩種方式可以停用呼叫安全性，其中一個方法是使用 Dcomcnfg.exe 修改登錄，而另一個則需要呼叫 CoInitializeSecurity。
ms.assetid: 7ce162d0-20e0-4385-ad9f-472f2c17b060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a838a9c7936c126a1fedeeafc977f55641b63c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371963"
---
# <a name="turning-off-call-security"></a>關閉通話安全性

呼叫安全性可判斷用戶端是否有權呼叫伺服器的方法。 有兩種方式可以停用呼叫安全性：其中一個會牽涉到使用 Dcomcnfg.exe 修改登錄，而另一個則需要呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)。

-   [使用 DCOMCNFG 關閉通話安全性](#turning-off-call-security-using-dcomcnfg)
-   [以程式設計方式關閉通話安全性](#turning-off-call-security-programmatically)
-   [相關主題](#related-topics)

## <a name="turning-off-call-security-using-dcomcnfg"></a>使用 DCOMCNFG 關閉通話安全性

使用 Dcomcnfg.exe 修改登錄，可最輕鬆地關閉呼叫安全性。 但是，如果用戶端和伺服器都沒有呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)，使用 Dcomcnfg.exe 關閉安全性將會運作。 這是因為當呼叫 **CoInitializeSecurity** 時，DCOM 會忽略登錄設定，並改用提供給 **CoInitializeSecurity** 的值。

若要關閉 Dcomcnfg.exe 的安全性，用戶端和伺服器都必須將其驗證層級設定為 [無]。 必須完成下列步驟：

1.  執行 Dcomcnfg.exe。
2.  在 [ **應用程式** ] 頁面上，選取代表伺服器的應用程式。 按一下 [ **屬性** ] 按鈕 (或按兩下選取的應用程式) 。
3.  按一下 [General] \(一般\) 索引標籤。
4.  從 [ **預設驗證等級** ] 清單方塊中，選取 [ **無] ()**。
5.  按一下 [ **套用** ] 按鈕以套用變更;不過，變更不會套用至任何執行中的應用程式實例。
6.  如果用戶端出現在 [ *應用程式* ] 頁面上的清單中，請重複步驟2到5，選擇用戶端，而不是步驟2的伺服器。 然後按一下 **[確定]** 按鈕。 如果用戶端不在清單中，您可以執行下列三項作業的其中一項：
    -   您可以使用 Dcomcnfg.exe，在整個電腦上將用戶端的驗證層級設定為 [無]。  (查看警告和下列程式。 ) 
    -   您可以用程式設計的方式將用戶端的驗證層級設定為 [無]。
    -   您可以為用戶端建立 [AppID](appid-key.md) 金鑰，以指出驗證層級為 [無]。  (參閱 [透過登錄設定 Process-Wide 安全性](setting-processwide-security-through-the-registry.md)。 ) 

若要在整個電腦上將驗證等級設定為 [無]：

> [!Note]  
> 將全電腦的驗證層級設定為 [無] 非常不安全。

 

1.  執行 Dcomcnfg.exe。
2.  選擇 [ **預設** 內容] 索引標籤。
3.  從 [ **預設驗證等級** ] 清單方塊中，選擇 [ **無] ()**。
4.  按一下 [確定] 按鈕。

## <a name="turning-off-call-security-programmatically"></a>以程式設計方式關閉通話安全性

若要以程式設計方式關閉呼叫安全性，用戶端和伺服器都必須呼叫 **CoInitializeSecurity**，將 *dwAuthnLevel* 參數中的驗證層級設定為「RPC \_ C \_ 驗證 \_ 層級 \_ 無」。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關閉啟用安全性](turning-off-activation-security.md)
</dt> </dl>

 

 




