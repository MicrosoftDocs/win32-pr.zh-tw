---
description: SetForm 函式會設定指定印表機的表單資訊。
ms.assetid: 05d5d495-952c-4a1d-8694-1004d0c2bcf6
title: 'SetForm 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetForm
- SetFormA
- SetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 93848afa0f36032bb972f8f4a7c6c3d5eb8c42ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319088"
---
# <a name="setform-function"></a>SetForm 函式

**SetForm** 函式會設定指定印表機的表單資訊。

## <a name="syntax"></a>語法


```C++
BOOL SetForm(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pFormName,
  _In_ DWORD  Level,
  _In_ LPTSTR pForm
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

已設定表單資訊之印表機的控制碼。 使用 [**OpenPrinter**](openprinter.md) 或 [**interactivesession.addprinter**](addprinter.md) 函式來取出印表機控制碼。

</dd> <dt>

*pFormName* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定設定表單資訊的表單名稱。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

*PForm* 所指向的結構版本。 此值必須是1或2。

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

 

您可以針對現有的 [**表單 \_ 資訊 \_ 2**](form-info-2.md)多次呼叫 **SetForm** ，每個呼叫都會新增額外的 **pDisplayName** 和 **wLangId** 值配對。 所有語言版本的表單都將在最近的 **SetForm** 呼叫中取得 **表單 \_ INFO \_ 2** 的 **大小** 與 **ImageableArea** 值。

如果呼叫端是遠端的，而且 *層級* 是2，則 [**表單 \_ 資訊 \_ 2**](form-info-2.md)的 **StringType** 值不能是字串 \_ MUIDLL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **SetFormW** (Unicode) 和 **SetFormA** (ANSI) <br/>                                                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**表單 \_ 資訊 \_ 1**](form-info-1.md)
</dt> <dt>

[**表單 \_ 資訊 \_ 2**](form-info-2.md)
</dt> </dl>

 

 




