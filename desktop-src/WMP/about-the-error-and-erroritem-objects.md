---
title: 關於 Error 和 ErrorItem 物件
description: 關於 Error 和 ErrorItem 物件
ms.assetid: 187f6835-3101-45db-87bd-930d222165ce
keywords:
- Windows Media Player，Error 物件
- Windows Media Player 物件模型，Error 物件
- 物件模型，Error 物件
- Windows Media Player ActiveX 控制項，Error 物件
- ActiveX 控制項，Error 物件
- Windows Media PlayerMobile ActiveX 控制項，Error 物件
- Windows Media PlayerMobile，Error 物件
- Error 物件
- Windows Media Player，ErrorItem 物件
- Windows Media Player 物件模型，ErrorItem 物件
- 物件模型，ErrorItem 物件
- Windows Media Player ActiveX control、ErrorItem 物件
- ActiveX control、ErrorItem 物件
- Windows Media PlayerMobile ActiveX control、ErrorItem 物件
- Windows Media PlayerMobile、ErrorItem 物件
- ErrorItem 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84dcd8e0961007c185640b32ac53d249d2e739ca5e1aa4247a6735e09b2a3242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004398"
---
# <a name="about-the-error-and-erroritem-objects"></a>關於 Error 和 ErrorItem 物件

**錯誤** 和 **ErrorItem** 物件會管理 Windows Media Player 的錯誤處理功能。 您可以透過 **error** 屬性從 **Player** 物件取得 **error** 物件。 您可以使用 **error** 物件的 **item** 屬性來建立 **ErrorItem** 物件，以取得 **錯誤** 物件中的特定程式碼。 例如，若要取得第一個錯誤專案的錯誤碼，請輸入：


```C++
myerrorcode = player.error.item(0).errorCode;

```



您也可以使用下列程式碼，以 **錯誤** 物件來叫用 Web 說明：


```C++
player.error.webHelp();

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Error 物件**](error-object.md)
</dt> <dt>

[**ErrorItem 物件**](erroritem-object.md)
</dt> <dt>

[**指令碼語言的播放程式物件模型**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




