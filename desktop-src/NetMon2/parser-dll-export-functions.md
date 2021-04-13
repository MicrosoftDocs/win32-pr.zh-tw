---
description: 下表所列的函式是剖析器 Dll 的進入點。 這些函式是從作業系統和網路監視器呼叫的進入點。
ms.assetid: 67811ddb-1961-4306-a62f-b9fd2d2d2b55
title: 剖析器 DLL 匯出函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929541a1eda60740fe219352fee285a5a34a89df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386098"
---
# <a name="parser-dll-export-functions"></a><span data-ttu-id="98a27-104">剖析器 DLL 匯出函數</span><span class="sxs-lookup"><span data-stu-id="98a27-104">Parser DLL Export Functions</span></span>

<span data-ttu-id="98a27-105">下表所列的函式是剖析器 Dll 的進入點。</span><span class="sxs-lookup"><span data-stu-id="98a27-105">The functions, listed in the following table, are entry points for parser DLLs.</span></span> <span data-ttu-id="98a27-106">這些函式是從作業系統和網路監視器呼叫的進入點。</span><span class="sxs-lookup"><span data-stu-id="98a27-106">The functions are the entry points for calls from the operating system and Network Monitor.</span></span>



| <span data-ttu-id="98a27-107">函式</span><span class="sxs-lookup"><span data-stu-id="98a27-107">Function</span></span>                                           | <span data-ttu-id="98a27-108">描述</span><span class="sxs-lookup"><span data-stu-id="98a27-108">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98a27-109">DllMain 剖析器</span><span class="sxs-lookup"><span data-stu-id="98a27-109">DllMain Parser</span></span>](dllmain-parser.md)               | <span data-ttu-id="98a27-110">指示剖析器 DLL 載入或卸載它。</span><span class="sxs-lookup"><span data-stu-id="98a27-110">Indicates to the parser DLL that it is loaded or unloaded.</span></span> <span data-ttu-id="98a27-111">當進程載入或卸載 DLL 時，作業系統會呼叫 **DllMain** 剖析器函式。</span><span class="sxs-lookup"><span data-stu-id="98a27-111">The operating system calls the **DllMain Parser** function when a process loads or unloads the DLL.</span></span> |
| [<span data-ttu-id="98a27-112">AttachProperties</span><span class="sxs-lookup"><span data-stu-id="98a27-112">AttachProperties</span></span>](attachproperties.md)           | <span data-ttu-id="98a27-113">通知剖析器附加存在於框架中的任何屬性。</span><span class="sxs-lookup"><span data-stu-id="98a27-113">Notifies the parser to attach any properties that exist in a frame.</span></span>                                                                                            |
| [<span data-ttu-id="98a27-114">取消註冊</span><span class="sxs-lookup"><span data-stu-id="98a27-114">Deregister</span></span>](deregister.md)                       | <span data-ttu-id="98a27-115">通知剖析器清除。</span><span class="sxs-lookup"><span data-stu-id="98a27-115">Notifies the parser to clean up.</span></span>                                                                                                                               |
| [<span data-ttu-id="98a27-116">FormatProperties</span><span class="sxs-lookup"><span data-stu-id="98a27-116">FormatProperties</span></span>](formatproperties.md)           | <span data-ttu-id="98a27-117">通知剖析器取得中的所有屬性實例，並建立每個 **PROPERTYINST** 結構的 **szPropertyText** 成員。</span><span class="sxs-lookup"><span data-stu-id="98a27-117">Notifies the parser to take all of the property instances in and build the **szPropertyText** member of each **PROPERTYINST** structure.</span></span>                       |
| [<span data-ttu-id="98a27-118">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="98a27-118">RecognizeFrame</span></span>](recognizeframe.md)               | <span data-ttu-id="98a27-119">判斷剖析器是否可以使用指定的通訊協定來解讀未處理的框架資料。</span><span class="sxs-lookup"><span data-stu-id="98a27-119">Determines whether the parser can interpret the unprocessed frame data with the specified protocol.</span></span>                                                            |
| [<span data-ttu-id="98a27-120">註冊剖析器</span><span class="sxs-lookup"><span data-stu-id="98a27-120">Register Parser</span></span>](register-parser.md)             | <span data-ttu-id="98a27-121">判斷 DLL 內剖析器的基本資訊。</span><span class="sxs-lookup"><span data-stu-id="98a27-121">Determines basic information about the parser within the DLL.</span></span> <span data-ttu-id="98a27-122">網路監視器會呼叫 **Register** 剖析器函數。</span><span class="sxs-lookup"><span data-stu-id="98a27-122">Network Monitor calls the **Register Parser** function.</span></span>                                          |
| [<span data-ttu-id="98a27-123">ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="98a27-123">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md) | <span data-ttu-id="98a27-124">自動安裝剖析器。</span><span class="sxs-lookup"><span data-stu-id="98a27-124">Installs a parser automatically.</span></span>                                                                                                                               |



 

<span data-ttu-id="98a27-125">網路監視器提供剖析器可呼叫的結構和 helper 函數。</span><span class="sxs-lookup"><span data-stu-id="98a27-125">Network Monitor provides structures and helper functions that the parser can call.</span></span>



| <span data-ttu-id="98a27-126">如需下列項目的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="98a27-126">For more information about</span></span>                          | <span data-ttu-id="98a27-127">請參閱</span><span class="sxs-lookup"><span data-stu-id="98a27-127">See</span></span>                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="98a27-128">專家和剖析器可以呼叫的協助程式函數。</span><span class="sxs-lookup"><span data-stu-id="98a27-128">Helper functions that experts and parsers can call.</span></span> | [<span data-ttu-id="98a27-129">專家和剖析器一般函數</span><span class="sxs-lookup"><span data-stu-id="98a27-129">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |
| <span data-ttu-id="98a27-130">只有剖析器可以呼叫的 Helper 函數。</span><span class="sxs-lookup"><span data-stu-id="98a27-130">Helper functions that only parsers can call.</span></span>        | [<span data-ttu-id="98a27-131">剖析器函式</span><span class="sxs-lookup"><span data-stu-id="98a27-131">Parser Functions</span></span>](parser-functions.md)                                     |
| <span data-ttu-id="98a27-132">剖析器函數使用的結構。</span><span class="sxs-lookup"><span data-stu-id="98a27-132">Structures that parser functions use.</span></span>               | [<span data-ttu-id="98a27-133">剖析器結構</span><span class="sxs-lookup"><span data-stu-id="98a27-133">Parser Structures</span></span>](parser-structures.md)                                   |



 

 

 



