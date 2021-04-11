---
description: 適用于 ASF 標頭物件的媒體基礎屬性
ms.assetid: 82d2bdeb-4ccf-4713-980e-59bddc7d9b6a
title: 適用于 ASF 標頭物件的媒體基礎屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db74ccb03536c7766dd7e1564119edbd41d5dbe
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321616"
---
# <a name="media-foundation-attributes-for-asf-header-objects"></a>適用于 ASF 標頭物件的媒體基礎屬性

檔案的最上層 ASF 標頭物件包含數個 ASF 子標頭物件。 ContentInfo 物件會儲存所有這些標頭物件的資訊，並透過屬性將某些值公開給應用程式。

## <a name="file-properties-object"></a>檔案屬性物件

此標頭物件存在於所有的 ASF 檔案中。 這些欄位描述整個簡報的檔案層級屬性。 下表列出 [檔案屬性] 物件中的欄位，以及對應的表示描述項屬性。



| 檔案屬性物件欄位 | 展示描述項屬性                                                                            | Description                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| 檔案識別碼                      | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 檔案 \_ 識別碼**](mf-pd-asf-fileproperties-file-id-attribute.md)                  | 這個檔案的唯一識別碼。                                                               |
| 檔案大小                    | [**MF \_ PD \_ 檔案 \_ \_ 大小總計**](mf-pd-total-file-size-attribute.md)                                         | 檔案的大小（以位元組為單位）。                                                                    |
| 建立日期                | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 建立 \_ 時間**](mf-pd-asf-fileproperties-creation-time-attribute.md)      | 檔案的建立日期和時間。                                                               |
| 資料封包計數           | [**MF \_ PD \_ ASF \_ FILEPROPERTIES 封 \_ 包**](mf-pd-asf-fileproperties-packets-attribute.md)                   | ASF 資料物件中的資料封包數目。                                                 |
| 播放持續時間                | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 播放 \_ 持續時間**](mf-pd-asf-fileproperties-play-duration-attribute.md)      | 播放檔案所需的時間，以 100-毫微秒單位表示。 此值包含預先進行的時間。 |
| 傳送持續時間                | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 傳送 \_ 持續時間**](mf-pd-asf-fileproperties-send-duration-attribute.md)      | 傳送檔案所需的時間，以 100-毫微秒單位表示。                                       |
| 預                      | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 預先進行**](mf-pd-asf-fileproperties-preroll-attribute.md)                   | 在播放檔案之前緩衝資料的時間長度，以 100-毫微秒單位表示。            |
| Flags                        | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 旗標**](mf-pd-asf-fileproperties-flags-attribute.md)                       | 旗標，指出檔案是否為廣播或可搜尋。                                    |
| 最小資料封包大小     | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 最小封 \_ 包 \_ 大小**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | 檔案中的資料封包大小下限（以位元組為單位）。                                        |
| 最大資料封包大小     | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 封 \_ 包 \_ 大小上限**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | 檔案中的資料封包大小上限（以位元組為單位）。                                        |
| 最大位元速率              | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 最大 \_ 位元速率**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)          | 最大瞬間位元速率（以每秒位數為單位）。                                            |



 

## <a name="stream-properties-object"></a>Stream 屬性物件

此標頭物件描述 ASF 檔案中的資料流程屬性。 在媒體基礎中，這是由設定檔物件和資料流程設定物件所管理。 如需詳細資訊，請參閱 [建立及設定 ASF 資料流程](creating-and-configuring-asf-streams.md)。

## <a name="codec-list-object"></a>編解碼器清單物件

如果此標頭物件存在，則 [ [**MF \_ PD \_ ASF \_ CODECLIST**](mf-pd-asf-codeclist-attribute.md) ] 屬性會提供編解碼器的清單，這些編解碼器是用來在 ASF 檔案內編碼串流。 每個資料流程在此物件中都應該有其編解碼器資訊。

## <a name="script-command-object"></a>指令碼命令物件

如果此標頭物件存在，則會指定 ASF 檔案中支援的指令碼命令清單。 指令碼命令包含命令類型、命令名稱和呈現時間。 命令類型和命令名稱是寬字元字串。 您可以使用這些命令來通知用戶端在簡報的某個點執行動作。 例如，應用程式可以使用命令類型 "FILENAME" 來播放 ASF 檔案的連續序列。

若要取得指令碼命令的清單，請從展示描述項取得 [**MF \_ PD \_ ASF \_ 腳本**](mf-pd-asf-script-attribute.md) 屬性。 應用程式應該在開始播放之前，先取出所有的指令碼命令。

## <a name="marker-object"></a>標記物件

