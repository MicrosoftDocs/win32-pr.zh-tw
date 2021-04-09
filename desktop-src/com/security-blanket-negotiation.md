---
title: 安全性的總協商
description: 安全性的總協商
ms.assetid: 5a01912d-611c-4a6e-ab9d-0243cba331f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51407de908eaaf0f79eea452046f8e424ccf900
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024167"
---
# <a name="security-blanket-negotiation"></a>安全性的總協商

安全性一般是一組值，這些值會描述套用至進程中所有 proxy 或只套用至特定介面 proxy 的安全性設定。 安全性的總包含下列值：

-   驗證服務
-   授權服務
-   主要名稱
-   驗證層級
-   模擬等級
-   驗證身分識別
-   功能
-   存取控制清單 (ACL) 僅 (伺服器) 

安全性全面協商是 COM 在建立時，用來選擇 proxy 安全性設定的程式。 此程式牽涉到將伺服器的安全性全面與用戶端的安全性全面進行比較，並使用這些值來建立 proxy 的適當預設安全性。 下列段落說明用戶端和伺服器安全性毛毯的來源，並說明 COM 如何使用用戶端和伺服器的安全性毛毯，為 proxy 協調安全性的綜合。

用戶端和伺服器都可以呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 來指定各自的安全性毛毯。 如果應用程式未明確呼叫 **CoInitializeSecurity** ，COM 會使用適當的預設值，針對應用程式隱含呼叫它。 如需這些預設值的詳細資訊，請參閱 [COM 安全性預設](com-security-defaults.md)值。

當應用程式為伺服器時，會套用 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 的一些參數，而當應用程式是用戶端時，則會套用某些參數。 當應用程式作為伺服器時，這些參數會相關： ACL、驗證服務/授權服務/主體名稱元組的清單，以及驗證層級。 伺服器對 **CoInitializeSecurity** 的呼叫（不論是隱含或明確）都會決定伺服器的安全性全面，也就是固定的。

當應用程式做為用戶端時，會將下列傳遞給 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 的值相關：驗證層級、模擬層級、驗證身分識別和功能。 用戶端對 **CoInitializeSecurity** 的隱含或明確呼叫會指出用戶端想要的安全性階層。

建立 proxy 時，COM 會使用伺服器安全性的總和用戶端安全性的總值，來協商適用于 proxy 的預設安全層。 COM 會挑選可同時在用戶端和伺服器上運作的驗證服務。 系統會選擇授權服務和主體名稱來使用驗證服務。 針對驗證層級，COM 會選擇用戶端和伺服器所指定的驗證層級較高。 模擬等級和 COM 所選擇的功能是用戶端所指定的功能。 驗證身分識別是用戶端為所選驗證服務指定的身分識別。

一旦計算預設安全性的總值，就會將其值指派給新建立的 proxy。 用戶端可以藉由呼叫 [**IClientSecurity：： SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)來覆寫 proxy 的安全性設定。 指定給 **SetBlanket** 的值不會進行協商;它們只會指派給指定的 proxy。 但是，如果 (預設參數，例如 RPC \_ C \_ IMP \_ 層級 \_ 預設) 會傳遞給 **SetBlanket**，則 COM 會使用先前所述的安全性整體協商演算法來計算預設參數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 中的安全性](security-in-com.md)
</dt> </dl>

 

 