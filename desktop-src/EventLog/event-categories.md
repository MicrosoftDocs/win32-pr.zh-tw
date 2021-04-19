---
description: 類別可協助您組織事件，讓事件檢視器可以進行篩選。 每個事件來源都可以定義自己的編號類別以及它們所對應的文字字串。
ms.assetid: ddba8066-b6b9-42a6-b49f-cbae8f97ef6d
title: 事件類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd84a095754bd51499edf5a21ebea0ade042d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972275"
---
# <a name="event-categories"></a><span data-ttu-id="f6b0d-104">事件類別</span><span class="sxs-lookup"><span data-stu-id="f6b0d-104">Event Categories</span></span>

<span data-ttu-id="f6b0d-105">類別可協助您組織事件，讓事件檢視器可以進行篩選。</span><span class="sxs-lookup"><span data-stu-id="f6b0d-105">Categories help you organize events so Event Viewer can filter them.</span></span> <span data-ttu-id="f6b0d-106">每個 [事件來源](event-sources.md) 都可以定義自己的編號類別以及它們所對應的文字字串。</span><span class="sxs-lookup"><span data-stu-id="f6b0d-106">Each [event source](event-sources.md) can define its own numbered categories and the text strings to which they are mapped.</span></span>

<span data-ttu-id="f6b0d-107">類別必須連續編號，以數位1為開頭。</span><span class="sxs-lookup"><span data-stu-id="f6b0d-107">The categories must be numbered consecutively, beginning with the number 1.</span></span> <span data-ttu-id="f6b0d-108">類別本身會定義在訊息檔案中。</span><span class="sxs-lookup"><span data-stu-id="f6b0d-108">The categories themselves are defined in a message file.</span></span> <span data-ttu-id="f6b0d-109">例如，使用下列語法來宣告三個事件類別目錄。</span><span class="sxs-lookup"><span data-stu-id="f6b0d-109">For example, use the following syntax to declare three event categories.</span></span> <span data-ttu-id="f6b0d-110">在事件檢視器中，使用這些分類的事件將會在 [ **類別目錄** ] 資料行中顯示類別1、類別2或類別3。</span><span class="sxs-lookup"><span data-stu-id="f6b0d-110">In Event Viewer, the events that use these categories will have Category 1, Category 2, or Category 3 displayed in the **Category** column.</span></span>

``` syntax
MessageId=0x1
SymbolicName=CATEGORY_1
Language=English
Category 1
.

MessageId=0x2
SymbolicName=CATEGORY_2
Language=English
Category 2
.

MessageId=0x3
SymbolicName=CATEGORY_3
Language=English
Category 3
.
```

<span data-ttu-id="f6b0d-111">類別可以儲存在個別的訊息檔案中，或是儲存在包含其他類型訊息的檔案中。</span><span class="sxs-lookup"><span data-stu-id="f6b0d-111">Categories can be stored in a separate message file, or in a file that contains messages of other types.</span></span> <span data-ttu-id="f6b0d-112">如果您建立單一訊息檔案，請確定類別是檔案中的第一則訊息。</span><span class="sxs-lookup"><span data-stu-id="f6b0d-112">If you create a single message file, be sure that the categories are the first messages in the file.</span></span> <span data-ttu-id="f6b0d-113">如需建立和使用訊息檔案的詳細資訊，請參閱 [訊息](message-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="f6b0d-113">For more information on creating and using message files, see [Message Files](message-files.md).</span></span>

<span data-ttu-id="f6b0d-114">類別目錄總數會儲存在事件來源的 **CategoryCount** 值中。</span><span class="sxs-lookup"><span data-stu-id="f6b0d-114">The total number of categories is stored in the **CategoryCount** value for the event source.</span></span>

 

 



