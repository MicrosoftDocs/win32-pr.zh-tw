---
description: 將 DEVMODE 結構轉換為列印票證。
ms.assetid: c03371f8-a978-4fb7-82cc-f76a65f3904c
title: ConvertDevModeToPrintTicketThunk2 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertDevModeToPrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: d5aea99e54a43eb35f76c719da885f8d7ae0352d47ecff62b7df38de30410025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950388"
---
# <a name="convertdevmodetoprintticketthunk2-function"></a>ConvertDevModeToPrintTicketThunk2 函式

\[這項功能不受支援，而且可能會在未來的 Windows 版本中停用或刪除。 [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) 會提供對等的功能，因此應該改用。\]

將 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構轉換為列印票證。

## <a name="syntax"></a>語法


```C++
HRESULT ConvertDevModeToPrintTicketThunk2(
  _In_  HPTPROVIDER hProvider,
  _In_  BYTE        *pDevmode,
  _In_  ULONG       cbSize,
  _In_  DWORD       scope,
  _Out_ BYTE        **ppPrintTicket,
  _Out_ INT         *pcbPrintTicketLength
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hProvider* \[在\]
</dt> <dd>

開啟的列印票證提供者的控制碼。 [**BindPTProviderThunk**](bindptproviderthunk.md)函數會傳回這個控制碼。

</dd> <dt>

*pDevmode* \[在\]
</dt> <dd>

要轉換的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 指標。

</dd> <dt>

*cbSize* \[在\]
</dt> <dd>

傳入 *pDevmode* 的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)大小（以位元組為單位）。

</dd> <dt>

*範圍* \[在\]
</dt> <dd>

值，這個值會指定 *ppPrintTicket* 的範圍。 這個值可以指定單一頁面、整份檔，或列印工作中的所有檔。 此參數的值必須是 [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) 列舉的成員（轉換為 **DWORD**）。

</dd> <dt>

*ppPrintTicket* \[擴展\]
</dt> <dd>

包含列印票證的緩衝區位址，代表在 *pDevmode* 中傳遞的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 。 此函數會呼叫 [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) 來配置這個緩衝區。 當不再需要緩衝區時，呼叫端必須藉由呼叫 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)來釋放它。

</dd> <dt>

*pcbPrintTicketLength* \[擴展\]
</dt> <dd>

*PpPrintTicket* 中傳回之列印票證的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 **S \_ OK**，否則會傳回 **HRESULT** 錯誤碼。 如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印架構](./printschema.md)
</dt> <dt>

[**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)
</dt> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> </dl>

 

