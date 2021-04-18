---
description: 將中斷點放在前面的單字後面。
ms.assetid: C8622067-D8CE-4099-8B9F-941720F4706B
title: 'IWordSink：:P utBreak 方法 (搜尋 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutBreak
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: c6407f1307b4860960c5202af13de736c7921139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318148"
---
# <a name="iwordsinkputbreak-method"></a>IWordSink：:P utBreak 方法

將中斷點放在前面的單字後面。

## <a name="syntax"></a>語法


```C++
HRESULT PutBreak(
  [in] WORDREP_BREAK_TYPE breakType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*breakType* \[在\]
</dt> <dd>

[**WORDREP \_ 中斷 \_ 型**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85))別中的值，這個值表示 WordSink 在上一個字後面插入的中斷類型。 每個 break 都會佔用索引中的唯一位置。 因此，在單字之間插入中斷會變更單字之間的相對距離。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                          | Description                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 作業已順利完成。<br/> |



 

## <a name="remarks"></a>備註

[**IWordSinkPutWord**](iwordsink-putword.md)和 [**IWordSink：:P utaltword**](iwordsink-putaltword.md)方法會自動插入單字結尾 (EOW，以 \_ WORDREP break \_ [**\_ \_ 型**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85))別列舉型別在每個單字之後) 的 EOW break WORDREP 元素表示。 呼叫 **PutBreak** 方法，以插入除了單字結尾以外的分隔型別。 這個方法不會變更來源文字緩衝區 (*pSourceText*) 或遞增 (*cwc*) 的字元計數。 但是，它會遞增索引中的目前位置，並影響查詢結果。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>搜尋。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWordSink**](iwordsink.md)
</dt> </dl>

 

 
