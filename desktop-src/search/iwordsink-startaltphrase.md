---
description: 表示在索引時間于斷詞工具產生的替代片語序列中，片語之間的界限。
ms.assetid: 3F3B6761-887B-426E-A44F-E636397180C7
title: 'IWordSink：： StartAltPhrase 方法 (搜尋 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.StartAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: e4e35c5ed75016292dd420e7a832c6cfb780284a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191191"
---
# <a name="iwordsinkstartaltphrase-method"></a>IWordSink：： StartAltPhrase 方法

表示在索引時間于斷詞工具產生的替代片語序列中，片語之間的界限。

## <a name="syntax"></a>語法


```C++
HRESULT StartAltPhrase();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                           | Description                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ \_ 僅限 WBREAK E 查詢 \_**</dt> </dl> | 查詢期間會呼叫 [**StartAltPhrase**](iwordsink-startaltphrase.md) 。<br/> |



 

## <a name="remarks"></a>備註

每個替代片語的開頭都是 **StartAltPhrase** 呼叫。 此片語會透過後續的 IWordSink 呼叫來放置在 [**IWordSink**](iwordsink.md) 物件中 [**：:P utword**](iwordsink-putword.md) 或 [**IWordSink：:P utaltword**](iwordsink-putaltword.md) 方法。 [**IWordSink：： EndAltPhrase**](iwordsink-endaltphrase.md)方法的呼叫會終止一系列片語中的最後一個替代片語。

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

 

 




