---
title: 混合式環境的系結問題
description: 混合式環境的系結問題
ms.assetid: d9f9a6bc-7733-4269-99c8-61a84b37d487
ms.tgt_platform: multiple
keywords:
- ADSI ADSI，使用，混合式環境的系結問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65135e0562f387ee9b70e2395d807b639a48e37
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106966269"
---
# <a name="binding-issues-for-mixed-environments"></a>混合式環境的系結問題

針對包含 Active Directory 網域與 Windows NT 4.0 網域具有信任關係的環境，使用無伺服器系結來系結至 Active Directory 物件時可能會發生問題。

在某些網路環境中，為了允許網域之間的驗證，在包含 Active Directory 和 Windows NT 4.0 伺服器的網域控制站之間已設定信任關係。 在這些混合的環境中，如果使用者是 Windows NT 4.0 的成員，網域會嘗試使用無伺服器系結來系結至受信任網域上的 Active Directory 物件，然後系結將會失敗，並傳回錯誤。 這是因為無伺服器系結會使用 [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) 函數系結至 Active Directory 中的物件，而此物件相依于適當的 DNS。

在此案例中，Windows NT 使用者必須提供要系結之特定網域的名稱。 以下是一個範例。

``` syntax
LDAP://fabrikam.com/OU=Sales
```

 

 