---
title: 'TS_IE_ 常數 (Textstor) '
description: TS \_ IE \_ \ 常數描述如何插入可包含文字服務所使用之内嵌物件的文字。
ms.assetid: a455d712-42d5-472e-862d-85ae3ba9149f
topic_type:
- apiref
api_name:
- TS_IE_CORRECTION
- TS_IE_COMPOSITION
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9abdb05ba065ed9bf41b5379060c0643053884e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094231"
---
# <a name="ts_ie_-constants"></a>TS \_ IE \_ \* 常數

TS \_ IE \_ \* 常數描述如何插入可包含文字服務所使用之内嵌物件的文字。



| 常數/值                                                                                                                                                                                                                          | Description                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IE_CORRECTION"></span><span id="ts_ie_correction"></span><dl> <dt>**TS \_IE \_ 更正**</dt> <dt> ( 0x1 )</dt> </dl>    | 文字是現有內容的轉換 (更正) ，而且會保留任何 (中繼資料) 的特殊文字標記資訊，例如 .wav 檔案資料或語言識別項。<br/> |
| <span id="TS_IE_COMPOSITION"></span><span id="ts_ie_composition"></span><dl> <dt>**TS \_IE \_ 組合**</dt> <dt> ( 0x2 )</dt> </dl> | 未使用。<br/>                                                                                                                                                                  |



## <a name="remarks"></a>備註

這些常數會用在 [ITextStoreACP：： InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)和 [ITextStoreAnchor：： InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded)的 *dwFlags* 參數中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                         |
| 標頭<br/>                   | <dl> <dt>Textstor。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Textstor .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ITextStoreACP：： InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> <dt>

[ITextStoreAnchor::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded)
</dt> </dl>

 

 





