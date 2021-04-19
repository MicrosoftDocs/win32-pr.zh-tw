---
description: 抓取保護離線登錄區中指定之開啟登錄機碼的安全描述項複本。
ms.assetid: 676d5be5-d9d8-48c6-848a-917d1a0474c6
title: 'ORGetKeySecurity 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 13594493af2e7992471d13dce30f0a848501c4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991140"
---
# <a name="orgetkeysecurity-function"></a>ORGetKeySecurity 函式

抓取保護離線登錄區中指定之開啟登錄機碼的安全描述項複本。

## <a name="syntax"></a>語法


```C++
DWORD ORGetKeySecurity(
  _In_      ORHKEY               Handle,
  _In_      SECURITY_INFORMATION SecurityInformation,
  _Out_opt_ PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Inout_   PDWORD               lpcbSecurityDescriptor
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

表示所要求之安全性資訊的 [安全性 \_ 資訊](../secauthz/security-information.md) 值。

</dd> <dt>

*pSecurityDescriptor* \[out、optional\]
</dt> <dd>

緩衝區的指標，此緩衝區會接收所要求之安全描述項的複本。 此參數可以是 **Null**。

</dd> <dt>

*lpcbSecurityDescriptor* \[in、out\]
</dt> <dd>

變數的指標，這個變數會指定 *pSecurityDescriptor* 參數所指向之緩衝區的大小（以位元組為單位）。 當函式傳回時，變數會包含寫入至緩衝區的位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，函數會傳回錯誤 \_ SUCCESS。

如果函式失敗，則會傳回 Winerror.h 中定義的非零錯誤碼。 您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。

如果 *pSecurityDescriptor* 參數所指定的緩衝區太小，則函式會傳回錯誤 \_ 的 \_ 緩衝區，而 *lpcbSecurityDescriptor* 參數會包含要求的安全描述項所需的位元組數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|---------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Offline Registry library 1.0 版或更新版本<br/>                      |
| 標頭<br/>          | <dl> <dt>Offreg。h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORSetKeySecurity**](orsetkeysecurity.md)
</dt> <dt>

[安全性 \_ 資訊](../secauthz/security-information.md)
</dt> </dl>

 

 
