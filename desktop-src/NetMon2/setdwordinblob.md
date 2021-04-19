---
description: SetDwordInBlob 函式會設定 BLOB 的已命名 DWORD 值。
ms.assetid: 9174cd5c-4442-4fbe-8dc7-f8a74e1cc85d
title: 'SetDwordInBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDwordInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9bca0efe61824c6fb8dd41b0b241791b6303799d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985636"
---
# <a name="setdwordinblob-function"></a>SetDwordInBlob 函式

**SetDwordInBlob** 函式會設定 BLOB 的已命名 **DWORD** 值。

## <a name="syntax"></a>語法


```C++
DWORD SetDwordInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       DWORD Dword
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hBlob* \[在\]
</dt> <dd>

要設定之 BLOB 的控制碼。

</dd> <dt>

*pOwnerName* \[在\]
</dt> <dd>

要設定之 BLOB **擁有** 者名稱的指標。

</dd> <dt>

*pCategoryName* \[在\]
</dt> <dd>

要設定之 BLOB **類別目錄** 名稱的指標。

</dd> <dt>

*pTagName* \[在\]
</dt> <dd>

要設定之 BLOB **標記** 名稱的指標。

</dd> <dt>

*Dword* \[在\]
</dt> <dd>

要設定之 BLOB 的 **DWORD** 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Npptools .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[GetDwordFromBlob](getdwordfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[SetClassIDInBlob](setclassidinblob.md)
</dt> <dt>

[SetMacAddressInBlob](setmacaddressinblob.md)
</dt> <dt>

[SetNetworkInfoInBlob](setnetworkinfoinblob.md)
</dt> <dt>

[SetNPPAddressFilterInBlob](setnppaddressfilterinblob.md)
</dt> <dt>

[SetNPPPatternFilterInBlob](setnpppatternfilterinblob.md)
</dt> <dt>

[SetNPPTriggerInBlob](setnpptriggerinblob.md)
</dt> <dt>

[SetStringInBlob](setstringinblob.md)
</dt> </dl>

 

 




