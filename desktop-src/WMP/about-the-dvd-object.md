---
title: 關於 DVD 物件
description: 關於 DVD 物件
ms.assetid: 6c255e9e-d537-4f4f-865c-b7fb26c8e413
keywords:
- Windows Media Player、DVD 物件
- Windows Media Player 物件模型、DVD 物件
- 物件模型、DVD 物件
- Windows Media Player ActiveX 控制項、DVD 物件
- ActiveX 控制項，DVD 物件
- Windows Media PlayerMobile ActiveX control、DVD 物件
- Windows Media Player行動電話、DVD 物件
- DVD 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109587f30e7df0ff49b1cdbe5b45d818decb1a3f50ffe4a4ba9cde53d00833f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583760"
---
# <a name="about-the-dvd-object"></a>關於 DVD 物件

**Dvd** 物件會新增 dvd 媒體的特定功能。 一般而言，DVD 媒體的處理方式就像 Windows Media Player 中的其他數位媒體一樣。 比方說，DVD 光碟機是使用 **CdromCollection** 物件來列舉，而 dvd 標題和章節則是使用 **播放清單** 物件和 **媒體** 物件來操作。 有些功能是 DVD 專用的，而 **dvd** 物件則提供此功能。 例如，DVD 的概念稱為「網域」。 若要取出 DVD 媒體的目前網域，請輸入下列內容：


```C++
mydomain = player.dvd.domain;

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DVD 物件**](dvd-object.md)
</dt> <dt>

[**指令碼語言的播放程式物件模型**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




