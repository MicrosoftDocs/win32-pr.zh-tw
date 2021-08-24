---
description: 主要媒體類型
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: 主要媒體類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec660dcb86cfd1da5a80bef106ee8ddd17cf1e89899fea6b824fba5ab9be04e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715298"
---
# <a name="major-media-types"></a>主要媒體類型

在媒體類型中， *主要類型* 會描述資料的整體類別，例如音訊或影片。 *子類型*（如果有的話）會進一步調整主要類型。 例如，如果主要類型是 video，則子類型可能是32位 RGB video。 子類型也可區分編碼格式，例如 h.264 video，從未壓縮的格式。

主要類型和子類型是由 Guid 所識別，並儲存在下列屬性中：



| 屬性                                             | 描述 |
|-------------------------------------------------------|-------------|
| [MF \_ MT \_ 主要 \_ 類型](mf-mt-major-type-attribute.md) | 主要類型。 |
| [MF \_ MT \_ 子類型](mf-mt-subtype-attribute.md)        | 亞。    |



 

以下是定義的主要類型。



| 主要類型                    | 描述                                                                                                                                                | 子類型                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **MFMediaType \_ 音訊**        | 音訊。                                                                                                                                                     | [音訊子類型 guid](audio-subtype-guids.md)。      |
| **MFMediaType \_ 二進位檔**       | 二進位資料流程。                                                                                                                                             | 無。                                                |
| **MFMediaType \_ FileTransfer** | 包含資料檔案的資料流程。                                                                                                                         | 無。                                                |
| **MFMediaType \_ HTML**         | HTML 資料流程。                                                                                                                                               | 無。                                                |
| **MFMediaType \_ 影像**        | 靜止影像資料流程。                                                                                                                                        | [WIC guid 和 clsid](../wic/-wic-guids-clsids.md)。       |
| **MFMediaType \_ 中繼資料**        | 中繼資料資料流程。                                                                                                                                        | 無。       |
| **MFMediaType \_ 保護**    | 受保護的媒體。                                                                                                                                           | 子類型指定內容保護設定。 |
| **MFMediaType \_ 認知**   | 從相機感應器或處理單位串流處理，並瞭解原始的影片資料，並瞭解其環境或人類。 | 無。                                                |
| **MFMediaType \_ 薩米文**         | 已同步處理的可存取媒體交換 (薩米) 字幕。                                                                                                 | 無。                                                |
| **MFMediaType \_ 腳本**       | 腳本資料流程。                                                                                                                                             | 無。                                                |
| **MFMediaType \_ 資料流程**       | 多工資料流程或基本資料流程。                                                                                                                   | [資料流程子類型 Guid](stream-subtype-guids.md)     |
| **MFMediaType \_ 影片**        | 影片。                                                                                                                                                     | [影片子類型 guid](video-subtype-guids.md)。      |



 

協力廠商元件可以定義新的主要類型和新的子類型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[媒體類型](media-types.md)
</dt> </dl>

 

 
