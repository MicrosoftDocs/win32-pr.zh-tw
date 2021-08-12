---
title: RoFailFastWithErrorCoNtextInternal2 函式
description: 在目前的進程中引發不可持續性例外狀況，也可讓您包含作業系統尚未捕捉的其他錯誤內容。
ms.localizationpriority: low
ms.topic: reference
ms.date: 03/13/2020
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ComBase.dll
api_name:
- RoFailFastWithErrorContextInternal2
targetos: Windows
ms.openlocfilehash: a2e8e2e357b7c4768596ca36cb48cdf1bb2cfdbd839ecc6949a607975d6000c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560624"
---
# <a name="rofailfastwitherrorcontextinternal2-function"></a>RoFailFastWithErrorCoNtextInternal2 函式

在目前的進程中引發不可持續性例外狀況，也可讓您包含作業系統 (OS) 尚未捕捉的其他錯誤內容。

## <a name="syntax"></a>語法

```cpp
void WINAPI RoFailFastWithErrorContextInternal2(
  HRESULT hrError,
  ULONG cStowedExceptions,
  _In_reads_opt_(cStowedExceptions) PSTOWED_EXCEPTION_INFORMATION_V2 aStowedExceptionPointers[]
);
```

## <a name="parameters"></a>參數

`hrError`

類型： **[HRESULT](../../com/structure-of-com-error-codes.md)**

與目前錯誤相關聯的 **HRESULT** 。 *HrError* 的任何值都會引發例外狀況。

`cStowedExceptions`

類型： **[ULONG](../../winprog/windows-data-types.md)**

*AStowedExceptionPointers* 陣列中的元素數目。

`aStowedExceptionPointers`

類型： **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**

[**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md)結構的指標陣列。 每個結構都包含描述 stowed 例外狀況的資訊。 然後，這些結構中的資訊會提交給 Windows 錯誤報告 (WER) 以及平臺所捕捉的 stowed 例外狀況資訊。

## <a name="return-value"></a>傳回值

此函數不會傳回值。

## <a name="remarks"></a>備註

**RoFailFastWithErrorCoNtextInternal2** 不會與匯入程式庫和標頭檔相關聯。 您可以先使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) 函式 (載入 `ComBase.dll`) ，然後呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函式來取出 **RoFailFastWithErrorCoNtextInternal2** 的位址，藉此呼叫該函數。

如需詳細資訊，請參閱 [RoFailFastWithErrorCoNtext 函數](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext)。

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **目標平台** | Windows |
| **標頭** | N/A |
| **程式庫** | N/A |
| **DLL** | ComBase.dll |

## <a name="see-also"></a>另請參閱

* [RoFailFastWithErrorCoNtext 函式](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext)