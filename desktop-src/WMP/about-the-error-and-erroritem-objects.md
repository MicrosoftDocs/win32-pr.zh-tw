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
- Windows Media Player Mobile ActiveX 控制項，Error 物件
- Windows Media Player Mobile，Error 物件
- Error 物件
- Windows Media Player，ErrorItem 物件
- Windows Media Player 物件模型，ErrorItem 物件
- 物件模型，ErrorItem 物件
- Windows Media Player ActiveX 控制項，ErrorItem 物件
- ActiveX 控制項，ErrorItem 物件
- Windows Media Player 行動 ActiveX 控制項，ErrorItem 物件
- Windows Media Player Mobile，ErrorItem 物件
- ErrorItem 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23064670f13229aca84ae6dc86cf27cf34abbc56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301099"
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

 

 




