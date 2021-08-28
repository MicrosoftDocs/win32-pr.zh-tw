---
description: 指出 \_ \_ 終止處理常式的 try 區塊是否正常終止。 函數只能從 \_ \_ 終止處理常式的 finally 區塊內呼叫。
ms.assetid: 0ddaef1f-03f0-45fc-9c5e-8d6a26a73245
title: AbnormalTermination 宏
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AbnormalTermination
api_type:
- NA
api_location: ''
ms.openlocfilehash: 137d6667c993d4a107be057e46c4ee469a513ec95d358b6d3cc50654a5bba520
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957127"
---
# <a name="abnormaltermination-macro"></a>AbnormalTermination 宏

指出終止處理常式的 **\_ \_ try** 區塊是否正常終止。 函數只能從終止處理常式的 **\_ \_ finally** 區塊內呼叫。

> [!Note]  
> Microsoft C/c + + 優化編譯器會將此函式解釋為關鍵字，而在適當的例外狀況處理語法外部使用會產生編譯器錯誤。

 

## <a name="syntax"></a>語法


```C++
BOOL AbnormalTermination(void);
```



## <a name="parameters"></a>參數

這個宏沒有任何參數。

## <a name="return-value"></a>傳回值

如果 **\_ \_ try** 區塊異常終止，則傳回值為非零值。

如果 **\_ \_ try** 區塊正常終止，則傳回值為零。

## <a name="remarks"></a>備註

只有在執行區塊中的最後一個語句之後，才會將 **\_ \_ try** 區塊依序結束。 語句 (例如 **return**、 **goto**、 **continue** 或 **break**) 導致執行離開 **\_ \_ try** 區塊會導致區塊異常終止。 即使這類的語句是 **\_ \_ try** 區塊中的最後一個語句，還是會發生這種情況。

**\_ \_ Try** 區塊的異常終止會導致系統向後搜尋所有堆疊框架，以判斷是否必須呼叫任何終止處理常式。 這可能會導致執行數百個指令，因此請務必避免因 **return**、 **goto**、 **continue** 或 **break** 語句而導致 **\_ \_ try** 區塊的異常終止。 請注意，即使終止不正常，這些語句也不會產生例外狀況。

為了避免異常終止，執行應會繼續到區塊結尾。 您也可以執行 **\_ \_ leave** 語句。 **\_ \_ Leave** 語句允許立即終止 **\_ \_ try** 區塊，而不會造成異常終止和其效能負面影響。 請檢查您的編譯器檔，以判斷是否支援 **\_ \_ leave** 語句。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[結構化例外狀況處理函式](structured-exception-handling-functions.md)
</dt> <dt>

[結構化例外狀況處理總覽](structured-exception-handling.md)
</dt> </dl>

 

 




