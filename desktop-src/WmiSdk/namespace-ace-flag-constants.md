---
description: 下列清單列出 WMI 存取控制專案中 [旗標] 欄位的可能值 (ACE) 。
ms.assetid: bd09691d-e285-40e0-8686-edd5a132a06e
ms.tgt_platform: multiple
title: '命名空間 ACE 旗標常數 (Winnt. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OBJECT_INHERIT_ACE
- CONTAINER_INHERIT_ACE
- NO_PROPAGATE_INHERIT_ACE
- INHERIT_ONLY_ACE
- INHERITED_ACE
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 053d4166882b6254dec313cb10fbf10588ba0071
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987910"
---
# <a name="namespace-ace-flag-constants"></a>命名空間 ACE 旗標常數

下列清單列出 WMI 存取控制專案中 [ **旗標** ] 欄位的可能值 (ACE) 。

<dl> <dt>

<span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**OBJECT \_ INHERIT \_ ACE**
</dt> <dd> <dl> <dt>

1 (0x1) 
</dt> <dt>



非容器子物件會將 ACE 繼承為有效的 ACE。


</dt> </dl> </dd> <dt>

<span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**容器 \_ 繼承 \_ ACE**
</dt> <dd> <dl> <dt>

2 (0x2) 
</dt> <dt>



ACE 會影響子命名空間以及目前的命名空間。


</dt> </dl> </dd> <dt>

<span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**沒有 \_ 傳播 \_ 繼承 \_ ACE**
</dt> <dd> <dl> <dt>

4 (0x4) 
</dt> <dt>



ACE 僅適用于目前的命名空間和立即的子系。


</dt> </dl> </dd> <dt>

<span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**\_只繼承 \_ ACE**
</dt> <dd> <dl> <dt>

8 (0x8) 
</dt> <dt>



ACE 僅適用于子命名空間。


</dt> </dl> </dd> <dt>

<span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**繼承的 \_ ACE**
</dt> <dd> <dl> <dt>

16 (0x10) 
</dt> <dt>



用戶端不會設定這項設定，但當 ACE 的來源是父命名空間時，就會向用戶端回報。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Winnt。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WMI 安全性常數](wmi-security-constants.md)
</dt> <dt>

[設定命名空間安全描述項](setting-namespace-security-descriptors.md)
</dt> <dt>

[建立命名空間安全性的繼承](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 




