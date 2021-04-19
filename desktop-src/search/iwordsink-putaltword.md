---
description: 在 IWordSink 物件中放置替代單字和其位置。
ms.assetid: 5C8A9B30-F9B5-42E9-ADAC-A11230F0C2FA
title: 'IWordSink：:P utAltWord 方法 (搜尋 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 21fd9eb9ac5a1bf0f52d6574595dc495432d7ec9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971179"
---
# <a name="iwordsinkputaltword-method"></a>IWordSink：:P utAltWord 方法

在 [**IWordSink**](iwordsink.md) 物件中放置替代單字和其位置。

## <a name="syntax"></a>語法


```C++
HRESULT PutAltWord(
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

緩衝區的指標，此緩衝區包含來源文字的替代文字形式。 **PutAltWord** 不會修改這個參數。 您可以視需要從 [**IWordBreaker：： BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)傳遞 *pTextSource* 參數。

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



| 傳回碼                                                                                              | Description                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                     | 作業已順利完成。 也指出不會再處理任何文字。<br/>                                            |
| <dl> <dt>**語言 \_S \_ 大型 \_ 單字**</dt> </dl> | *Cwc* 的值大於 [**IWordBreaker：： Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init)中指定的 *ulMaxTokenSize* 值。 <br/> |



 

## <a name="remarks"></a>備註

**PutAltWord** 會將替代形式的單字放在 [**IWordSink**](iwordsink.md)中。 在 [**IWordBreaker：： BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) 中，單字會放在與文字來源 (*pTextSource* 中原始單字相同的位置。 根據預設， **PutAltWord** 會使用 **WORDREP \_ break \_ EOW** break type from [**WORDREP \_ break \_ type**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) 列舉型別來終止單字。

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

 

 
