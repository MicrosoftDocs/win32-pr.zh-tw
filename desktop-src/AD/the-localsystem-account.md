---
title: 使用 LocalSystem 帳戶做為服務登入帳戶
description: 以 LocalSystem 帳戶執行的其中一項優點是，服務對本機資源的存取權完全不受限制。
ms.assetid: 2bc2e16d-bd25-4ec6-91a2-8d03052df021
ms.tgt_platform: multiple
keywords:
- localsystem 帳戶
- localsystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bec3826984e28e29d3156b784da229f8e53e34e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931873"
---
# <a name="using-the-localsystem-account-as-a-service-logon-account"></a>使用 LocalSystem 帳戶做為服務登入帳戶

以 LocalSystem 帳戶執行的其中一項優點是，服務對本機資源的存取權完全不受限制。 這也是 LocalSystem 的缺點，因為 LocalSystem 服務可以採取一些動作來關閉整個系統。 尤其是在網域控制站 () DC 上以 LocalSystem 身分執行的服務，可不受限制地存取 Active Directory Domain Services。 這表示服務中的錯誤或服務的安全性攻擊可能會損毀系統，或者，如果服務是在 DC 上，則會損毀整個商業網路。

基於這些理由，在機密安裝上的網域系統管理員將會注意到允許服務以 LocalSystem 身分執行。 事實上，它們可能會對它有原則，特別是在 Dc 上。 如果您的服務必須以 LocalSystem 的身分執行，則您服務的檔應該向網域系統管理員證明，這是授與服務許可權以提高許可權執行的原因。 服務絕對不應該在網域控制站上以 LocalSystem 的身分執行。 如需詳細資訊和示範服務或服務安裝程式如何判斷它是否正在網域控制站上執行的程式碼範例，請參閱 [測試是否正在網域控制站上執行](testing-whether-running-on-a-domain-controller.md)。

當服務在屬於網域成員的電腦上以 LocalSystem 帳戶執行時，服務會將任何網路存取權授與電腦帳戶，或電腦帳戶所屬的任何群組。 請注意，在 Windows 2000 中，網域電腦帳戶是與使用者帳戶類似的服務主體。 這表示電腦帳戶可以位於安全性群組中，而安全描述項中的 ACE 可以授與電腦帳戶的存取權。 請注意，不建議將電腦帳戶新增至群組，原因有兩個：

-   如果電腦離開然後重新加入網域，電腦帳戶可能會被刪除並重新建立。
-   如果您將電腦帳戶新增至群組，則在該電腦上以 LocalSystem 身分執行的所有服務都會被允許該群組的存取權限。 這是因為所有 LocalSystem 服務都會共用其主機伺服器的電腦帳戶。 基於這個理由，電腦帳戶不能成為任何網域系統管理員群組的成員，這點特別重要。

電腦帳戶通常有少數許可權，而且不屬於群組。 Active Directory Domain Services 中的預設 ACL 保護允許對電腦帳戶進行最基本的存取。 因此，在 Dc 以外的電腦上，以 LocalSystem 身分執行的服務只有 Active Directory Domain Services 的存取權。

如果您的服務是在 LocalSystem 下執行，您必須在成員伺服器上測試您的服務，以確保您的服務具有足夠的許可權可讀取/寫入 Active Directory 網網域控制站。 網域控制站不應該是您用來測試服務的唯一 Windows 電腦。 請注意，在 Windows 網域控制站上以 LocalSystem 身分執行的服務具有 Active Directory Domain Services 的完整存取權，而成員伺服器則是在擁有較少許可權的電腦帳戶內容中執行。

 

 