標記是 ASF 檔案內的書簽。 應用程式可以使用標記來搜尋內容中的各個點。 每個標記都包含一個標記名稱、相關聯的呈現時間，以及從檔案開頭算起的位移。 [ [**MF \_ PD \_ ASF \_ 標記**](mf-pd-asf-marker-attribute.md) ] 屬性會提供可供檔案使用的標記清單。

## <a name="stream-bitrate-properties-object"></a>資料流程位元速率屬性物件

此標頭會將每個資料流程的平均位元速率儲存在 ASF 檔案中。 此值會儲存在 [**MF \_ SD \_ ASF \_ STREAMBITRATES \_ 位元速率**](mf-sd-asf-streambitrates-bitrate-attribute.md) 屬性中資料流程的資料流程描述元。

## <a name="content-encryption-object"></a>內容加密物件

如果內容提供者已使用 Microsoft 數位 Rights Management 保護內容，則會出現此標頭物件。 下表列出內容加密物件中的欄位，以及對應的表示描述項屬性：



| 內容加密物件欄位 | 展示描述項屬性                                                                         | Description                                                                                        |
|---------------------------------|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| 秘密資料                     | [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ 秘密 \_ 資料**](mf-pd-asf-contentencryption-secret-data-attribute.md) | 包含秘密資料的位元組陣列。                                                                 |
| 保護類型                 | [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ 類型**](mf-pd-asf-contentencryption-type-attribute.md)                | 以 Null 終止的字串，其值為 "DRM"。                                                       |
| 金鑰 ID                          | [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ KEYID**](mf-pd-asf-contentencryption-keyid-attribute.md)              | 以 Null 終止的字串，描述金鑰識別碼。                                          |
| 授權 URL                     | [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ 授權 \_ URL**](mf-pd-asf-contentencryption-license-url-attribute.md) | 以 Null 終止的字串，其中包含要從中取得授權以使用內容的 URL。 |



 

## <a name="extended-content-encryption-object"></a>擴充內容加密物件

如果內容提供者使用 Windows Media Rights Manager 7 SDK 來保護內容，則會出現此標頭物件。 [ [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ 授權 \_ URL**](mf-pd-asf-contentencryption-license-url-attribute.md) ] 屬性提供的位元組陣列，會對應至標頭物件的資料欄位。 此為使用內容的必要欄位。

## <a name="extended-stream-properties-object"></a>擴充資料流程屬性物件

此標頭是標頭擴充物件的一部分。 擴充的資料流程屬性物件會提供資料流程屬性物件中未定義之資料流程的屬性。 這些屬性主要用於判斷由解碼器使用的 "有漏洞 bucket" 參數。 當壓縮資料時，編碼器也會使用這些屬性。 這是由設定檔物件和資料流程設定物件所管理。 如需詳細資訊，請參閱 [建立及設定 ASF 資料流程](creating-and-configuring-asf-streams.md)。

下表列出 [擴充資料流程屬性] 物件欄位和對應的資料流程描述元屬性。



| 擴充資料流程屬性欄位 | 資料流程描述元屬性                                                                                | Description                                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| 資料位元速率                     | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ DATA \_ 位元速率**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)   | 平均資料速率（以每秒位數為單位）。                                                                                   |
| 緩衝區大小                      | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)        | 有漏洞 bucket 大小。 值是可在緩衝區中以平均資料速率容納的資料毫秒數。      |
| 替代資料位元速率           | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ 最大 \_ 資料 \_ 位元速率**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)   | 尖峰資料速率（以每秒的片段）。 尖峰資料速率可用於具有變數位元速率的資料流程。                    |
| 替代緩衝區大小            | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ 最大的 \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)        | 有漏洞 bucket 大小上限。 值是緩衝區中可容納尖峰資料速率的資料毫秒數。 |
| 串流語言識別項               | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ 語言 \_ 識別碼 \_ 索引**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) | 資料流程所使用的語言，指定為語言清單物件中語言清單的索引。         |



 

## <a name="language-list-object"></a>語言清單物件

此標頭物件是標頭擴充物件的一部分。 如果有的話， [**MF \_ PD \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md) 屬性會提供檔案所支援的語言識別項清單。 識別碼符合指定語言的 RFC 1766。

## <a name="mutual-exclusion-object"></a>相互排除物件

此標頭會指定資料流程的群組及其屬性，一次只會傳遞其中一個。 如需詳細資訊，請參閱 [使用 ASF 資料流程的相互排除](using-mutual-exclusion-for-asf-streams.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ASF ContentInfo 物件](asf-contentinfo-object.md)
</dt> <dt>

[ASF 標頭物件](asf-file-structure.md)
</dt> <dt>

[媒體基礎中的 ASF 支援](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



