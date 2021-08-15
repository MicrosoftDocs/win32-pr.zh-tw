---
title: 支援多種語言
description: 支援多種語言
ms.assetid: f46efb7f-73d1-4f64-aa44-cb50170a2245
keywords:
- Windows媒體中繼檔播放清單，支援多種語言
- 中繼檔播放清單，支援多種語言
- 播放清單、支援多種語言
- Windows媒體中繼檔播放清單，支援多種語言
- 中繼檔播放清單，支援多種語言
- 播放清單、多重語言支援
- Windows媒體中繼檔播放清單，語言支援
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
ms.openlocfilehash: a04fc9f3a1f6d481ad88e85323c7bdd253ddde7dd2f020de2ea42e77c83c4ea3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002068"
---
# <a name="support-for-multiple-languages"></a>支援多種語言

Windows Media Player 9 系列或更新版本支援使用 Unicode 字元集所建立的 Windows 媒體中繼檔。 這可讓您在中繼檔播放清單中包含多語系中繼資料。 下列規則會管理 Windows 媒體中繼檔中多語系中繼資料的使用：

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

[**Windows媒體中繼檔總覽**](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




