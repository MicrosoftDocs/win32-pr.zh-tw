---
title: 建立新群組
description: Joe Worden，企業系統管理員必須建立新的群組。
ms.assetid: a1bea695-d43f-47e6-af74-ba5abb0116a2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a4f46d595aa892ac75aa67d14bbc0356122271
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933619"
---
# <a name="creating-a-new-group"></a>建立新群組

Joe Worden，企業系統管理員必須建立新的群組。 他想要根據此群組的成員資格來保護某些資源，例如檔案、Active Directory 物件或其他物件。 下列程式碼範例顯示如何建立新的群組。


```VB
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")
Set grp = ou.Create("group", "CN=Management")
grp.Put "samAccountName", "mgmt"
grp.Put "groupType", ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP Or ADS_GROUP_TYPE_SECURITY_ENABLED
grp.SetInfo
```



此群組管理將會在銷售組織單位中建立。 首先，Joe 必須建立 Sales 組織單位的 ADSI 物件。 其次，他必須在這個物件上設定 [**samAccountName**](/windows/desktop/AD/group-objects) 屬性，因為它是回溯相容性的必要屬性。 在此範例中，當已設定 **samAccountName** 時，Windows NT 4.0 工具（例如使用者管理員）會將 **屬性視為管理** 而非 **管理**。

第三，Joe 必須指定群組的類型。 在 Windows 2000 網域中，有三種類型的群組：全域、網域本機和通用。 此外，群組也會攜帶其安全性特性。 群組可以是啟用安全性或不安全的群組。 基本上，啟用安全性的群組就是可授與或拒絕資源存取權的群組，類似于使用者。 例如，將檔案共用的存取權授與群組，即表示該群組的所有成員都可以存取檔案共用。 通訊群組清單無法以類似的方式使用，例如，您無法授與通訊群組清單存取檔案共用的許可權。 升級期間，會將 Windows NT 4.0 群組遷移為啟用安全性的群組。 Active Directory 中的不安全群組與 Exchange 中的通訊群組清單類似。 因此，建立群組或通訊群組清單與 Windows 2000 中的作業類似。 在 Windows 2000 原生模式 (原生模式中，表示網域中的所有網域控制站都是執行 Windows 2000 Server) 的電腦，這些群組可以嵌套到任何層級。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列舉物件](enumerating-objects.md)
</dt> </dl>

 

 