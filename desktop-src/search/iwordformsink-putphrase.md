---
description: 在 IWordFormSink 物件中放置替代的單字形式。
ms.assetid: 4F6A3E88-A17C-4CA3-849D-FF0DC06D5DC3
title: 'IWordFormSink：:P utAltWord 方法 (搜尋 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 874428ed435d2336398f6e72c58b70de275565cce2e606f1fdddea54f0684742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944408"
---
# <a name="iwordformsinkputaltword-method"></a>IWordFormSink：:P utAltWord 方法

在 [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) 物件中放置替代的單字形式。

## <a name="syntax"></a>語法


```C++
HRESULT PutAltWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pwcInBuf* \[在\]
</dt> <dd>

包含單字替代形式的緩衝區指標。

</dd> <dt>

*cwc* \[在\]
</dt> <dd>

*PwcInBuf* 中的字元數。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                              | 描述                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                     | 作業已順利完成。 <br/>                                                                                             |
| <dl> <dt>**語言 \_S \_ 大型 \_ 單字**</dt> </dl> | *Cwc* 的值大於 [**IStemmer：： Init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init)中指定的 *ulMaxTokenSize* 值。 <br/> |



 

## <a name="remarks"></a>備註

這個方法是從 [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer)執行的 [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms)方法呼叫。 單字的所有替代形式（最後一個除外）都會藉由呼叫 **IWordFormSink：:P utaltword** 放置在 [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)物件中。 單字的最後一個替代形式（一律是單字的原始形式）是藉由呼叫 [**IWordFormSink：:P utword**](iwordformsink-putword.md)來處理。

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

 

 
