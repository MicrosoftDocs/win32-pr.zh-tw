---
description: 在某些情況下，伺服器應用程式必須在用戶端上代表其存取的資源出示用戶端身分識別，通常是為了對用戶端身分識別執行存取檢查或驗證。
ms.assetid: fd75eb54-eefe-411f-a7aa-0bc8628f8778
title: 用戶端模擬和委派
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b0262f3d8dd6736d183fa76eb5d3f0946d50b2724e76bcea73843644aaefb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129370"
---
# <a name="client-impersonation-and-delegation"></a>用戶端模擬和委派

在某些情況下，伺服器應用程式需要對其代表用戶端存取的資源出示用戶端的身分識別，通常是為了針對用戶端的身分識別來執行存取檢查或驗證。 在特定範圍內，伺服器可以在用戶端的身分識別下採取動作，這是一種稱為模擬用戶端的動作。

模擬是執行緒在安全性內容中執行的 *能力，與* 擁有線程的進程不同。 伺服器執行緒會使用代表用戶端認證的存取權杖，並透過此存取權杖存取用戶端可以存取的資源。

使用模擬可確保伺服器可以精確地達成用戶端的功能。 資源的存取權可能會受到限制或展開，取決於用戶端有許可權進行的作業。

連接到資料庫時，您可以選擇讓伺服器模擬用戶端，讓資料庫可以驗證和授權用戶端。 或者，如果您的應用程式存取以安全描述項保護的檔案，並讓用戶端取得這些檔案中資訊的授權存取，應用程式就可以在存取檔案之前模擬用戶端。

## <a name="how-to-implement-impersonation"></a>如何執行模擬

模擬需要用戶端和伺服器 (的參與，而且在某些情況下，系統管理員) 。 用戶端必須指出其意願讓伺服器使用其身分識別，而伺服器必須以程式設計的方式明確地假設用戶端的身分識別。 如需詳細資訊，請參閱用戶端模擬和伺服器端[需求](server-side-requirements-for-impersonation.md)的[用戶端需求](client-side-requirements-for-impersonation.md)。

## <a name="administrative-requirements-for-delegate-level-impersonation"></a>Delegate-Level 模擬的系統管理需求

若要有效地使用模擬、 *委派*（透過網路模擬用戶端）的最強大形式，必須在 Active Directory 服務中正確設定用戶端和伺服器使用者帳戶，以支援其 (，除了用戶端授與委派層級模擬) 的許可權，如下所示：

-   伺服器身分識別在 Active Directory 服務中必須標示為「受信任的委派」。
-   在 Active Directory 服務中，用戶端身分識別不得標示為「帳戶是機密的，無法委派」。

這些設定功能讓網域系統管理員有更高程度的委派控制權，也就是，假設有多少信任 (，因此涉及安全性風險) 。 如需委派的詳細資訊，請參閱 [委派和](/windows/desktop/com/delegation-and-impersonation)模擬。

## <a name="cloaking"></a>隱形

除了用戶端透過模擬等級授與伺服器的授權單位之外，伺服器的掩蓋功能主要決定模擬的行為。 當伺服器呼叫用戶端（本身或用戶端）發出呼叫時，會影響伺服器實際呈現的身分識別。 如需詳細資訊，請參閱「 [掩蔽](cloaking.md)」。

## <a name="performance-implications"></a>效能影響

模擬可能會大幅影響效能和調整。 通常在呼叫上模擬用戶端比直接進行呼叫更昂貴。 以下是一些要考慮的問題：

-   以複雜模式傳遞身分識別的計算額外負荷，尤其是在啟用動態遮蓋的情況下。
-   在許多地方強制執行重複的安全性檢查（而不是集中在中介層）的一般複雜性。
-   在開啟模擬用戶端時，資料庫連接之類的資源無法跨多個用戶端重複使用—這是很大的障礙，可進行適當的調整。

有時候，唯一有效的解決方法是使用模擬，但應謹慎考慮這項決策。 如需這些問題的進一步討論，請參閱 [多層式應用程式安全性](multi-tier-application-security.md)。

## <a name="queued-components"></a>已排入佇列的元件

已[排入佇列的元件](com--queued-components.md)不支援模擬。 當用戶端呼叫已排入佇列的物件時，實際上會對記錄器進行呼叫，這會將它封裝成訊息的一部分。 然後，接聽程式會從佇列讀取訊息，並將它傳遞給播放程式，叫用實際的伺服器元件，並進行相同的方法呼叫。 因此，當伺服器接收到呼叫時，原始用戶端權杖無法透過模擬來使用。 但是，以角色為基礎的安全性仍然適用，而且使用 [**ISecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) 介面的程式設計安全性也可以運作。 如需詳細資訊，請參閱已 [排入佇列的元件安全性](queued-components-security.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[用戶端驗證](client-authentication.md)
</dt> <dt>

[程式庫應用程式安全性](library-application-security.md)
</dt> <dt>

[多層式應用程式安全性](multi-tier-application-security.md)
</dt> <dt>

[程式設計元件安全性](programmatic-component-security.md)
</dt> <dt>

[以角色為基礎的安全性管理](role-based-security-administration.md)
</dt> <dt>

[在 COM + 中使用軟體限制原則](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
