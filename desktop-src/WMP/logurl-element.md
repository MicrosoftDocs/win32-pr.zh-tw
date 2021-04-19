---
title: LOGURL 元素
description: LOGURL 元素會指示 Windows Media Player 將任何記錄資料提交至指定的 URL。
ms.assetid: fc1895af-c9d7-43ca-9839-7e884cc219f4
keywords:
- LOGURL 元素 Windows Media Player
topic_type:
- apiref
api_name:
- LOGURL Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f5fc4a5259f009e7298c0609fc4e6fa8c533b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977503"
---
# <a name="logurl-element"></a>LOGURL 元素

**LOGURL** 元素會指示 Windows Media Player 將任何記錄資料提交至指定的 URL。

``` syntax
<LOGURL
   HREF = "URL"
/>
```

## <a name="attributes"></a>屬性

需要) **HREF** (

可以處理記錄要求的主機 URL。

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素           |
|-----------------|--------------------|
| 父元素 | **ASX**， **進入** |
| 子元素  | 無               |



 

## <a name="remarks"></a>備註

**LOGURL** 元素可讓用戶端中繼檔播放清單將其他記錄資訊傳送到指定的伺服器。 當檔案開啟時，記錄資訊會自動傳送到播放清單的源伺服器，而且會在每個 **LOGURL** 中指定給 **ASX** 元素（如果有的話）。 當到達專案時，記錄資訊也會傳送到針對 **entry** 元素指定的每個 **LOGURL** 。 在 **LOGURL** 元素的 **HREF** 屬性中指定的 URL 必須是能夠處理記錄要求的主控制項位址。 URL 可以是任何有效的 HTTP URL。 URL 也可以指出 CGI 腳本的位置。

**LOGURL** 元素唯一有效的通訊協定為 HTTP 和 HTTPS。

在 **ASX** 元素範圍內的 **LOGURL** 元素只適用于它所在的中繼檔，不論該中繼檔是否從其他中繼檔參考。 **LOGURL** 元素會強制提交從其定義範圍內串流處理之所有內容的記錄資料，而且只會針對從其定義範圍內串流的內容進行提交。 記錄檔資料會提交至源伺服器，以及範圍內每個 **LOGURL** 專案中所列的所有 url。 記錄檔資料只會提交到每個列出的 URL 一次，即使相同的 URL 在指定的範圍內列出一次以上。 重複 **專案** 會導致另一個提交至列出的 url。

中繼檔播放清單中的 **LOGURL** 元素數目沒有任何限制。

## <a name="examples"></a>範例


```XML
<ASX VERSION="3.0">
  <TITLE>Example Media Player Show</TITLE>
  <LOGURL HREF="https://example.microsoft.com/info/showlog.asp?whatsup" />
  <ENTRY>
    <REF href="mms://ucast.proseware.com/Media1.asf" />
    <LOGURL HREF="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal"/>
  </ENTRY>
</ASX>
```



以下是有效 Url 的範例。

ISAPI 應用程式的 URL：


```XML
https://www.proseware.com/logs/WMSLogging.dll
```



CGI 腳本的 URL：


```XML
https://www.proseware.com/cgi-bin/My_WMS_Logging_Script.pl
```



有效的 HTTP URL：


```XML
https://www.proseware.com/some/arbitrary/path/My_WMS_Logging_Page.asp?PubPoint=FooPubPoint&AnotherName=AnotherValue
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------|
| 版本<br/> | Windows Media Player 70 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Windows Media 中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Media 中繼檔參考**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





