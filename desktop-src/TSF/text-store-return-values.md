---
title: '文字存放區傳回值 (Textstor) '
description: 當檔管理員處理文字存放區時，它會從0xHHHH0200 到0xHHHH0300 的範圍內產生傳回值。 下表依字母順序列出文字存放區的傳回值。
ms.assetid: 20b0a89f-ab52-466f-9669-c6c29ad12de0
topic_type:
- apiref
api_name:
- Text Store Return Values
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adc2e0141eea559371411455973f1fa4aa87f31e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508991"
---
# <a name="text-store-return-values"></a>文字存放區傳回值

當檔管理員處理文字存放區時，它會從 0x *hhhh hhhh* 0200 到 0x *hhhh hhhh* 0300 的範圍產生傳回值。 下表依字母順序列出文字存放區的傳回值。



| 傳回碼/值                                                                                                                                                                                                                          | Description                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_E_FORMAT"></span><span id="ts_e_format"></span><dl> <dt>**TS \_E \_ FORMAT**</dt> <dt>0x8004020a</dt> </dl>                   | 應用程式不支援使用 [**ITextStoreACP：： InsertEmbedded**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)來插入 [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject)物件中所包含的資料類型。<br/> |
| <span id="TS_E_INVALIDPOINT"></span><span id="ts_e_invalidpoint"></span><dl> <dt>**TS \_E \_ INVALIDPOINT**</dt> <dt>0x80040207</dt> </dl> | 參數不在任何字元的周框方塊內。<br/>                                                                                                                                        |
| <span id="TS_E_INVALIDPOS"></span><span id="ts_e_invalidpos"></span><dl> <dt>**TS \_E \_ INVALIDPOS**</dt> <dt>0x80040200</dt> </dl>       | 指定的範圍會延伸至檔之外。<br/>                                                                                                                                                     |
| <span id="TS_E_NOINTERFACE"></span><span id="ts_e_nointerface"></span><dl> <dt>**TS \_E \_ NOINTERFACE**</dt> <dt>0x80040204</dt> </dl>    | 物件不支援要求的介面。<br/>                                                                                                                                                  |
| <span id="TS_E_NOLAYOUT"></span><span id="ts_e_nolayout"></span><dl> <dt>**TS \_E \_ NOLAYOUT**</dt> <dt>0x80040206</dt> </dl>             | 應用程式尚未計算文字版面配置。<br/>                                                                                                                                                     |
| <span id="TS_E_NOLOCK"></span><span id="ts_e_nolock"></span><dl> <dt>**TS \_E \_ NOLOCK**</dt> <dt>0x80040201</dt> </dl>                   | 應用程式沒有檔的唯讀鎖定或讀取/寫入鎖定。<br/>                                                                                                                   |
| <span id="TS_E_NOOBJECT"></span><span id="ts_e_noobject"></span><dl> <dt>**TS \_E \_ NOOBJECT**</dt> <dt>0x80040202</dt> </dl>             | 內嵌的內容位移未放置於 TF \_ 字元 \_ 內嵌字元之前。<br/>                                                                                                                  |
| <span id="TS_E_NOSELECTION"></span><span id="ts_e_noselection"></span><dl> <dt>**TS \_E \_ NOSELECTION**</dt> <dt>0x80040205</dt> </dl>    | 檔沒有選取專案。<br/>                                                                                                                                                                        |
| <span id="TS_E_NOSERVICE"></span><span id="ts_e_noservice"></span><dl> <dt>**TS \_E \_ NOSERVICE**</dt> <dt>0x80040203</dt> </dl>          | 無法傳回內容以符合服務 GUID。<br/>                                                                                                                                             |
| <span id="TS_E_READONLY"></span><span id="ts_e_readonly"></span><dl> <dt>**TS \_E \_ READONLY**</dt> <dt>0x80040209</dt> </dl>             | 檔是唯讀的。 無法修改內容。<br/>                                                                                                                                                     |
| <span id="TS_E_SYNCHRONOUS"></span><span id="ts_e_synchronous"></span><dl> <dt>**TS \_E \_ 同步**</dt> <dt>0x00040300</dt> </dl>    | 無法同步鎖定檔。<br/>                                                                                                                                                          |
| <span id="TS_S_ASYNC"></span><span id="ts_s_async"></span><dl> <dt>**TS \_S \_ ASYNC**</dt> <dt> ( 0x1 )</dt> </dl>                         | 檔已成功接收非同步鎖定。<br/>                                                                                                                                              |



 

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

[**ITextStoreACP：： InsertEmbedded**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> </dl>

 

