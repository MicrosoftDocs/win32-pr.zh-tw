---
title: 中繼檔延伸指導方針
description: 中繼檔延伸指導方針
ms.assetid: 079fac31-7a6f-4775-a337-870ad25a56a0
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
ms.openlocfilehash: 31d2793b19576e26096bc30c834666828cf9ed29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022022"
---
# <a name="metafile-extension-guidelines"></a>中繼檔延伸指導方針

副檔名可提供獨立軟體廠商 (ISV) ，其中包含使用延伸模組之應用程式轉譯需求的相關資訊，並可讓內容作者以一般類型的播放程式為目標。

Windows Media 中繼檔副檔名用來識別中繼檔所參考之 Windows Media 檔案的格式。 具有. 地板蠟、. 300k.wvx 或 .asx 副檔名的 Windows Media 中繼檔會分別參考副檔名為 .wma、.wmv 和 .asf 的檔案。 所有的中繼檔（不論使用的副檔名為何）都有指定 **version** 屬性之檔案開頭的 **ASX** 元素標記。

下表顯示每種類型的中繼檔副檔名所參考的媒體檔案類型。 資料行列出媒體副檔名，資料列會列出中繼檔名稱延伸。 資料行中的 X 表示特定的中繼檔副檔名可以參考的媒體檔案類型。



| 分機 | .asf | .wma | .wmv |
|-----------|------|------|------|
| . 300k.wvx      | X    | X    | X    |
| . 地板蠟      | X    | X    |      |
| .asx      | X    |      |      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**副檔名**](file-name-extensions.md)
</dt> <dt>

[**中繼檔播放清單**](metafile-playlists.md)
</dt> <dt>

[**Windows Media 中繼檔指南**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




