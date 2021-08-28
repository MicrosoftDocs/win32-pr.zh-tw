---
description: 設定離線登錄區中已開啟登錄機碼的安全性。
ms.assetid: 002866bb-1532-41ad-a4db-a32d6e1c0a6a
title: 'ORSetKeySecurity 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 933bc37e8bc4a79191d781fa5981e8633939757482d6156a7a08f7da6a36cff2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758428"
---
# <a name="orsetkeysecurity-function"></a>ORSetKeySecurity 函式

設定離線登錄區中已開啟登錄機碼的安全性。

## <a name="syntax"></a>語法


```C++
DWORD ORSetKeySecurity(
  _In_ ORHKEY               Handle,
  _In_ SECURITY_INFORMATION SecurityInformation,
  _In_ PSECURITY_DESCRIPTOR pSecurityDescriptor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*控制碼* \[在\]
</dt> <dd>

離線登錄 hive 中開啟登錄機碼的控制碼。

</dd> <dt>

*SecurityInformation* \[在\]
</dt> <dd>

位旗標，表示要設定的安全性資訊類型。 這個參數可以是 [安全性 \_ 資訊](../secauthz/security-information.md) 位旗標的組合。

</dd> <dt>

*pSecurityDescriptor* \[在\]
</dt> <dd>

[安全 \_ 描述項](/windows/win32/api/winnt/ns-winnt-security_descriptor)結構的指標，指定要為指定的索引鍵設定的安全性屬性。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，函數會傳回錯誤 \_ SUCCESS。

如果函式失敗，則會傳回 Winerror.h 中定義的非零錯誤碼。 您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|---------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows離線登錄庫1.0 版或更新版本<br/>                      |
| 標頭<br/>          | <dl> <dt>Offreg。h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORGetKeySecurity**](orgetkeysecurity.md)
</dt> <dt>

[安全 \_ 描述項](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[安全性 \_ 資訊](../secauthz/security-information.md)
</dt> </dl>

 

 
