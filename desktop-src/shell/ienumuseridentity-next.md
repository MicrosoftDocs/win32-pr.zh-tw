---
description: IEnumUserIdentity：： Next 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: 2c8dfe36-c1bb-49f8-8847-f355cfab2984
title: 'IEnumUserIdentity：： Next 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Next
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eb3074a7b55ce03e7372491fce11160f1df1bc5fc8a4e45ad0f12d4538d4b2f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009398"
---
# <a name="ienumuseridentitynext-method"></a>IEnumUserIdentity：： Next 方法

\[**IEnumUserIdentity：： Next** 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]

已取代。 從列舉中抓取使用者識別介面的陣列。

## <a name="syntax"></a>語法


```C++
HRESULT Next(
  [in]  ULONG    celt,
  [out] IUnknown **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*celt* \[在\]
</dt> <dd>

類型： **ULONG**

**ULONG** 值，表示要取出的介面數目。

</dd> <dt>

*rgelt* \[擴展\]
</dt> <dd>

類型： **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

接收介面之指標的位址。

</dd> <dt>

*pceltFetched* \[擴展\]
</dt> <dd>

類型： **ULONG \***

接收成功抓取之介面數目的指標位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

[**IEnumUserIdentity**](ienumuseridentity.md) 會保留內部計數，以指定要取出的介面。 這個方法的多個呼叫不會重設這個計數。 若要重設計數，請呼叫 [**IEnumUserIdentity：： reset**](ienumuseridentity-reset.md)。 若要遞增計數而不需要取出介面，請呼叫 [**IEnumUserIdentity：： Skip**](ienumuseridentity-skip.md)。

*Celt* 的值不應超過 [**IEnumUserIdentity：： GetCount**](ienumuseridentity-getcount.md)傳回的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                   |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                  |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>Msident。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IEnumUserIdentity：： Skip**](ienumuseridentity-skip.md)
</dt> <dt>

[**IEnumUserIdentity：： Reset**](ienumuseridentity-reset.md)
</dt> <dt>

[**IEnumUserIdentity：： GetCount**](ienumuseridentity-getcount.md)
</dt> </dl>

 

 
