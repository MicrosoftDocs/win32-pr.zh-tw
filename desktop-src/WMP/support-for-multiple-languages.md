---
title: 支援多種語言
description: 支援多種語言
ms.assetid: f46efb7f-73d1-4f64-aa44-cb50170a2245
keywords:
- Windows Media 中繼檔播放清單，支援多種語言
- 中繼檔播放清單，支援多種語言
- 播放清單、支援多種語言
- Windows Media 中繼檔播放清單，支援多種語言
- 中繼檔播放清單，支援多種語言
- 播放清單、多重語言支援
- Windows Media 中繼檔播放清單，語言支援
- 中繼檔播放清單，語言支援
- 播放清單、語言支援
- 支援多種語言
- 多重語言支援
- 語言支援
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d8855aeb798e4243182a6f82479289ccccbd97d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021929"
---
# <a name="support-for-multiple-languages"></a>支援多種語言

Windows Media Player 9 系列或更新版本支援使用 Unicode 字元集建立的 Windows Media 中繼檔。 這可讓您在中繼檔播放清單中包含多語系中繼資料。 下列規則會管理在 Windows Media 中繼檔中使用多語系中繼資料的方式：

-   字元必須使用 UTF-8 編碼配置進行編碼。
-   中繼檔播放清單必須在播放清單層級包含下列 **參數** ：
    ```XML
    <PARAM  NAME = "Encoding"  VALUE = "utf-8">
    
    ```

    

-   只有 Windows Media Player 9 系列或更新版本才支援此功能。
-   如果未使用 UTF-8 編碼和正確的 **PARAM** 專案儲存中繼檔播放清單，則會使用使用者電腦的預設系統地區設定字碼頁面來剖析中繼檔播放清單。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**PARAM 元素**](param-element.md)
</dt> <dt>

[**Windows Media 中繼檔總覽**](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




