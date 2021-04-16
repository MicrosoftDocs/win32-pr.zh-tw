---
title: 呼叫函式
description: 呼叫函式
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- Windows Media Player 的外觀，在 JScript 中呼叫函式
- 在 JScript 中呼叫函數的外觀
- 在 JScript 中呼叫函數
- 用於外觀的 JScript 檔案，呼叫函式
- Windows Media Player 的外觀、JScript 中的 scriptFile 屬性
- scriptFile 屬性（JScript）中的外觀
- 屬性，JScript 中的 scriptFile
- JScript 中的 scriptFile 屬性
- 適用于外觀的 JScript 檔案，scriptFile 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9450c8ca09b75f66f6206c850a656192bb1bb9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507441"
---
# <a name="calling-functions"></a>呼叫函式

如果您需要呼叫多行程式碼，您可以使用 **VIEW** 專案的 **scriptFile** 屬性載入腳本檔案，然後呼叫腳本中的函數。 您可以針對每個 view 載入一個以上的檔案：


```C++
scriptFile = "myfile1.js;myfile2.js;myfile3.js"

```



載入腳本檔案之後，您可以從 [View] 區段內呼叫函式。 例如，若要在按一下某個名稱時呼叫稱為 *myfunction* 的函式，請輸入下列內容：


```C++
onclick = "JScript: myfunction()"

```



> [!Note]  
> 如果您有一個以上的視圖，則只有在目前的視圖中載入的檔案中的函式可供 XML 和 JScript 程式碼使用。 在其他視圖中載入的檔案不在目前的視圖範圍內。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用 JScript**](using-jscript.md)
</dt> </dl>

 

 




