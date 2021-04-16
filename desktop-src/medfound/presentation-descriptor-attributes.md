---
description: 展示描述項屬性
ms.assetid: 2a092a6a-956b-4c1f-955f-529ec08665fe
title: 展示描述項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18bba97a0e0428bf2ceb91b04c79f69b557876a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512564"
---
# <a name="presentation-descriptor-attributes"></a>展示描述項屬性

## <a name="common-presentation-descriptor-attributes"></a>一般展示描述項屬性

下列屬性可以套用至任何展示描述項。



| 屬性                                                                          | 描述                                                                                                                                     |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ PD \_ 應用程式 \_ 內容**](mf-pd-app-context-attribute.md)                        | 包含從受保護媒體路徑到展示描述項的指標 (PMP) 。                                                          |
| [**MF \_ PD \_ 音訊 \_ 編碼 \_ 位元速率**](mf-pd-audio-encoding-bitrate-attribute.md) | 指定標記法的音訊編碼位元速率（以每秒位數為單位）。                                                                 |
| [MF \_ PD \_ 音訊 \_ ISVARIABLEBITRATE](mf-pd-audio-isvariablebitrate.md)              | 指定簡報中的音訊資料流程是否有可變的位元速率。                                                               |
| [**MF \_ PD \_ 持續時間**](mf-pd-duration-attribute.md)                               | 指定簡報的持續時間，以 100-毫微秒單位表示。                                                                              |
| [**MF \_ PD \_ 上次 \_ 修改 \_ 時間**](mf-pd-last-modified-time-attribute.md)         | 指定上一次修改簡報的時間。                                                                                                |
| [**MF \_ PD \_ MIME \_ 類型**](mf-pd-mime-type-attribute.md)                            | 指定內容的 MIME 類型。                                                                                                         |
| [MF \_ PD \_ 播放 \_ 界限 \_ 時間](mf-pd-playback-boundary-time.md)               | 簡報必須開始的時間，相對於媒體來源的開始時間。                                                       |
| [MF \_ PD \_ 播放 \_ 元素 \_ 識別碼](mf-pd-playback-element-id.md)                     | 簡報中播放清單元素的識別碼。                                                                                     |
| [**MF \_ PD \_ PMPHOST \_ 內容**](mf-pd-pmphost-context-attribute.md)                | 包含應用程式之展示描述項的 proxy 物件指標。                                                           |
| [MF \_ PD \_ 慣用 \_ 語言](mf-pd-preferred-language.md)                        | 包含媒體來源慣用的 RFC 1766 語言。                                                                                   |
| [**MF \_ PD \_ 薩米文 \_ STYLELIST**](mf-pd-sami-stylelist-attribute.md)                  | 包含支援的已同步存取媒體交換的易記名稱 (薩米) 樣式。 這個屬性只適用于薩米文的檔案。 |
| [**MF \_ PD \_ 檔案 \_ \_ 大小總計**](mf-pd-total-file-size-attribute.md)               | 指定原始程式檔的大小總計（以位元組為單位）。                                                                                          |
| [**MF \_ PD \_ 影片 \_ 編碼 \_ 位元速率**](mf-pd-video-encoding-bitrate-attribute.md) | 指定標記法的影片編碼位元速率（以每秒位數為單位）。                                                                 |



 

## <a name="presentation-descriptor-attributes-for-asf"></a>適用于 ASF 的簡報描述項屬性

下列屬性適用于 Advanced Systems Format (ASF) 檔的呈現描述項。



