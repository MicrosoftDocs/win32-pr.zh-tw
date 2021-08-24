---
title: 'UtilAssembleStringsWithAlloc 函式 (Ndattributils) '
description: 配置字串並使用字串資料表所提供的字串將它格式化。 此函數會使用 StringCchPrintf 來建立格式化的字串。
ms.assetid: eedc2874-b949-4cc2-ba7c-ebf1924f1156
keywords:
- UtilAssembleStringsWithAlloc 函式 NDF
topic_type:
- apiref
api_name:
- UtilAssembleStringsWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38473f45e2bd4c53b964bb38ec285cdf3eea091a96d72684c1d801b949f4d0a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801728"
---
# <a name="utilassemblestringswithalloc-function"></a>UtilAssembleStringsWithAlloc 函式

**UtilAssembleStringsWithAlloc** 函式會配置字串，並使用字串資料表所提供的字串將它格式化。 此函數會使用 [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) 來建立格式化的字串。

## <a name="syntax"></a>語法


```C++
HRESULT UtilAssembleStringsWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR InputFormat,
  _In_  LPCWSTR InputString,
  _In_  BOOLEAN AdditionalArgument,
  _In_  ULONG   AdditionalValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*緩衝區* \[擴展\]
</dt> <dd>

類型： **LPWSTR \***

將放置新配置之字串的位置。 當不再需要字串時，必須使用 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)來釋放。

</dd> <dt>

*BufferMax* \[在\]
</dt> <dd>

類型： **UINT**

*緩衝區* 所配置的字串中允許的最大字元數。 如果產生的格式化字串長度超過指定的字元數，則會被截斷並以 null 結束。

> [!Note]  
> 此參數不可以設定為零。

 

</dd> <dt>

*InputFormat* \[在\]
</dt> <dd>

類型： **LPCWSTR**

字串資料表中的字串資源，代表傳遞給 [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)的格式參數。 它是使用 [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)所建立。

資源字串格式必須指定採用寬字元串的格式參數，或採用不帶正負號的 long 和寬字元串格式參數。

</dd> <dt>

*InputString* \[在\]
</dt> <dd>

類型： **LPCWSTR**

字串資料表中的字串資源，代表傳遞給 [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa) 的引數，用於取代格式參數中的寬字元串。 它是使用 [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)所建立。

</dd> <dt>

*AdditionalArgument* \[在\]
</dt> <dd>

類型： **布林值**

如果應將 *AdditionalValue* 作為第一個格式化引數傳遞至 [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)，則為 True;否則 (為 false，而且只會將 *InputString* 所識別的資源字串傳遞) 。

</dd> <dt>

*AdditionalValue* \[在\]
</dt> <dd>

類型： **ULONG**

當 *AdditionalArgument* 為 true 時，要做為第一個格式化引數傳遞至 [**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

可能的傳回值包括（但不限於）下列各項。



| 傳回碼                                                                                  | 描述                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 作業成功。<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 未正確提供一或多個參數。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>Ndattributils。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**UtilStringCopyWithAlloc**](utilstringcopywithalloc.md)
</dt> <dt>

[**UtilLoadStringWithAlloc**](utilloadstringwithalloc.md)
</dt> <dt>

[**StringCchPrintf**](/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa)
</dt> <dt>

[**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

