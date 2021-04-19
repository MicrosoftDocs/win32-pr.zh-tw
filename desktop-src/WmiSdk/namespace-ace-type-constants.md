---
description: 存取控制專案中的類型欄位 (ACE) ，可判斷 ACE 是否為允許存取或拒絕存取的 ACE。
ms.assetid: a78c72f7-0bc0-4bda-9012-4abe45342d8d
ms.tgt_platform: multiple
title: '命名空間 ACE 類型常數 (Winnt. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Allow
- Deny
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 0c9f1f7e05f663782c0d748ddb296ca36ecbe29c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999384"
---
# <a name="namespace-ace-type-constants"></a>命名空間 ACE 類型常數

存取控制專案中的 **類型** 欄位 (ace) ，可判斷 ace 是否為允許存取或拒絕存取的 ace。

<dl> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**允許**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



ACE 允許存取命名空間。


</dt> </dl> </dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>**否認**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



ACE 會拒絕對命名空間的存取。


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

 

 




