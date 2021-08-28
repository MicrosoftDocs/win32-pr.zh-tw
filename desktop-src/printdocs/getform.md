---
description: GetForm 函式會捕獲指定表單的相關資訊。
ms.assetid: 10b25748-6d7c-46ab-bd2c-9b6126a1d7d1
title: 'GetForm 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetForm
- GetFormA
- GetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: bf5263d0de24d86053f8293f2fc9f6c410519ddef568cec9f4692223166e6ab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971437"
---
# <a name="getform-function"></a>GetForm 函式

**GetForm** 函式會捕獲指定表單的相關資訊。

## <a name="syntax"></a>語法


```C++
BOOL GetForm(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pFormName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

印表機的控制碼。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

</dd> <dt>

*pFormName* \[在\]
</dt> <dd>

指定表單名稱之以 null 結束的字串指標。 若要取得印表機支援的表單名稱，請呼叫 [**EnumForms**](enumforms.md) 函式。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

*PForm* 所指向的結構版本。 此值必須是1或2。

</dd> <dt>

*pForm* \[擴展\]
</dt> <dd>

位元組陣列的指標，此陣列會接收初始化的 [**表單 \_ 資訊 \_ 1**](form-info-1.md) 或 [**表單 \_ 資訊 \_ 2**](form-info-2.md) 結構。

</dd> <dt>

*cbBuf* \[在\]
</dt> <dd>

*PForm* 陣列的大小（以位元組為單位）。

</dd> <dt>

*pcbNeeded* \[擴展\]
</dt> <dd>

值的指標，指定函式成功時所複製的位元組數目，或如果 *cbBuf* 太小，則為所需的位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

如果呼叫端是遠端的，而且 *層級* 是2，則傳回 [**表單 \_ INFO \_ 2**](form-info-2.md)的 **StringType** 值一律會是字串 \_ LANGPAIR。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **GetFormW** (Unicode) 和 **GetFormA** (ANSI) <br/>                                                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**DeleteForm**](deleteform.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetForm**](setform.md)
</dt> </dl>

 

 




