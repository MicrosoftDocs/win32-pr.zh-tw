---
title: 關於薩米文的 Url
description: 關於薩米文的 Url
ms.assetid: 6898a0d5-cfd0-4ba5-8cd1-907cf110667c
keywords:
- 'Windows Media Player，可同步的可存取媒體交換 (薩米文) '
- 'Windows Media Player 物件模型、已同步處理的可存取媒體交換 (薩米文) '
- '物件模型、同步的可存取媒體交換 (薩米) '
- 'Windows Media Player行動裝置、已同步處理的可存取媒體交換 (薩米) '
- 'Windows Media Player ActiveX 控制項、同步可存取媒體交換 (薩米文) '
- 'Windows Media PlayerMobile ActiveX control、可同步存取的媒體交換 (薩米文) '
- 'ActiveX control、可同步存取的媒體交換 (薩米文) '
- 已同步處理的可存取媒體交換 (薩米) ，檔案
- 薩米文 (同步處理的可存取媒體交換) 、檔案
- 已同步的可存取媒體交換 (薩米) 、Url
- 薩米文 (同步處理的可存取媒體交換) 、Url
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a35976c6988ad4298c812005002da010730d5254bd7c010f24fe32741be393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956798"
---
# <a name="about-sami-urls"></a>關於薩米文的 Url

您可以使用單一 URL，將薩米文的檔案與數位媒體檔案相關聯。 這是使用 *薩米* 文 URL 參數來完成的。 URL 參數的前面會有基底 URL 和？ 字元之後。 具有 *薩米* 參數的 URL 會遵循此語法：

*URL*？*薩米* = 文 *captionsURL*。

URL 參數的值會在參數名稱和等號後面，如下列範例所示：


```C++
https://proseware.com/samitest.wma?sami=https://acc.proseware.com/test.smi

```



此 URL 語法常用於超連結或 Windows 媒體中繼檔中，以直接連結至數位媒體檔案和薩米文檔案的位置。 當使用者按一下超連結時，Windows Media Player 會以完整模式啟動，並播放數位媒體內容。

如果未指定 *薩米* URL 參數，Windows Media Player 將會尋找與數位媒體檔案位於相同位置的薩米文檔案，而且檔案名除外（副檔名必須是 smi-s）也會有相同的名稱。 如果有這類檔案存在，則會在播放程式中啟用標題顯示時自動開啟。

按一下 [**播放**] 功能表，然後按一下 [**標題] 和 [副標題**]，再按一下 [**開啟**]，即可在 Windows Media Player 中啟用隱藏式輔助字幕。 如果啟用了隱藏式輔助字幕，當媒體專案播放時，會顯示包含在薩米文檔案中的標題。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**將隱藏式輔助字幕新增至數位媒體**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




