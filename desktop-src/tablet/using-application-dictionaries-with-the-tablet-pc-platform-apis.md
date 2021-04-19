---
description: 若要使用應用程式字典搭配 Tablet PC API，您必須先使用應用程式字典的單字清單建立檔案。
ms.assetid: 6abadad1-262b-4536-8846-1c06226dc18a
title: 使用應用程式字典搭配 Tablet PC 平臺 Api
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fc0e444ad2213d945c0210d07c72f9540ae16be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973451"
---
# <a name="using-application-dictionaries-with-the-tablet-pc-platform-apis"></a><span data-ttu-id="94213-103">使用應用程式字典搭配 Tablet PC 平臺 Api</span><span class="sxs-lookup"><span data-stu-id="94213-103">Using Application Dictionaries with the Tablet PC Platform APIs</span></span>

<span data-ttu-id="94213-104">若要使用應用程式字典搭配 Tablet PC API，您必須先使用應用程式字典的單字清單建立檔案。</span><span class="sxs-lookup"><span data-stu-id="94213-104">To use an application dictionary with the Tablet PC API, you must first create a file with the list of words for your application dictionary.</span></span>

<span data-ttu-id="94213-105">最簡單的解決方法是使用包含單字清單的文字檔。</span><span class="sxs-lookup"><span data-stu-id="94213-105">The easiest solution for this is to use a text file that contains a list of the words.</span></span> <span data-ttu-id="94213-106">當您的應用程式載入時，它會讀取文字檔，並從檔案中的單字清單建立 [**單詞表**](inkwordlist-class.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="94213-106">When your application loads, it reads the text file and creates a [**WordList**](inkwordlist-class.md) object from the list of words in the file.</span></span> <span data-ttu-id="94213-107">針對與應用程式字典相關聯的每個 [**RecognizerCoNtext**](inkrecognizercontext-class.md) ，將 **RecognizerCoNtext** 物件的 [[**單詞表**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)] 屬性設定為文字檔中的單字清單。</span><span class="sxs-lookup"><span data-stu-id="94213-107">For each [**RecognizerContext**](inkrecognizercontext-class.md) associated with the application dictionary, set the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the **RecognizerContext** object to the word list in the text file.</span></span>

<span data-ttu-id="94213-108">下列範例說明如何從 [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1)集合建立 [**單詞表**](inkwordlist-class.md)物件。</span><span class="sxs-lookup"><span data-stu-id="94213-108">The following example illustrates how to create a [**WordList**](inkwordlist-class.md) object from a [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) collection.</span></span> <span data-ttu-id="94213-109">此範例假設您已從磁片載入單字清單，並從這些字組建立 StringCollection 集合。</span><span class="sxs-lookup"><span data-stu-id="94213-109">This example assumes that you have already loaded the list of words from disk and created a StringCollection collection from these words.</span></span>


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
> <span data-ttu-id="94213-110">在您設定 [[**單詞表**](inkwordlist-class.md)] 屬性之前， [**RecognizerCoNtext**](inkrecognizercontext-class.md)物件的 [[**筆劃**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes)] 屬性必須是空的。</span><span class="sxs-lookup"><span data-stu-id="94213-110">The [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object must be empty before you set the [**WordList**](inkwordlist-class.md) property.</span></span> <span data-ttu-id="94213-111">如果 [**筆觸**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 屬性不是空的，則會擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="94213-111">If the [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) property is not empty, an exception is thrown.</span></span> <span data-ttu-id="94213-112">此外，在將單字指派給 **RecognizerCoNtext** 物件之後，不應該將它們新增至單字清單。</span><span class="sxs-lookup"><span data-stu-id="94213-112">In addition, words should never be added to a word list after it has been assigned to a **RecognizerContext** object.</span></span> <span data-ttu-id="94213-113">在辨識器中，不會更新在指派給 **RecognizerCoNtext** 物件的單字清單中新增的單字。</span><span class="sxs-lookup"><span data-stu-id="94213-113">Words that are added to the word list after it is assigned to the **RecognizerContext** object are not updated in the recognizer.</span></span> <span data-ttu-id="94213-114">若要更新字組清單，您必須將 **單詞表** 物件重新指派給 **RecognizerCoNtext** 物件的 [**單詞表**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)屬性。</span><span class="sxs-lookup"><span data-stu-id="94213-114">To update the word list you must reassign the **WordList** object to the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the **RecognizerContext** object.</span></span>

 

<span data-ttu-id="94213-115">如需最大辨識精確度，請以有利的關聯性，將 factoids 與您的應用程式字典合併。</span><span class="sxs-lookup"><span data-stu-id="94213-115">For maximum recognition accuracy, combine factoids with your application dictionary in an advantageous relationship.</span></span> <span data-ttu-id="94213-116">如需 factoids 和應用程式字典之間關聯性的詳細資訊，請參閱 [瞭解單字清單、辨識器內容和 factoids](understanding-wordlists--the-recognizercontext--and-factoids.md)。</span><span class="sxs-lookup"><span data-stu-id="94213-116">For more information about the relationship between factoids and application dictionaries, see [Understanding Word Lists, Recognizer Context, and Factoids](understanding-wordlists--the-recognizercontext--and-factoids.md).</span></span>

<span data-ttu-id="94213-117">如需使用應用程式字典搭配 [InkEdit](inkedit-control-reference.md) 控制項的範例，請參閱搭配 [InkEdit 使用應用程式字典](using-an-application-dictionary-with-inkedit.md)。</span><span class="sxs-lookup"><span data-stu-id="94213-117">For an example of using application dictionaries with the [InkEdit](inkedit-control-reference.md) control, see [Using an Application Dictionary with InkEdit](using-an-application-dictionary-with-inkedit.md).</span></span>

 

 
