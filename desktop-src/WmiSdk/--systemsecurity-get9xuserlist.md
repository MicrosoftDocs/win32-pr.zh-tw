---
description: 針對執行過時 Windows 的電腦上的個別使用者清單取得遠端存取許可權，但無法使用透過 Windows 安全描述項的存取控制。
ms.assetid: 79a596db-5f85-4664-8989-f309286eca0d
ms.tgt_platform: multiple
title: __SystemSecurity：： Get9XUserList 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Get9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: 521f2fe489089d486480c138293ebea39ca6f105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975827"
---
# <a name="__systemsecurityget9xuserlist-method"></a>\_\_SystemSecurity：： Get9XUserList 方法

[**\_ \_ SystemSecurity：： Set9XUserList**](--systemsecurity-set9xuserlist.md)方法會針對執行過時 windows 的電腦上的個別使用者清單取得遠端存取許可權，但無法使用透過 windows 安全描述項的存取控制。

這項功能類似于安全描述項，但更受限制。 群組不受支援，而且無法控制本機存取，因為本機使用者一律具有完整存取權。 拒絕和允許存取控制專案 (ACE) ，因此 ACE 順序在 (DACL) 的任意存取控制清單中很重要。 如需詳細資訊，請參閱 [DACL 中的 Ace 順序](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)。

## <a name="syntax"></a>語法


```C++
HRESULT Get9XUserList(
  [out] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ul* \[擴展\]
</dt> <dd>

使用者的陣列。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **HRESULT** ，指出方法呼叫的狀態。 下列清單列出對 **Get9XUserList** 而言很重要的傳回值。 針對腳本和 Visual Basic 的應用程式，結果可以是 [OutParameters. ReturnValue](parsing-outparameters-objects.md)。 如需詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。

<dl> <dt>

**\_ \_ \_ 已停用 WBEM E 方法**
</dt> <dd>

支援的 Windows 版本不支援這個方法。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[**\_\_SystemSecurity::GetSD**](--systemsecurity-getsd.md)
</dt> <dt>

[**\_\_SystemSecurity::SetSD**](--systemsecurity-setsd.md)
</dt> <dt>

[**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[保護 WMI 命名空間](securing-wmi-namespaces.md)
</dt> <dt>

[WMI 安全性常數](wmi-security-constants.md)
</dt> </dl>

 

