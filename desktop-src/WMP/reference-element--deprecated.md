---
title: '參考元素 (已被取代) '
description: '參考元素 (已被取代) '
ms.assetid: 0a549750-abaa-43bf-8420-8fe00eb6feff
keywords:
- Windows Media 中繼檔，reference 元素
- 中繼檔，reference 元素
- reference 元素
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c521b080609bbe51470a2de960481a86e8264c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966810"
---
# <a name="reference-element-deprecated"></a>參考元素 (已被取代) 

本主題說明在目前版本的 Windows Media 中繼檔中不再使用的功能。

**Reference** 元素包含 url 的參考清單。 清單中的每個專案都有格式 Ref *XX*  =  *URL*，其中 *XX* 是整數，而 *url* 是 Advanced 系統格式的 url (ASF) 檔。

**語法**


```XML
[reference]
RefXX = URL
RefXX = URL
   
<entity type="hellip"/>
```



以 *XX* 表示的整數必須是遞增順序。 也就是說，每一行中的整數必須大於上一行中的整數。

當用戶端程式讀取參考專案時，它會嘗試連接至清單中第一個 URL 所代表的媒體檔案。 如果失敗，用戶端程式會嘗試連接到清單中下一個 URL 所代表的檔案。 用戶端程式會繼續執行清單，直到成功連接或到達清單結尾為止。 請注意，如果用戶端程式成功連接，則不會讀取清單中的任何後續 Url。

**範例程式碼**

在下列範例中，用戶端程式會先嘗試連接到以 mms URL 表示的檔案。 如果失敗，用戶端程式會嘗試連接至 HTTP URL 所表示的檔案。


```XML
[reference]
Ref01 = mms://example.com/MusicFile.wma
Ref02 = https://example.com/MusicFile.wma

```



## <a name="remarks"></a>備註

ASF 檔案格式包含各種不同的媒體類型，包括音訊和影片。 ASF 檔案也會使用數種不同的副檔名，包括 .wma 和 .wmv。

以 *XX* 表示的整數必須是遞增順序。 也就是說，每一行中的整數必須大於上一行中的整數。

當用戶端程式讀取參考專案時，它會嘗試連接至清單中第一個 URL 所代表的媒體檔案。 如果失敗，用戶端程式會嘗試連接到清單中下一個 URL 所代表的檔案。 用戶端程式會繼續執行清單，直到成功連接或到達清單結尾為止。 請注意，如果用戶端程式成功連接，則不會讀取清單中的任何後續 Url。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**舊版的 Windows Media 中繼檔 (已淘汰)**](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




