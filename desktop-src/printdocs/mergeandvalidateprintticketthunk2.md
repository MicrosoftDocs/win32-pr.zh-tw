---
description: 合併兩個列印票證，並傳回有效的可用列印票證。
ms.assetid: 4aa7b9de-abf2-4781-942e-0b992a6bffed
title: MergeAndValidatePrintTicketThunk2 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeAndValidatePrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: 4a21b9e505e39d64e8e0c696a3b8a6432a012d76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971609"
---
# <a name="mergeandvalidateprintticketthunk2-function"></a>MergeAndValidatePrintTicketThunk2 函式

\[這項功能不受支援，而且可能會在未來的 Windows 版本中停用或刪除。 [**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) 會提供對等的功能，因此應該改用。\]

合併兩個列印票證，並傳回有效的可用列印票證。

## <a name="syntax"></a>語法


```C++
HRESULT MergeAndValidatePrintTicketThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pBasePrintTicket,
  _In_      INT         basePrintTicketLength,
  _In_opt_  BYTE        *pDeltaPrintTicket,
  _In_      INT         deltaPrintTicketLength,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppValidatedPrintTicket,
  _Out_     INT         *pValidatedPrintTicketLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hProvider* \[在\]
</dt> <dd>

開啟的列印票證提供者的控制碼。 [**BindPTProviderThunk**](bindptproviderthunk.md)函數會傳回這個控制碼。

</dd> <dt>

*pBasePrintTicket* \[在\]
</dt> <dd>

包含基底列印票證資料的緩衝區，以 XML 表示，如 [列印架構](./printschema.md)中所述。

</dd> <dt>

*basePrintTicketLength* \[在\]
</dt> <dd>

*PBasePrintTicket* 所參考的緩衝區大小（以位元組為單位）。

</dd> <dt>

*pDeltaPrintTicket* \[在中，選擇性\]
</dt> <dd>

包含要合併之列印票證的緩衝區。 列印票證資料是以 XML 表示，如 [列印架構](./printschema.md)中所述。 此參數的值可以是 **Null**。

</dd> <dt>

*deltaPrintTicketLength* \[在\]
</dt> <dd>

*PDeltaPrintTicket* 所參考的緩衝區大小（以位元組為單位）。

</dd> <dt>

*範圍* \[在\]
</dt> <dd>

值，指定 *pDeltaPrintTicket* 和 *ppValidatedPrintTicket* 的範圍是單一頁面、整份檔，還是列印工作中的所有檔。 此參數的值必須是 [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) 列舉的成員（轉換為 **DWORD**）。

</dd> <dt>

*ppValidatedPrintTicket* \[擴展\]
</dt> <dd>

包含已合併和已驗證之列印票證的緩衝區位址。 此函數會呼叫 [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) 來配置這個緩衝區。 當不再需要緩衝區時，呼叫端必須藉由呼叫 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)來釋放它。

</dd> <dt>

*pValidatedPrintTicketLength* \[擴展\]
</dt> <dd>

*PpValidatedPrintTicket* 所參考的緩衝區大小（以位元組為單位）。

</dd> <dt>

*pbstrErrorMessage* \[out、optional\]
</dt> <dd>

字串的指標，指定 *pBasePrintTicket* 或 *pDeltaPrintTicket* 中列印票證的無效內容（如果有的話）。 如果兩者都是有效的，則此值為 **Null**。 當函式傳回時，如果 *pbstrErrorMessage* 不是 **Null** ，則呼叫端必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)釋放字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 **S \_ OK**，否則會傳回 **HRESULT** 錯誤碼。 如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印架構](./printschema.md)
</dt> <dt>

[**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)
</dt> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> </dl>

 

