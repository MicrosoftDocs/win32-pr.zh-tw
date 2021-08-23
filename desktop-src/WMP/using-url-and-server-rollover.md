---
title: 使用 URL 和伺服器變換
description: 使用 URL 和伺服器變換
ms.assetid: d0d15b1c-5631-486e-8490-b85ec51bd355
keywords:
- Windows媒體中繼檔播放清單，URL 變換
- 播放清單，URL 變換
- 中繼檔播放清單，URL 變換
- Windows媒體中繼檔播放清單，伺服器變換
- 播放清單，伺服器變換
- 中繼檔播放清單，伺服器變換
- Windows媒體中繼檔播放清單，通訊協定變換
- 播放清單，通訊協定變換
- 中繼檔播放清單，通訊協定變換
- Windows Media Player，URL 變換
- Windows Media Player，伺服器變換
- Windows Media Player，通訊協定變換
- URL 變換
- 伺服器變換
- 通訊協定變換
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3988ff019fba838e86ea1d0e7b0f6124c367bb8b505a0f2d2e2f639b94d93e52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465670"
---
# <a name="using-url-and-server-rollover"></a>使用 URL 和伺服器變換

您可以使用中繼檔播放清單，在無法存取或播放資料流程時，提供自動變換替代內容來源的方法。 您可以使用這個變換方法，在不同的伺服器或不同類型的伺服器上指定相同內容的來源。 例如，您可以指定不同 Windows 媒體伺服器上的第一個替代。 如果該內容無法播放，用戶端可以變換為 web 伺服器上的第二個替代。 Windows Media Player 會根據 Windows 媒體內容設定，自動嘗試變換至不同的通訊協定，然後再嘗試播放清單中的換用 url。

藉由在一個 **專案專案** 中連續放置多個 **REF** 元素，來設定伺服器和通訊協定變換。 每個 **REF** 元素都會指定媒體檔案或資料流程的替代位置或通訊協定。

範例程式碼


```XML
<!--Server and protocol rollover is set for the file Rollover.wma.-->
<ASX version="3.0">
    <TITLE>MyServer Rollover</TITLE>
   <ENTRY>
      <REF HREF="mms://Server1.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server2.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server3.proseware.com/Path/Rollover.wma"/>
      <REF HREF="https://www.proseware.com/Path/Rollover.wma"/>
   </ENTRY>
</ASX>

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立中繼檔播放清單**](creating-metafile-playlists.md)
</dt> <dt>

[**使用中繼檔播放清單**](using-metafile-playlists.md)
</dt> </dl>

 

 




