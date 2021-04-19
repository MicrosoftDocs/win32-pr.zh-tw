---
description: 本節說明如何設定您的環境，以使用 c + + 中的 Tablet PC platform COM 程式庫。
ms.assetid: c0d7f703-d4aa-4c26-ae81-a4c888383c1e
title: COM 程式庫和 ActiveX 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9304880380ea95bc698c52d200931b77f64480
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971159"
---
# <a name="com-library-and-activex-controls"></a>COM 程式庫和 ActiveX 控制項

本節說明如何設定您的環境，以使用 c + + 中的 Tablet PC platform COM 程式庫。

## <a name="microsoft-visual-c"></a>Microsoft Visual C++

若要在 Visual C++ 中建立 Tablet PC 應用程式，您必須更新系統內容變數、設定 Visual Studio 的目錄選項，以及存取專案中的 Tablet PC 介面。

若要更新環境變數，請依照 Windows SDK 所提供的指示，將環境變數新增至 Visual Studio。

### <a name="accessing-the-tablet-pc-interfaces"></a>存取 Tablet PC 介面

若要存取 Tablet PC 介面，您必須在專案中包含 Msinkaut 和 Msinkaut 的 c 檔案。 \_


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



您也可以使用下列匯入指示詞，而不是 \# 先前列出的 include 語句。


```C++
#import "InkObj.dll" no_namespace exclude("tagXFORM")
```



若要存取 InkAnalysis 介面，您必須 \_ 在專案中包含 IACom .h 和 IACom 檔案。


```C++
#include <IACom.h>
#include <IACom_i.c>
```



您也可以使用下列匯入指示詞，而不是 \# 先前列出的 include 語句。


```C++
#import "IACom.dll" no_namespace exclude("tagXFORM")
```



若要存取 [**InkDivider**](inkdivider-class.md) 介面，您必須 \_ 在專案中包含 msinkaut15 c 和 msinkaut15 .h 檔案。

> [!Note]  
> InkDivider 已被筆墨分析 Api 取代。

 


```C++
#include <msinkaut15.h>
#include <msinkaut15_i.c>
```



您也可以使用下列匯入指示詞，而不是 \# include 語句。


```C++
#import "InkDiv.dll" no_namespace exclude("tagXFORM")
```



若要存取 [**PenInputPanel**](peninputpanel-class.md) 介面，您必須 \_ 在專案中包含 PenInputPanel c 和 PenInputPanel .h 檔案。


```C++
#include <PenInputPanel.h>
#include <PenInputPanel_i.c>
```



您也可以使用下列匯入指示詞，而不是 \# include 語句。


```C++
#import "PIPanel.dll" no_namespace 
```



> [!Note]  
> 在 Windows Vista 中，PenInputPanel Api 已由新的文字輸入面板介面取代。

 

若要存取 [InkEdit](inkedit-control-reference.md) 控制項介面，您必須 \_ 在您的專案中包含筆跡 .h 和筆跡檔。


```C++
#include <inked.h>
#include <inked_i.c>
```



或者，您也可以匯 \# 入 InkEd.dll 檔案。


```C++
#import "InkEd.dll" no_namespace exclude("tagXFORM")
```



 

 