| 屬性                                                                                                             | 描述                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**MF \_ PD \_ ASF \_ CODECLIST**](mf-pd-asf-codeclist-attribute.md)                                                       | 包含用來對 ASF 檔案中的內容進行編碼之編解碼器的相關資訊。                     |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ KEYID**](mf-pd-asf-contentencryption-keyid-attribute.md)                          | 指定加密的 ASF 檔案的金鑰識別碼。                                              |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ 授權 \_ URL**](mf-pd-asf-contentencryption-license-url-attribute.md)             | 指定加密 ASF 檔案的授權取得 URL。                                     |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ 秘密 \_ 資料**](mf-pd-asf-contentencryption-secret-data-attribute.md)             | 包含加密 ASF 檔案的秘密資料。                                                      |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ 類型**](mf-pd-asf-contentencryption-type-attribute.md)                            | 指定 ASF 檔案中使用的保護機制類型。                                      |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTIONEX \_ 加密 \_ 資料**](mf-pd-asf-contentencryptionex-encryption-data-attribute.md) | 包含 ASF 檔案的加密資料。                                                            |
| [**MF \_ PD \_ ASF \_ 資料 \_ 長度**](mf-pd-asf-data-length-attribute.md)                                                  | 指定 ASF 檔案的資料區段大小（以位元組為單位）。                                    |
| [**MF \_ PD \_ ASF \_ 資料 \_ 起始 \_ 位移**](mf-pd-asf-data-start-offset-attribute.md)                                     | 指定從 ASF 檔案開頭到第一個資料封包開頭的位移（以位元組為單位）。 |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 建立 \_ 時間**](mf-pd-asf-fileproperties-creation-time-attribute.md)               | 指定一開始建立 ASF 檔案的日期和時間。                                  |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 檔案 \_ 識別碼**](mf-pd-asf-fileproperties-file-id-attribute.md)                           | 指定 ASF 檔案的檔案識別碼。                                                        |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 旗標**](mf-pd-asf-fileproperties-flags-attribute.md)                                | 包含來自 ASF 標頭的其他旗標。                                                     |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 最大 \_ 位元速率**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)                   | 指定 ASF 檔案的最大瞬間位元速率（以每秒位數為單位）。                   |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 封 \_ 包 \_ 大小上限**](mf-pd-asf-fileproperties-max-packet-size-attribute.md)          | 指定 ASF 檔案的封包大小上限（以位元組為單位）                                         |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 最小封 \_ 包 \_ 大小**](mf-pd-asf-fileproperties-min-packet-size-attribute.md)          | 指定 ASF 檔案的最小封包大小（以位元組為單位）。                                        |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES 封 \_ 包**](mf-pd-asf-fileproperties-packets-attribute.md)                            | 指定 ASF 檔案的 [資料] 區段中的封包數目。                                  |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 播放 \_ 持續時間**](mf-pd-asf-fileproperties-play-duration-attribute.md)               | 指定播放 ASF 檔案所需的時間，以 100-毫微秒單位表示。                              |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 預先進行**](mf-pd-asf-fileproperties-preroll-attribute.md)                            | 指定開始播放 ASF 檔案之前緩衝資料的時間量（以毫秒為單位）。    |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 傳送 \_ 持續時間**](mf-pd-asf-fileproperties-send-duration-attribute.md)               | 指定傳送 ASF 檔案所需的時間，以 100-毫微秒單位表示。                              |
| [**MF \_ PD \_ ASF \_ 資訊 \_ 有 \_ 音訊**](mf-pd-asf-info-has-audio-attribute.md)                                           | 指定 ASF 檔案是否至少包含一個音訊串流。                                    |
| [**MF \_ PD \_ ASF \_ 資訊 \_ 有 \_ 非 \_ 音訊 \_ 影片**](mf-pd-asf-info-has-non-audio-video-attribute.md)                     | 指定 ASF 檔案是否包含任何非音訊、非影片的串流。                             |
| [**MF \_ PD \_ ASF \_ 資訊 \_ 有 \_ 影片**](mf-pd-asf-info-has-video-attribute.md)                                           | 指定 ASF 檔案是否至少包含一個影片串流。                                    |
| [**MF \_ PD \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md)                                                         | 指定 ASF 檔案中使用的語言清單。                                                 |
| [MF \_ PD \_ ASF \_ LANGLIST \_ LEGACYORDER](mf-pd-asf-langlist-legacyorder.md)                                              | 包含目前簡報中使用的 RFC 1766 語言清單。                              |
| [**MF \_ PD \_ ASF \_ 標記**](mf-pd-asf-marker-attribute.md)                                                             | 指定 ASF 檔案中的標記。                                                                |
| [**MF \_ PD \_ ASF \_ 中繼資料 \_ 是 \_ VBR**](mf-pd-asf-metadata-is-vbr-attribute.md)                                         | 指定 ASF 檔案是否使用變數位元速率 (VBR) 編碼。                                 |
| [**MF \_ PD \_ ASF \_ 中繼資料 \_ 有漏洞 \_ BUCKET 組 \_ 配對**](mf-pd-asf-metadata-leaky-bucket-pairs-attribute.md)                | 說明 VBR ASF 檔案的緩衝需求。                                             |
| [**MF \_ PD \_ ASF \_ 中繼資料 \_ V8 \_ BUFFERAVERAGE**](mf-pd-asf-metadata-v8-bufferaverage-attribute.md)                     | 指定 VBR ASF 檔案所需的平均緩衝區大小。                                         |
| [**MF \_ PD \_ ASF \_ 中繼資料 \_ V8 \_ VBRPEAK**](mf-pd-asf-metadata-v8-vbrpeak-attribute.md)                                 | 指定 VBR ASF 檔案中最高的瞬間位元速率。                                          |
| [**MF \_ PD \_ ASF \_ 腳本**](mf-pd-asf-script-attribute.md)                                                             | 指定 ASF 檔案中的指令碼命令。                                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> <dt>

[簡報描述項](presentation-descriptors.md)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> </dl>

 

 



