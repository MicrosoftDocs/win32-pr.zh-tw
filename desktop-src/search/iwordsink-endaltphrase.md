---
description: 以斷詞工具在索引時間產生的替代片語順序表示最後一個片語的結尾。
ms.assetid: 50E4E208-A290-42B7-9152-9472C01B20D5
title: 'IWordSink：： EndAltPhrase 方法 (搜尋 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.EndAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 4056357de5e3e479124e8f9a91d9b3d906300709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191192"
---
# <a name="iwordsinkendaltphrase-method"></a>IWordSink：： EndAltPhrase 方法

以斷詞工具在索引時間產生的替代片語順序表示最後一個片語的結尾。

## <a name="syntax"></a>語法


```C++
HRESULT EndAltPhrase();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                           | Description                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**\_ \_ 僅限 WBREAK E 查詢 \_**</dt> </dl> | 查詢期間會呼叫 [**EndAltPhrase**](iwordsink-endaltphrase.md) 。<br/> |



 

## <a name="remarks"></a>備註

[**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker)執行會從 [**IWordBreaker：： BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)方法呼叫 **IWordSink：： EndAltPhrase** ，以終止一系列的替代片語。 呼叫 [**IWordSink：： StartAltPhrase**](iwordsink-startaltphrase.md) 方法，以表示一個片語的結尾和另一個句子順序的開頭。 只有序列中的最後一個片語會透過呼叫 **EndAltPhrase** 來終止。

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

 

 
