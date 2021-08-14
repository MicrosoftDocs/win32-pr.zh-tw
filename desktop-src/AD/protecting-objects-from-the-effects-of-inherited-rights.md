---
title: 保護物件不受繼承許可權的影響
description: 如在繼承和委派管理主題中所討論，Ace 可以設定在容器物件上（例如 organizationalUnit、domainDNS、容器等），並根據這些 Ace 上設定的 ACE 旗標傳播到子物件。
ms.assetid: 3da000dd-3a32-4294-a636-ad077e618db2
ms.tgt_platform: multiple
keywords:
- 保護物件不受繼承的許可權 AD 影響
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcc1067fcfe0d57e2e7aca837b97d73f18b55a41a4f1347ac36224b987918aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185013"
---
# <a name="protecting-objects-from-the-effects-of-inherited-rights"></a>保護物件不受繼承許可權的影響

如在 [繼承和委派管理](inheritance-and-delegation-of-administration.md)主題中所討論，ace 可以設定在容器物件上（例如 **organizationalUnit**、 **domainDNS**、 **容器** 等），並根據這些 ace 上設定的 ace 旗標傳播到子物件。

如果您有一個安全物件或您想要明確控制其 Ace 的物件（例如私用 OU 或特殊使用者），則可以防止 Ace 依其父容器或其父容器的前置項傳播至物件。

您可以使用 [**IADsSecurityDescriptor**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) 屬性來控制是否要由物件的父容器繼承 Dacl 和 sacl。

[**IADsSecurityDescriptor 控制項**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods)屬性可以用來保護物件免于繼承的 ace 的影響。 下列旗標會強制在物件上明確設定存取控制，並防止使用者藉由在物件的父容器上設定可繼承的 Ace 或其父容器的前身來修改物件的存取控制。



| 旗標                               | 描述                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SE \_已 \_ 保護 DACL**<br/> | 防止在父容器的 DACL 上設定 Ace，以及目錄階層中父容器上方的任何物件套用至物件 DACL。<br/> |
| **SE \_SACL \_ 受保護**<br/> | 防止將 Ace 設定在父容器的 SACL，以及目錄階層中父容器上方的任何物件，而不會套用到物件 SACL。<br/> |



 

請注意，必須要有 **SE \_ dacl \_ 存在** 旗標，才能將 SE 的 dacl 設定為 **\_ \_ 受保護**，而且必須要有 **SE \_ sacl \_** ，才能設定 **SE 的 \_ sacl \_ 受保護**。

 

