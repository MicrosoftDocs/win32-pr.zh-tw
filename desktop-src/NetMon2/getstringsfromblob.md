---
description: 使用連續呼叫來取得指定範圍內的所有字串。
ms.assetid: 4e819975-84a5-4b73-9a19-792d3607da9c
title: 'GetStringsFromBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringsFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 25fbc149a663ef68d1588218937568401f414ef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936615"
---
# <a name="getstringsfromblob-function"></a>GetStringsFromBlob 函式

**GetStringsFromBlob** 函式會使用連續呼叫來取得指定範圍內的所有字串。

## <a name="syntax"></a>語法


```C++
DWORD GetStringsFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pRequestedOwnerName,
  _In_  const char  *pRequestedCategoryName,
  _In_  const char  *pRequestedTagName,
  _Out_ const char  **ppReturnedOwnerName,
  _Out_ const char  **ppReturnedCategoryName,
  _Out_ const char  **ppReturnedTagName,
  _Out_ const char  **ppReturnedString,
  _Out_       DWORD *pRestartKey
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hBlob* \[在\]
</dt> <dd>

BLOB 的控制碼。

</dd> <dt>

*pRequestedOwnerName* \[在\]
</dt> <dd>

要從中取得字串的擁有者區段指標。

</dd> <dt>

*pRequestedCategoryName* \[在\]
</dt> <dd>

要從中取得字串的類別目錄區段指標。

</dd> <dt>

*pRequestedTagName* \[在\]
</dt> <dd>

要求之字串的標記指標。

</dd> <dt>

*ppReturnedOwnerName* \[擴展\]
</dt> <dd>

指向將傳回 **擁有** 者名稱之變數的指標。

</dd> <dt>

*ppReturnedCategoryName* \[擴展\]
</dt> <dd>

指向將傳回 **分類** 名稱之變數的指標。

</dd> <dt>

*ppReturnedTagName* \[擴展\]
</dt> <dd>

指向變數的指標，指向將傳回 **標記** 名稱的位置。

</dd> <dt>

*ppReturnedString* \[擴展\]
</dt> <dd>

指向將傳回字串名稱之變數的指標。

</dd> <dt>

*pRestartKey* \[擴展\]
</dt> <dd>

變數的指標，其中將會指定並傳回重新啟動金鑰。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值會是指出問題的 NMERR 值。

如果 **擁有** 者、 **類別** 和 **標記** 資訊的指定組合不存在，則傳回值為 **NMERR \_ BLOB 專案不 \_ \_ \_ \_ 存在**。

當 BLOB 完全在一開始指定的界限內進行時，此函 **式 \_ 會傳回 NMERR BLOB 專案不 \_ \_ \_ \_ 存在**，而且 *pRestartKey* 參數會指向零。

## <a name="remarks"></a>備註

在 **GetStringsFromBlob** 函數的初始呼叫上， *pRestartKey* 參數會指向包含零值的變數。 只有當重新啟動金鑰為零時，才能使用 *pRequested* 參數。 在後續的呼叫中，當 *pRestartKey* 有非零值時，會忽略 *pRequested* 參數。 在初始呼叫上，所有專案都可能指向 **Null**，這會設定查詢來傳回 BLOB 中的每個專案，每個後續呼叫一個專案。

指定擁有者會將傳回的字串限制為只有該擁有者。 類別和標籤也有類似的限制，另外請注意，如果指定了類別，也必須指定擁有者，如果指定了標籤，則類別 (，因此必須指定擁有者) 。

當初次呼叫 **GetStringsFromBlob** 時， *pRestartKey* 會指向新的值，此值應在下一次呼叫函式時指定以取得下一個值。

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

[SetStringInBlob](setstringinblob.md)
</dt> <dt>

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

[GetNPPTriggerFromBlob](getnpptriggerfromblob.md)
</dt> <dt>

[GetStringFromBlob](getstringfromblob.md)
</dt> </dl>

 

 




