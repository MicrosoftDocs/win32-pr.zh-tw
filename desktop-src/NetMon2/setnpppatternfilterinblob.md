---
description: 設定 BLOB 模式符合篩選。
ms.assetid: 44e7c67a-f430-4d68-bc7f-f6bbd5b9e5a9
title: 'SetNPPPatternFilterInBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPPatternFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a920d6ffc135855826719e31613119a27671e334d5a75ce7dba29c2b140816fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363749"
---
# <a name="setnpppatternfilterinblob-function"></a>SetNPPPatternFilterInBlob 函式

**SetNPPPatternFilterInBlob** 函數會設定 BLOB 模式比對篩選。

## <a name="syntax"></a>語法


```C++
DWORD SetNPPPatternFilterInBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hBlob* \[在\]
</dt> <dd>

BLOB 的控制碼。

</dd> <dt>

*pExpression* \[在\]
</dt> <dd>

[運算式](expression.md)結構的指標，此結構會定義要設定的篩選運算式。

</dd> <dt>

*hErrorBlob* \[擴展\]
</dt> <dd>

錯誤 BLOB 的控制碼，指定當發生任何) 時，原始 BLOB 中的錯誤 (。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 **SetNPPPatternFilterInBlob** 函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。

## <a name="remarks"></a>備註

模式會比對儲存在 BLOB 之 **Config** 分類中的篩選資料。

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

[GetNPPAddressFilterFromBlob](getnppaddressfilterfromblob.md)
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

[SetNPPTriggerInBlob](setnpptriggerinblob.md)
</dt> <dt>

[SetStringInBlob](setstringinblob.md)
</dt> </dl>

 

 




