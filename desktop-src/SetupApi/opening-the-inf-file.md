---
description: 您必須使用 SetupOpenInfFile 函式來開啟 INF 檔案，才能從其中抓取資訊，或將其他 INF 檔案附加至該檔案。
ms.assetid: ba4d511a-ad19-4619-a10a-cafef789821b
title: 開啟 INF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8493fda983f2942705b97ea243f6cb95e91c15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849603"
---
# <a name="opening-the-inf-file"></a>開啟 INF 檔案

您必須使用 [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) 函式來開啟 INF 檔案，才能從其中抓取資訊，或將其他 INF 檔案附加至該檔案。

下列程式會使用 [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) 開啟 inf 檔案，並將控制碼 MyInf 傳回至已開啟的 INF 檔案。 **SetupOpenInfFile** 的 *InfClass* 參數會指定為 **Null** ，表示應該忽略 INF 檔案的類別。


```C++
HINF MyInf;                //variable to hold the INF handle
UINT ErrorLine;            //variable to hold errors returned
BOOL test=0;                 //variable to receive function success
 
MyInf = SetupOpenInfFile (
      szInfFileName,       //the filename of the inf file to open
      NULL,                //optional class information
      INF_STYLE_WIN4,      //the inf style
      &ErrorLine           //line number of the syntax error
);
```



開啟 INF 檔案之後，您可以呼叫 [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) 函式，將檔案附加至開啟的 INF 檔案。 若要附加數個檔案，請重複此程式。 如果您呼叫 **SetupOpenAppendInfFile** 函式，且傳遞給它的檔案名為 **Null**，則函式會在開啟的 inf 檔案的版本區段中搜尋 (以及 LayoutFile 金鑰的任何附加 INF 檔案) 。 如果函式找到索引鍵，則會附加該索引鍵所指定的檔案， (通常是版面配置。INF) 。 合併多個 INF 檔案時， **SetupOpenAppendInfFile** 會在搜尋版本區段時，從最後附加的 inf 檔案開始。

 

 



