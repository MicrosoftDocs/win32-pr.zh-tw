---
description: 將列印票證轉換成 DEVMODE 結構。
ms.assetid: 3b0a6afd-fa9d-434e-a95f-b051296d4567
title: ConvertPrintTicketToDevModeThunk2 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertPrintTicketToDevModeThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: e6325ca61d18d571a3a3b346b18f6191b53e43d2ce96799c34a643477123f20c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112678"
---
# <a name="convertprinttickettodevmodethunk2-function"></a>ConvertPrintTicketToDevModeThunk2 函式

\[這項功能不受支援，而且可能會在未來的 Windows 版本中停用或刪除。 [**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) 會提供對等的功能，因此應該改用。\]

將列印票證轉換成 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 結構。

## <a name="syntax"></a>語法


```C++
HRESULT ConvertPrintTicketToDevModeThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      ULONG       cbSize,
  _In_      INT         baseType,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppDevmode,
  _Out_     ULONG       *pcbDevModeLength,
  _Out_opt_ BSTR        *errMsg
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hProvider* \[在\]
</dt> <dd>

開啟的列印票證提供者的控制碼。 [**BindPTProviderThunk**](bindptproviderthunk.md)函數會傳回這個控制碼。

</dd> <dt>

*pPrintTicket* \[在\]
</dt> <dd>

包含要轉換之列印票證的緩衝區。

</dd> <dt>

*cbSize* \[在\]
</dt> <dd>

傳入 *pPrintTicket* 的緩衝區大小（以位元組為單位）。

</dd> <dt>

*baseType* \[在\]
</dt> <dd>

值，指出當 *pPrintTicket* 未指定 **DEVMODE** 的每個可能設定時，是否使用使用者的預設 [**devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)或列印佇列的預設 **devmode** 來提供值給輸出 **DEVMODE** 。 此參數的值必須是 [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) 列舉的成員，並轉換為 **INT**。

</dd> <dt>

*範圍* \[在\]
</dt> <dd>

值，這個值會指定 *pPrintTicket* 的範圍。 這個值可以指定單一頁面、整份檔，或列印工作中的所有檔。 此參數的值必須是 [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) 列舉的成員（轉換為 **DWORD**）。

</dd> <dt>

*ppDevmode* \[擴展\]
</dt> <dd>

新建立之 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)的位址。 此函數會呼叫 [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) 來配置這個緩衝區。 當不再需要緩衝區時，呼叫端必須藉由呼叫 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)來釋放它。

</dd> <dt>

*pcbDevModeLength* \[擴展\]
</dt> <dd>

*PpDevmode* 中傳回的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)大小（以位元組為單位）。

</dd> <dt>

*errMsg* \[out、optional\]
</dt> <dd>

字串的指標，指定 *pPrintTicket* 中列印票證不正確內容（如果有的話）。 如果有效，則為 **Null**。 當函式傳回時，如果 *errMsg* 不是 **Null** ，則呼叫端必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)釋放字串。

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

[**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)
</dt> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> </dl>

 

