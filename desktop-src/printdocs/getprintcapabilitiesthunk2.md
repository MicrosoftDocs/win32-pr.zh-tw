---
description: 抓取格式符合 XML 列印架構的印表機功能。
ms.assetid: 15219c19-b64c-4c51-9357-15a797557693
title: GetPrintCapabilitiesThunk2 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintCapabilitiesThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: 55127d15eae41380fd5376ca54589488e255a740a7881042f54bc203873701f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971387"
---
# <a name="getprintcapabilitiesthunk2-function"></a>GetPrintCapabilitiesThunk2 函式

\[這項功能不受支援，而且可能會在未來的 Windows 版本中停用或刪除。 [**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) 會提供對等的功能，因此應該改用。\]

抓取格式符合 XML [列印架構](./printschema.md)的印表機功能。

## <a name="syntax"></a>語法


```C++
HRESULT GetPrintCapabilitiesThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      INT         cbPrintTicket,
  _Out_     BYTE        **ppbPrintCapabilities,
  _Out_     INT         *pcbPrintCapabilitiesLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
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

包含列印票證資料的緩衝區，如 [列印架構](./printschema.md)中所述，以 XML 表示。

</dd> <dt>

*cbPrintTicket* \[在\]
</dt> <dd>

*PPrintTicket* 所參考的緩衝區大小（以位元組為單位）。

</dd> <dt>

*ppbPrintCapabilities* \[擴展\]
</dt> <dd>

這個函式所配置並包含有效列印功能資訊（編碼為 XML）的緩衝區位址。 此函數會呼叫 [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) 來配置這個緩衝區。 當不再需要緩衝區時，呼叫端必須藉由呼叫 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)來釋放它。

</dd> <dt>

*pcbPrintCapabilitiesLength* \[擴展\]
</dt> <dd>

*PpbPrintCapabilities* 所參考的緩衝區大小（以位元組為單位）。

</dd> <dt>

*pbstrErrorMessage* \[out、optional\]
</dt> <dd>

字串的指標，這個字串會指定 *pPrintTicket* 不正確內容（如果有的話）。 如果有效，則此值為 **Null**。 當函式傳回時，如果 *pbstrErrorMessage* 不是 **Null** ，則呼叫端必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)釋放字串。

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

[**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)
</dt> <dt>

[列印架構](./printschema.md)
</dt> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> </dl>

 

