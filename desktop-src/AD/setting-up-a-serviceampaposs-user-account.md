---
title: 設定服務的使用者帳戶
description: 您的服務安裝程式可以針對服務實例建議預設登入帳戶，並允許系統管理員選取預設帳戶或指定不同的帳戶。
ms.assetid: 37285c23-8922-4da5-9f0b-922ea5e5794e
ms.tgt_platform: multiple
keywords:
- 設定服務的使用者帳戶 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f310ee97c68ded8c4086694302feccb5991d726e01f9addbeced21cc5b9acfdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183275"
---
# <a name="setting-up-a-services-user-account"></a>設定服務的使用者帳戶

您的服務安裝程式可以針對服務實例建議預設登入帳戶，並允許系統管理員選取預設帳戶或指定不同的帳戶。 如果系統管理員選取使用者帳戶，而不是 LocalSystem 帳戶，則在呼叫 [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) 函式之前，帳戶必須存在，才能在主機伺服器上安裝服務的實例。 如需可在 Active Directory Domain Services 中用來建立新網域使用者物件的詳細資訊和程式碼範例，請參閱 [建立使用者](creating-a-user.md)。

在理想情況下，服務的每個實例（不論是主機型或可複寫服務）都應該有自己的網域使用者帳戶。 針對每個服務實例使用不同的帳戶，比讓多個實例共用相同的帳戶更安全。 此外，使用不同的帳戶，可以讓您審核每個服務實例的活動。

當您的安裝程式建議使用預設登入帳戶時，應該為新的服務實例指定要建立之新帳戶的名稱。 帳戶名稱可能是由用來撰寫服務主體名稱的相同元素所組成，例如服務類別、主機電腦和服務名稱。 如需詳細資訊，請參閱[服務主體名稱](service-principal-names.md)。 一般而言，您會在主機電腦網域的 [使用者] 容器中建立帳戶。

您必須為每個帳戶產生密碼。 如需有關如何撰寫可自動化更新服務帳戶密碼之工作的詳細資訊，請參閱 [變更服務之使用者帳戶的密碼](changing-the-password-on-a-serviceampaposs-user-account.md)。

 

 