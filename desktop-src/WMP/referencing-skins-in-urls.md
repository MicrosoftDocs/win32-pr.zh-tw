---
title: 參考 Url 中的外觀
description: 參考 Url 中的外觀
ms.assetid: 9ae30c12-2dee-46b2-90e2-c101a83856fb
keywords:
- Windows Media Player 的外觀、URL 參考
- 外觀、URL 參考
- 外觀中的 URL 參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b33ac9a5f37dce242797ae93dc4e85b973c76b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675564"
---
# <a name="referencing-skins-in-urls"></a>參考 Url 中的外觀

如果您使用 URL 載入將由 Windows Media Player 播放的媒體檔案，您可以要求使用特定的外觀搭配該檔案。 如果已在使用者的電腦上安裝該面板，則會使用該面板;否則，將會使用先前的外觀。

若要要求面板，請將下列內容新增至 URL 的結尾：


```C++
?WMPSkin=skinname
```



*skinname* 是您想要要求的面板名稱。 請勿在面板的名稱前後使用引號。

例如，若要要求使用 headspace 面板，請輸入下列 HTTP URL：


```C++
https://www.proseware.com/mymedia.wma?WMPSkin=headspace

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於外觀**](about-skins.md)
</dt> </dl>

 

 




