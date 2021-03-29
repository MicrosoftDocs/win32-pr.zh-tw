---
description: IEnumUserIdentity：： Skip 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: bb19ae50-b384-48fb-9272-15e3e3eaa9d0
title: 'IEnumUserIdentity：： Skip 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Skip
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: cedd4f3c6e9736e26cbf8d58f27f805f0f5d33a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991523"
---
# <a name="ienumuseridentityskip-method"></a>IEnumUserIdentity：： Skip 方法

\[**IEnumUserIdentity：： Skip** 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]

在列舉中略過指定數目的使用者識別介面。 在抓取介面時使用。

## <a name="syntax"></a>語法


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*celt* \[在\]
</dt> <dd>

類型： **ULONG**

要略過的介面數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

[**IEnumUserIdentity**](ienumuseridentity.md) 會保留內部計數，以指定要取出的介面。 若要遞增此計數而不需要抓取介面，請呼叫這個方法。 若要重設計數，請呼叫 [**IEnumUserIdentity：： reset**](ienumuseridentity-reset.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                   |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                  |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>Msident。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IEnumUserIdentity：： Reset**](ienumuseridentity-reset.md)
</dt> <dt>

[**IEnumUserIdentity：： Next**](ienumuseridentity-next.md)
</dt> <dt>

[**IEnumUserIdentity：： GetCount**](ienumuseridentity-getcount.md)
</dt> </dl>

 

 




