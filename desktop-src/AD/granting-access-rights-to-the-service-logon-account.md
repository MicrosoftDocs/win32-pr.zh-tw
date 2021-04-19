---
title: 將存取權限授與服務登入帳戶
description: 安裝服務實例的主要考慮是確保已安裝的服務可以存取所需的資源。
ms.assetid: 5b756318-f621-4fce-af2b-71ccccbb4e3c
ms.tgt_platform: multiple
keywords:
- 將存取權限授與服務登入帳戶 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f4ea5b85e6158109338b881eeb3f59d74a3910
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "106965229"
---
# <a name="granting-access-rights-to-the-service-logon-account"></a>將存取權限授與服務登入帳戶

安裝服務實例的主要考慮是確保已安裝的服務可以存取所需的資源。 若要這樣做，請在服務必須存取之物件的安全描述項中設定 Ace。 ACE 可以授與或拒絕指定安全性主體的存取權限，例如服務使用者帳戶，或 LocalSystem 服務的電腦帳戶，或是服務帳戶所屬的群組。 如需 Ace、安全描述項和存取控制的詳細資訊，請參閱 [控制存取 Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) 和 [存取控制](/windows/desktop/SecAuthZ/access-control)中的物件。

如需可用來設定可讓服務修改其服務連接點之 ACE 的詳細資訊和程式碼範例，請參閱 [啟用服務帳戶以存取 SCP 屬性](enabling-service-account-to-access-scp-properties.md)。

在某些情況下，您必須將您的服務使用者帳戶新增為一或多個安全性群組的成員。 例如，如果您為您的服務建立系統管理員群組，您可能會將服務設為群組的成員。 然後，您可以將存取權限授與群組，而不是明確地授與服務帳戶。 如需安全性群組的詳細資訊，請參閱 [管理群組](managing-groups.md)。

 

 