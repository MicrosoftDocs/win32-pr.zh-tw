---
description: GetNPPTriggerFromBlob 函式會從指定的 BLOB 抓取觸發程式。
ms.assetid: 48a27cf3-57b0-4241-a925-4209e0d384e2
title: 'GetNPPTriggerFromBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPTriggerFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e8faa4dd2cbd4d54fa0fb43b371529a4e867c50c9ff7237f2860c83cff911628
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366036"
---
# <a name="getnpptriggerfromblob-function"></a>GetNPPTriggerFromBlob 函式

**GetNPPTriggerFromBlob** 函式會從指定的 BLOB 抓取觸發程式。

## <a name="syntax"></a>語法


```C++
DWORD GetNPPTriggerFromBlob(
  _In_  HBLOB     hBlob,
  _Out_ LPTRIGGER pTrigger,
  _Out_ HBLOB     hErrorBlob
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hBlob* \[在\]
</dt> <dd>

BLOB 的控制碼。

</dd> <dt>

*pTrigger* \[擴展\]
</dt> <dd>

觸發程式值的指標。

</dd> <dt>

*hErrorBlob* \[擴展\]
</dt> <dd>

錯誤 BLOB 的控制碼，指定發生任何) 時，在原始 BLOB 中的錯誤 (。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。

## <a name="remarks"></a>備註

觸發程式資訊會儲存在 BLOB 的 **觸發** 程式類別中。

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

[GetBoolFromBlob](getboolfromblob.md)
</dt> <dt>

[GetClassIDFromBlob](getclassidfromblob.md)
</dt> <dt>

[GetDwordFromBlob](getdwordfromblob.md)
</dt> <dt>

[GetMacAddressFromBlob](getmacaddressfromblob.md)
</dt> <dt>

[GetNetworkInfoFromBlob](getnetworkinfofromblob.md)
</dt> <dt>

[GetNPPAddressFilterFromBlob](getnppaddressfilterfromblob.md)
</dt> <dt>

[GetNPPPatternFilterFromBlob](getnpppatternfilterfromblob.md)
</dt> <dt>

[GetStringFromBlob](getstringfromblob.md)
</dt> <dt>

[GetStringsFromBlob](getstringsfromblob.md)
</dt> </dl>

 

 




