---
description: 根據預設，辨識器會使用系統字典，其中包含所有常用的語言文字。
ms.assetid: 2ddf04dd-613b-4570-9474-0e33208c4012
title: 使用應用程式字典
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74dfda443a688af9dfcec44a81f0e5ed2d50846c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468980"
---
# <a name="using-application-dictionaries"></a><span data-ttu-id="28937-103">使用應用程式字典</span><span class="sxs-lookup"><span data-stu-id="28937-103">Using Application Dictionaries</span></span>

<span data-ttu-id="28937-104">根據預設，辨識器會使用系統字典，其中包含所有常用的語言文字。</span><span class="sxs-lookup"><span data-stu-id="28937-104">By default, the recognizer uses a system dictionary that contains all of the commonly written words in a language.</span></span> <span data-ttu-id="28937-105">此外，辨識器具有使用者字典，其中包含使用者已新增至字典的單字。</span><span class="sxs-lookup"><span data-stu-id="28937-105">In addition, the recognizer has a user dictionary that contains words that the user has added to the dictionary.</span></span> <span data-ttu-id="28937-106">使用者可以透過 [Tablet PC 輸入面板]，透過 [Tablet PC 輸入面板]，透過 [Tablet PC 輸入面板] 將</span><span class="sxs-lookup"><span data-stu-id="28937-106">Users add a word to the user dictionary through Tablet PC Input Panel through selections in:</span></span>

-   <span data-ttu-id="28937-107">寫入) 時 (替代清單。</span><span class="sxs-lookup"><span data-stu-id="28937-107">The alternate list (when writing).</span></span>
-   <span data-ttu-id="28937-108">語音工具功能表 (說話) 。</span><span class="sxs-lookup"><span data-stu-id="28937-108">The Speech Tools menu (when speaking).</span></span>

<span data-ttu-id="28937-109">如果您要設計應用程式，讓使用者能夠撰寫在系統字典或使用者字典中找不到的單字，請建立應用程式字典。</span><span class="sxs-lookup"><span data-stu-id="28937-109">If you are designing an application into which you anticipate the user will write words that are not found in either the system dictionary or the user dictionary, create an application dictionary.</span></span> <span data-ttu-id="28937-110">應用程式字典提供辨識器額外的自訂字詞清單，可能會以手寫形式輸入到應用程式中，藉此提升辨識準確度。</span><span class="sxs-lookup"><span data-stu-id="28937-110">An application dictionary further improves recognition accuracy by providing the recognizer with an additional customized list of words likely to be entered as handwriting into an application.</span></span>

<span data-ttu-id="28937-111">您可以使用 [**單詞表**](inkwordlist-class.md) 物件來建立應用程式字典。</span><span class="sxs-lookup"><span data-stu-id="28937-111">You create an application dictionary by using the [**WordList**](inkwordlist-class.md) object.</span></span> <span data-ttu-id="28937-112">後續的應用程式字典藉由提供辨識器與預期的單字清單來增加辨識精確度。</span><span class="sxs-lookup"><span data-stu-id="28937-112">The ensuing application dictionary increases recognition accuracy by providing the recognizer with a list of expected words.</span></span> <span data-ttu-id="28937-113">例如，包含醫學術語的應用程式字典會在針對醫療產業開發的應用程式中增加辨識精確度，而該應用程式可能會撰寫詞彙。</span><span class="sxs-lookup"><span data-stu-id="28937-113">For example, an application dictionary that contains medical terminology increases recognition accuracy within an application developed for the medical industry into which the terms are likely to be written.</span></span>

<span data-ttu-id="28937-114">另一個例子是，當您設計表單以訂購音樂器材時，請建立一個包含最常見檢測製造商名稱的 [**單詞表**](inkwordlist-class.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="28937-114">As another example, when designing a form for someone to order musical instruments, create a [**WordList**](inkwordlist-class.md) object that contains the names of the most common instrument manufacturers.</span></span> <span data-ttu-id="28937-115">將 [**RecognizerCoNtext**](inkrecognizercontext-class.md)物件的 [[**單詞表**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)] 屬性設定為您所建立的 **單詞表** 物件。</span><span class="sxs-lookup"><span data-stu-id="28937-115">Set the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object to the **WordList** object you created.</span></span> <span data-ttu-id="28937-116">然後， **RecognizerCoNtext** 物件會將這份單字清單傳遞給辨識器。</span><span class="sxs-lookup"><span data-stu-id="28937-116">This list of words is then passed to the recognizer by the **RecognizerContext** object.</span></span> <span data-ttu-id="28937-117">應用程式字典會在應用程式中的欄位寫入這些名稱時，增加辨識精確度。</span><span class="sxs-lookup"><span data-stu-id="28937-117">The application dictionary increases recognition accuracy when those names are written in a field in the application.</span></span>

<span data-ttu-id="28937-118">下列主題描述如何使用應用程式字典。</span><span class="sxs-lookup"><span data-stu-id="28937-118">The following topics describe how to use application dictionaries.</span></span>

-   [<span data-ttu-id="28937-119">瞭解單字清單、辨識器內容和 Factoids</span><span class="sxs-lookup"><span data-stu-id="28937-119">Understanding Word Lists, Recognizer Context, and Factoids</span></span>](understanding-wordlists--the-recognizercontext--and-factoids.md)
-   [<span data-ttu-id="28937-120">使用應用程式字典搭配 Tablet PC 平臺 Api</span><span class="sxs-lookup"><span data-stu-id="28937-120">Using Application Dictionaries with the Tablet PC Platform APIs</span></span>](using-application-dictionaries-with-the-tablet-pc-platform-apis.md)
-   [<span data-ttu-id="28937-121">建立手寫辨識的自訂字典</span><span class="sxs-lookup"><span data-stu-id="28937-121">Creating Custom Dictionaries for Handwriting Recognition</span></span>](creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2.md)

 

 



