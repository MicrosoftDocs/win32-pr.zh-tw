---
description: 若要使用應用程式字典搭配 Tablet PC API，您必須先使用應用程式字典的單字清單建立檔案。
ms.assetid: 6abadad1-262b-4536-8846-1c06226dc18a
title: 使用應用程式字典搭配 Tablet PC 平臺 Api
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c30fec5539a9b1f4efb0ca89a53568becff2368942d069149106a4032676d50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091296"
---
# <a name="using-application-dictionaries-with-the-tablet-pc-platform-apis"></a>使用應用程式字典搭配 Tablet PC 平臺 Api

若要使用應用程式字典搭配 Tablet PC API，您必須先使用應用程式字典的單字清單建立檔案。

最簡單的解決方法是使用包含單字清單的文字檔。 當您的應用程式載入時，它會讀取文字檔，並從檔案中的單字清單建立 [**單詞表**](inkwordlist-class.md) 物件。 針對與應用程式字典相關聯的每個 [**RecognizerCoNtext**](inkrecognizercontext-class.md) ，將 **RecognizerCoNtext** 物件的 [[**單詞表**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)] 屬性設定為文字檔中的單字清單。

下列範例說明如何從 [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1)集合建立 [**單詞表**](inkwordlist-class.md)物件。 此範例假設您已從磁片載入單字清單，並從這些字組建立 StringCollection 集合。


```C++
using System.Collections.Specialized;
using Microsoft.Ink;
//...
RecognizerContext theRecognizerContext;
StringCollection theUserDictionary;
//... 
// Initialize theRecognizerContext and theUserDictionary objects here.
//...
WordList theUserWordList = new WordList();
foreach (string s in theUserDictionary)
{
    theUserWordList.Add(s);
}
theRecognizerContext.WordList = theUserWordList;
```



> [!Note]  
> 在您設定 [[**單詞表**](inkwordlist-class.md)] 屬性之前， [**RecognizerCoNtext**](inkrecognizercontext-class.md)物件的 [[**筆劃**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes)] 屬性必須是空的。 如果 [**筆觸**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 屬性不是空的，則會擲回例外狀況。 此外，在將單字指派給 **RecognizerCoNtext** 物件之後，不應該將它們新增至單字清單。 在辨識器中，不會更新在指派給 **RecognizerCoNtext** 物件的單字清單中新增的單字。 若要更新字組清單，您必須將 **單詞表** 物件重新指派給 **RecognizerCoNtext** 物件的 [**單詞表**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)屬性。

 

如需最大辨識精確度，請以有利的關聯性，將 factoids 與您的應用程式字典合併。 如需 factoids 和應用程式字典之間關聯性的詳細資訊，請參閱 [瞭解單字清單、辨識器內容和 factoids](understanding-wordlists--the-recognizercontext--and-factoids.md)。

如需使用應用程式字典搭配 [InkEdit](inkedit-control-reference.md) 控制項的範例，請參閱搭配 [InkEdit 使用應用程式字典](using-an-application-dictionary-with-inkedit.md)。

 

 
