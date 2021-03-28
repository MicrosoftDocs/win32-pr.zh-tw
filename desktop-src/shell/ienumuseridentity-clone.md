---
description: IEnumUserIdentity：： Clone 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用使用者帳戶搭配快速切換使用者與遠端桌面。
ms.assetid: dde9afca-db8d-41ba-afa0-94eadecb695b
title: 'IEnumUserIdentity：： Clone 方法 (Msident .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Clone
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: ebdec426fe7ab591c801c00b637211e903cf5356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991530"
---
# <a name="ienumuseridentityclone-method"></a>IEnumUserIdentity：： Clone 方法

\[**IEnumUserIdentity：： Clone** 不受支援，而且可能會在未來變更或無法使用。 相反地，請使用 [使用者帳戶搭配快速切換使用者與遠端桌面](fastuserswitching.md)。\]

取得目前列舉的複本。

## <a name="syntax"></a>語法


```C++
HRESULT Clone(
  [out] IEnumUserIdentity **ppenum
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppenum* \[擴展\]
</dt> <dd>

類型： **[ **IEnumUserIdentity**](ienumuseridentity.md)\*\***

接收此列舉複本之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

[**IEnumUserIdentity**](ienumuseridentity.md) 會保留內部計數，以指定要取出的介面。 此計數的值將會套用至 *ppenum* 所接收的介面。 若要重設計數，請呼叫 [**IEnumUserIdentity：： reset**](ienumuseridentity-reset.md)。

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
</dt> </dl>

 

 




