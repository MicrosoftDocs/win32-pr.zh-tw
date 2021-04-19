---
description: AddForm 函式會將表單新增至可針對指定印表機選取的可用表單清單。
ms.assetid: 17b59019-f93a-4b57-86fb-91c61aecbac4
title: 'AddForm 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddForm
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2de3ddbdc57a5a41bac048a94a8175cd124df4ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980830"
---
# <a name="addform-function"></a>AddForm 函式

**AddForm** 函式會將表單新增至可針對指定印表機選取的可用表單清單。

## <a name="syntax"></a>語法


```C++
BOOL AddForm(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pForm
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

印表機的控制碼，可支援以指定的表單進行列印。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

*PForm* 所指向之結構的層級。 此值必須是1或2。

</dd> <dt>

*pForm* \[在\]
</dt> <dd>

[**表單 \_ 資訊 \_ 1**](form-info-1.md)或 [**表單 \_ 資訊 \_ 2**](form-info-2.md)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

應用程式可以藉由呼叫 [**EnumForms**](enumforms.md) 函式來判斷可供印表機使用的表單。

如果 *pForm* 指向 [**表單 \_ 資訊 \_ 2**](form-info-2.md)，而具有指定名稱的表單已經存在，或結構的 *pKeyword* 值已經存在，則 **AddForm** 將會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumForms**](enumforms.md)
</dt> <dt>

[**表單 \_ 資訊 \_ 1**](form-info-1.md)
</dt> <dt>

[**表單 \_ 資訊 \_ 2**](form-info-2.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




