---
description: SetMacAddressInBlob 函式會設定 BLOB 的要求 MAC 位址。
ms.assetid: f44d0cec-ced7-4d2a-a58e-aeb476bfe800
title: 'SetMacAddressInBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetMacAddressInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 20ed4a0358bc0aecada66858f9814bce94252ff9d705c971be947ca5af788ab3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364056"
---
# <a name="setmacaddressinblob-function"></a>SetMacAddressInBlob 函式

**SetMacAddressInBlob** 函式會設定 BLOB 的要求 MAC 位址。

## <a name="syntax"></a>語法


```C++
DWORD SetMacAddressInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const BYTE  *pMacAddress
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

*pMacAddress* \[在\]
</dt> <dd>

要設定之 BLOB 的 MAC 位址指標。

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

[GetMacAddressFromBlob](getmacaddressfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[SetClassIDInBlob](setclassidinblob.md)
</dt> <dt>

[SetDwordInBlob](setdwordinblob.md)
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

 

 




