---
description: 資料流程描述元屬性
ms.assetid: 1364d7c5-67e8-49b6-8038-d6d4ea03fb7d
title: 資料流程描述元屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5db29ef0076415ff07e9ed25f7e6ca3e0588ec25257802fe0c7829ab3178c935
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953228"
---
# <a name="stream-descriptor-attributes"></a>資料流程描述元屬性

## <a name="common-stream-descriptor-attributes"></a>通用資料流程描述元屬性

下列屬性適用于資料流程描述項。



| 屬性                                                   | 描述                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**MF \_ SD \_ 語言**](mf-sd-language-attribute.md)        | 指定資料流程的語言。                                                  |
| [MF \_ SD \_ 互斥 \_](mf-sd-mutually-exclusive.md) | 指定資料流程是否與相同類型的其他資料流程相互排斥。 |
| [**已 \_ 保護 MF SD \_**](mf-sd-protected-attribute.md)      | 指定資料流程是否包含受保護的內容。                                |
| [MF \_ SD \_ STREAM \_ 名稱](mf-sd-stream-name.md)               | 包含資料流程的名稱。                                                        |



 

## <a name="asf-specific-stream-descriptor-attributes"></a>ASF-Specific 資料流程描述元屬性

下列屬性適用于 Advanced 系統格式 (ASF) 檔的資料流程描述元。



| 屬性                                                                                                                | 描述                                                                                |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)                      | 指定在 ASF 檔案中資料流程所需的平均緩衝區大小（以位元組為單位）。            |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ DATA \_ 位元速率**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)                 | 在 ASF 檔案中指定資料流程的平均資料位元速率，以每秒位數表示。        |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ 語言 \_ 識別碼 \_ 索引**](mf-sd-asf-extstrmprop-language-id-index-attribute.md)               | 在 ASF 檔案中指定資料流程所使用的語言。                                    |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ 最大的 \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)                      | 指定 ASF 檔案中資料流程所需的緩衝區大小上限（以位元組為單位）。            |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ 最大 \_ 資料 \_ 位元速率**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)                 | 指定 ASF 檔案中資料流程的最大資料位速率（以每秒位數為單位）         |
| [**MF \_ SD \_ ASF \_ 中繼資料 \_ 裝置 \_ 一致性 \_ 範本**](mf-sd-asf-metadata-device-conformance-template-attribute.md) | 針對 ASF 檔案中的資料流程指定裝置一致性範本，以每秒位數為單位。 |
| [**MF \_ SD \_ ASF \_ STREAMBITRATES \_ 位元速率**](mf-sd-asf-streambitrates-bitrate-attribute.md)                               | 在 ASF 檔案中指定資料流程的平均位元速率，以每秒位數表示。             |



 

## <a name="sami-media-source-stream-descriptor-attributes"></a>薩米文媒體來源串流描述元屬性

下列屬性適用于薩米文媒體來源的資料流程描述項。



| 屬性                                                       | 描述                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**MF \_ SD \_ 薩米文 \_ 語言**](mf-sd-sami-language-attribute.md) | 包含針對資料流程所定義的已同步可存取媒體交換 (薩米) 語言名稱。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> </dl>

 

 



