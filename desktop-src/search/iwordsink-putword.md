---
description: 在 IWordSink 物件中放置單字和其位置。
ms.assetid: 3D645BF6-895E-46E2-92A3-3E301CD228D8
title: 'IWordSink：:P utWord 方法 (搜尋 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: e860aafbef633e226933281aaaa0be5c6429387542e7c3ae2d65d3026fd7fe37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597598"
---
# <a name="iwordsinkputword-method"></a>IWordSink：:P utWord 方法

在 [**IWordSink**](iwordsink.md) 物件中放置單字和其位置。

## <a name="syntax"></a>語法


```C++
HRESULT PutWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cwc* \[在\]
</dt> <dd>

*PwcInBuf* 中的字元數。

</dd> <dt>

*pwcInBuf* \[在\]
</dt> <dd>

緩衝區的指標，此緩衝區包含來源文字的替代文字形式。 **PutWord** 不會修改這個參數。 您可以視需要從 [**IWordBreaker：： BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)傳遞 *pTextSource* 參數。

</dd> <dt>

*cwcSrcLen* \[在\]
</dt> <dd>

來源文字緩衝區中的字元數 (由 *pTextSource* 參數指定為 [**IWordBreaker：： BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) 對應至 *pwcInBuf* 中包含的單字。

</dd> <dt>

*cwcSrcPos* \[在\]
</dt> <dd>

來源文字緩衝區中 *pwcInBuf* 文字的開始位置， (由 *pTextSource* 參數指定為 [**IWordBreaker：： BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                              | 描述                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                     | 作業已順利完成。 也指出沒有其他文字可用來重填緩衝區。<br/>                                  |
| <dl> <dt>**語言 \_S \_ 大型 \_ 單字**</dt> </dl> | *Cwc* 的值大於 [**IWordBreaker：： Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init)中指定的 *ulMaxTokenSize* 值。 <br/> |



 

## <a name="remarks"></a>備註

我們建議 **IWordSink：:P utword** 方法一律包含在 *pTextSource* 中找到的原始文字。 單字的替代形式會使用 [**IWordSink：:P utaltword**](iwordsink-putaltword.md)傳遞至 WordSink。 我們也建議 *pwcInBuf* 中的單字盡可能符合來源文字。 例如，盡可能保留大小寫和重音。

您必須對每個從 *pTextSource* 抓取的單字進行此呼叫，但已建立 [**IWordSink：:P utaltword**](iwordsink-putaltword.md) 呼叫的單字除外。 當單字儲存至 WordSink 時，會以 EOW 字元終止。

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

 

 
