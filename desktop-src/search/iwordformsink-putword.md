---
description: 將原始單字形式放在 IWordFormSink 物件中。
ms.assetid: 333A3109-6C0A-42AE-9E10-87F53C7F737C
title: 'IWordFormSink：:P utWord 方法 (搜尋 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 438cb41e50f264bd373ae2ef8e84598b651b0352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985401"
---
# <a name="iwordformsinkputword-method"></a>IWordFormSink：:P utWord 方法

將原始單字形式放在 [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) 物件中。

## <a name="syntax"></a>語法


```C++
HRESULT PutWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pwcInBuf* \[在\]
</dt> <dd>

緩衝區的指標，其中包含單字的最終替代形式，一律為原始單字。

</dd> <dt>

*cwc* \[在\]
</dt> <dd>

*PwcInBuf* 中的字元數。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                          | Description                                           |
|--------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 作業已順利完成。 <br/> |



 

## <a name="remarks"></a>備註

**PutWord** 是從 [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer)執行的 [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms)方法中呼叫。 這個方法會處理單字的原始形式，最後會呼叫。 所有上述的單字替代形式都會藉由呼叫 [**IWordFormSink：:P utaltword**](iwordformsink-putphrase.md)來放置於 [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)物件中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>搜尋。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
