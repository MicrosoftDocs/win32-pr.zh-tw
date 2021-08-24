---
title: 呼叫函式
description: 呼叫函式
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- Windows Media Player 的面板，呼叫 JScript 中的函式
- 在 JScript 中呼叫函式的外觀
- 在 JScript 中呼叫函數
- 適用于面板的 JScript 檔案，呼叫函式
- Windows Media Player 的 scriptFile 屬性 JScript 中的外觀
- JScript 中的外觀、scriptFile 屬性
- 屬性，JScript 中的 scriptFile
- JScript 中的 scriptFile 屬性
- scriptFile 屬性的 JScript 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e41b5fdfd6109292a1a42cae43e42e8424348090541fd50a8d83f04d23b8329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764268"
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
> 如果您有多個 view，則只有載入目前視圖之檔案中的函式可供 XML 使用，以及使用目前的視圖執行 JScript 程式碼。 在其他視圖中載入的檔案不在目前的視圖範圍內。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用 JScript**](using-jscript.md)
</dt> </dl>

 

 




