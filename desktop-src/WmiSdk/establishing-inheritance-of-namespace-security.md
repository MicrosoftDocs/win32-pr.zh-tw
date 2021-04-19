---
description: 您可以控制子命名空間是否繼承父命名空間的安全描述項。
ms.assetid: d4fbd5af-69e2-4c60-907a-cb2a1506b7c9
ms.tgt_platform: multiple
title: 建立命名空間安全性的繼承
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e242299b78ede3ff49679305a97823bc022358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990426"
---
# <a name="establishing-inheritance-of-namespace-security"></a>建立命名空間安全性的繼承

您可以控制子命名空間是否繼承父命名空間的安全描述項。

WMI 命名空間具有安全描述項，可控制誰可以存取命名空間和命名空間的資料。 每個安全描述項都有 (DACL) 的任意存取控制清單，以及 (SACL) 的安全性存取控制清單。 這些清單包含 (ACE) 的存取控制專案。

根據設定的 [**命名空間 ACE 旗標常數**](namespace-ace-flag-constants.md) ，該命名空間的所有子命名空間可能會繼承套用至命名空間的許可權。 如果 **容器 \_ 繼承 \_ ACE** 旗標是在父命名空間安全描述項中，則在建立子命名空間時，子命名空間會繼承其父命名空間的安全描述項。 如果 **CONTAINER \_ INHERIT \_ ace \| 未設定 \_ 無限傳播 \_ INHERIT \_ ace** ，則只有子命名空間會繼承安全描述項，而非孫命名空間。 子命名空間可以藉由呼叫 [**\_ \_ SystemSecurity**](--systemsecurity.md)類別的方法來寫入新的安全描述項，藉以覆寫其父系的安全性許可權。 無法變更預設安全性設定。 如需詳細資訊，請參閱 [設定命名空間安全描述項](setting-namespace-security-descriptors.md)。如需 Dacl 的詳細資訊，請參閱 (ACL) 和 [**命名空間 ACE 類型常數**](namespace-ace-type-constants.md)的 [存取控制清單](/windows/desktop/SecAuthZ/access-control-lists)。

請注意，預設許可權無法變更。 此外，設定安全描述項 (SD) 時，設定「 **SE \_ DACL \_ 保護** 」旗標並不會用來將特製化 SD 新增至子命名空間。 若要覆寫繼承的 SD，請只設定一個新的 SD。 若要將該 SD 繼承至子命名空間，請在命名空間安全描述項中傳遞 **容器 \_ inherit \_ ACE** 旗標。 若要只繼承子系，而不是子代，請傳遞 `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`

.

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定命名空間安全描述項](setting-namespace-security-descriptors.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 
