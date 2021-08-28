---
description: 定義來源解析程式的行為。 配置處理常式和位元組資料流程處理常式也會使用這些旗標。
ms.assetid: fe0b9090-5d2a-41a4-a806-57c874d3b3a2
title: '來源解析程式旗標 (Mfidl .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c779a54467390abf6cfb186f6b76043fd19617f5d129b88e6697a45c01708510
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847818"
---
# <a name="source-resolver-flags"></a>來源解析程式旗標

定義來源解析程式的行為。 配置處理常式和位元組資料流程處理常式也會使用這些旗標。



| 常數/值                                                                                                                                                                                                                                                                                                                                                                                               | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_RESOLUTION_MEDIASOURCE"></span><span id="mf_resolution_mediasource"></span><dl> <dt>**MF \_解決方式 \_ MEDIASOURCE**</dt> <dt>0x00000001</dt> </dl>                                                                                                                                           | 嘗試建立媒體來源。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="MF_RESOLUTION_BYTESTREAM"></span><span id="mf_resolution_bytestream"></span><dl> <dt>**MF \_解決方式 \_ BYTESTREAM**</dt> <dt>0x00000002</dt> </dl>                                                                                                                                              | 嘗試建立位元組資料流程。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="MF_RESOLUTION_CONTENT_DOES_NOT_HAVE_TO_MATCH_EXTENSION_OR_MIME_TYPE_"></span><span id="mf_resolution_content_does_not_have_to_match_extension_or_mime_type_"></span><dl> <dt> **MF \_ 解析 \_ 內容 \_ 不 \_ \_ 需要 \_ \_ 符合延伸模組 \_ \_ 或 \_ MIME \_ 類型**</dt>的 <dt>0x00000010</dt> </dl> | 如果來源解析失敗，使用針對 MIME 類型或副檔名所註冊的位元組資料流程處理常式，來源解析程式會列舉所有已註冊的位元組資料流程處理常式。<br/> 位元組資料流程處理常式是以副檔名或 MIME 類型來註冊。 來源解析程式一開始會嘗試使用與副檔名或 MIME 類型相符的處理常式。 如果失敗，則根據預設，整個來源解析會失敗，而且來源解析程式會將錯誤碼傳回給應用程式。 但是，如果指定此旗標，來源解析程式會繼續透過所有已註冊的位元組資料流程處理常式來列舉。 可能是不相符的處理常式可能會成功建立媒體來源。<br/> 此旗標無法與 MF 解析結合，因此 \_ \_ \_ \_ \_ \_ 在 \_ FAIL 旗標上保持位元組資料流程保持運作。 如需詳細資訊，請參閱「備註」。<br/> |
| <span id="MF_RESOLUTION_KEEP_BYTE_STREAM_ALIVE_ON_FAIL"></span><span id="mf_resolution_keep_byte_stream_alive_on_fail"></span><dl> <dt>**MF \_解決 \_ \_ \_ \_ \_ \_ 失敗的情況，讓位元組資料流程保持**</dt>運作 <dt></dt> </dl>                                                                             | 如果來源解析失敗，來源解析程式就不會關閉位元組資料流程。 根據預設，來源解析程式會在失敗時關閉位元組資料流程。<br/> 如果使用此旗標，且來源解析失敗，則呼叫端應該再次呼叫方法，並設定 MF \_ 解析 \_ 內容 \_ \_ 不 \_ 需要 \_ \_ 符合延伸模組 \_ \_ 或 \_ MIME \_ 類型旗標。<br/> 此旗標無法與 MF \_ 解析內容結合 \_ \_ \_ ，而不 \_ 需要 \_ \_ 符合 \_ 延伸模組 \_ 或 \_ MIME \_ 類型旗標。 如需詳細資訊，請參閱「備註」。<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="MF_RESOLUTION_READ"></span><span id="mf_resolution_read"></span><dl> <dt>**MF \_解決方式 \_ 讀取**</dt> <dt>0x00010000</dt> </dl>                                                                                                                                                                | 要求來源的讀取存取權。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MF_RESOLUTION_WRITE"></span><span id="mf_resolution_write"></span><dl> <dt>**MF \_解決方式 \_ 寫入**</dt> <dt>0x00020000</dt> </dl>                                                                                                                                                             | 要求來源的寫入存取權。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="MF_RESOLUTION_DISABLE_LOCAL_PLUGINS"></span><span id="mf_resolution_disable_local_plugins"></span><dl> <dt>**MF \_解決方式 \_ 停用 \_ 本機 \_ 外掛程式**</dt> <dt>0x00000040</dt> </dl>                                                                                                           | 來源解析程式不會使用本機註冊的配置或 bytestream 處理常式外掛程式。<br/> 需要 Windows 8。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## <a name="remarks"></a>備註

當應用程式使用 [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) 介面時，會設定這些旗標。 來源解析程式會將相同的旗標傳遞給 [**IMFByteStreamHandler：： BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) 和 [**IMFSchemeHandler：： BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject) 方法。

您必須指定其中一個 MF \_ 解析 \_ MEDIASOURCE 或 mf \_ 解析 \_ BYTESTREAM 旗標。 其餘旗標都是選擇性的。

適用于 \_ 下列案例的 MF 解析 \_ \_ \_ \_ \_ 會在「失敗」旗標上定義「位元組資料流程保持 \_ 運作」：

1.  應用程式嘗試透過網路開啟來源。 應用程式會設定 MF \_ 解析 \_ ， \_ 讓 \_ 位元組 \_ 資料流程 \_ 在 \_ 失敗旗標上保持運作。

2.  來源的 URL 包含不正確的檔案名副檔名。 因為副檔名錯誤，所以預設的位元組資料流程處理常式無法建立媒體來源。 由於應用程式會將 MF 解析設定為「失敗」旗標上的「 \_ \_ 位元組資料流程保持運作」 \_ ，因此 \_ \_ \_ \_ 來源解析程式會快取位元組資料流程。

3.  來源解析程式會將錯誤碼傳回給應用程式。

4.  用戶端會再次開啟來源，這次設定 MF \_ 解析 \_ 內容 \_ \_ 不 \_ 需要 \_ \_ 符合延伸模組 \_ \_ 或 \_ MIME \_ 類型旗標。 此旗標會導致來源解析程式嘗試所有已註冊的處理常式，而不只是預設處理常式。 因為已快取位元組資料流程，所以來源解析程式不需要再次開啟位元組資料流程。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎常數](media-foundation-constants.md)
</dt> <dt>

[**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
</dt> <dt>

[**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)
</dt> <dt>

[**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> <dt>

[來源解析程式](source-resolver.md)
</dt> </dl>

 

 




