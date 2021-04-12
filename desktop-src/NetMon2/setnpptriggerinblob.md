---
description: 設定 BLOB 觸發程式。
ms.assetid: 88bfd5cd-f563-4d0c-81a3-54a846805b87
title: 'SetNPPTriggerInBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPTriggerInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 05b8bb3f7f95dc3246ef10f3945b9ab0868550cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191487"
---
# <a name="setnpptriggerinblob-function"></a>SetNPPTriggerInBlob 函式

**SetNPPTriggerInBlob** 函式會設定 BLOB 觸發程式。

## <a name="syntax"></a>語法


```C++
DWORD SetNPPTriggerInBlob(
  _In_  HBLOB     hBlob,
  _In_  LPTRIGGER pTrigger,
  _Out_ HBLOB     hErrorBlob
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hBlob* \[在\]
</dt> <dd>

BLOB 的控制碼。

</dd> <dt>

*pTrigger* \[在\]
</dt> <dd>

觸發程式值的指標。

</dd> <dt>

*hErrorBlob* \[擴展\]
</dt> <dd>

錯誤 BLOB 的控制碼，指定當發生任何) 時，原始 BLOB 中的錯誤 (。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。

## <a name="remarks"></a>備註

此觸發程式資料會儲存在 BLOB 的 **觸發** 程式類別中。

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

[GetNPPTriggerFromBlob](getnpptriggerfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[SetClassIDInBlob](setclassidinblob.md)
</dt> <dt>

[SetDwordInBlob](setdwordinblob.md)
</dt> <dt>

[SetMacAddressInBlob](setmacaddressinblob.md)
</dt> <dt>

[SetNetworkInfoInBlob](setnetworkinfoinblob.md)
</dt> <dt>

[SetNPPAddressFilterInBlob](setnppaddressfilterinblob.md)
</dt> <dt>

[SetNPPPatternFilterInBlob](setnpppatternfilterinblob.md)
</dt> <dt>

[SetStringInBlob](setstringinblob.md)
</dt> </dl>

 

 




