---
title: 副檔名
description: 副檔名
ms.assetid: c17bf4e5-b469-45b6-bc22-2b451723d85e
keywords:
- Windows Media 中繼檔，擴充功能
- Windows Media 中繼檔，副檔名
- 中繼檔，擴充功能
- 中繼檔，副檔名
- Windows Media，中繼檔
- Windows Media 中繼檔的副檔名
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d95d5bcba9bbad5f04b0d085ba712d5b9306c8b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965814"
---
# <a name="file-name-extensions"></a>副檔名

使用 Windows Media 中繼檔的副檔名時，有特定的指導方針。 Windows Media 中繼檔名稱延伸模組是用來識別不同類型的 Windows Media 檔案。 副檔名可提供獨立軟體廠商 (ISV) 包含使用特定延伸模組之應用程式轉譯需求的相關資訊，並讓內容作者以一般類型的媒體播放機為目標。

下表列出檔案名延伸指導方針。 建議您將檔案標頭中的檔案 MIME 類型用於檔案類型識別。



| 副檔名 | MIME 類型 (MIME type)      | 檔案內容                                                                                                                                                                            |
|---------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .wma                | 音訊/x-ms-wma | 只有音訊內容的 Windows Media 檔案。 通常用來下載及播放檔案，或串流內容。                                                                             |
| .wmv                | 影片/x-ms-wmv | 具有音訊和/或影片內容的 Windows Media 檔案。 通常用來下載及播放檔案，或串流內容。                                                                     |
| .asf                | video/x-ms-asf | 舊版內容。 通常用來下載及播放檔案，或串流內容。 可能包含音訊和/或影片內容。 通常用來下載及播放檔案，或串流內容。 |
| .wm                 | 影片/x-ms-wm  | 保留                                                                                                                                                                                |
| . 地板蠟                | 音訊/x-地板蠟 | 參考具有 .asf、.wma 或副檔名為地板蠟之 Windows Media 檔案的中繼檔。                                                                                             |
| . 300k.wvx                | 影片/x-300k.wvx | 參考包含 .wma、.wmv、. 300k.wvx 或. 地板蠟副檔名之 Windows Media 檔案的中繼檔。                                                                                       |
| .asx                | video/x-ms-asf | 參考包含 .wma、. 地板蠟、.wmv、. 300k.wvx、.asf 或 .asx 副檔名之 Windows Media 檔案的中繼檔。                                                                           |
| .wmx                | 影片/x-300k.wvx | 保留的。                                                                                                                                                                               |



 

## <a name="remarks"></a>備註

轉譯 Windows Media 檔案的任何應用程式都必須支援腳本和數位版權管理 (DRM) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Windows Media 中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Media 中繼檔指南**](windows-media-metafile-guide.md)
</dt> <dt>

[**Windows Media 中繼檔參考**](windows-media-metafile-reference.md)
</dt> </dl>

 

 




