---
description: 剖析器 DLL 的架構必須提供下圖所示的功能。
ms.assetid: 2da5d4bc-a219-47b5-8522-1237f7bcac16
title: 剖析器 DLL 架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7852029a892d8b74c954cbc2d7341fcaf29032fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469513"
---
# <a name="parser-dll-architecture"></a><span data-ttu-id="71ee2-103">剖析器 DLL 架構</span><span class="sxs-lookup"><span data-stu-id="71ee2-103">Parser DLL Architecture</span></span>

<span data-ttu-id="71ee2-104">剖析器 DLL 的架構必須提供下圖所示的功能。</span><span class="sxs-lookup"><span data-stu-id="71ee2-104">The architecture of the parser DLL must provide the features shown in the following illustration.</span></span> <span data-ttu-id="71ee2-105">請注意，某些功能只需要執行一個進入點。</span><span class="sxs-lookup"><span data-stu-id="71ee2-105">Be aware that some features require the implementation of only one entry point.</span></span> <span data-ttu-id="71ee2-106">但是，如果您的剖析器 DLL 支援多個通訊協定，則功能需要執行多個進入點。</span><span class="sxs-lookup"><span data-stu-id="71ee2-106">However, if your parser DLL supports multiple protocols, then the feature requires the implementation of multiple entry points.</span></span>

![剖析器 dll 功能](images/parserarchitecture1.png)



| <span data-ttu-id="71ee2-108">如需下列資訊</span><span class="sxs-lookup"><span data-stu-id="71ee2-108">For information about</span></span>                                                  | <span data-ttu-id="71ee2-109">請參閱</span><span class="sxs-lookup"><span data-stu-id="71ee2-109">See</span></span>                                                                    |
|------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="71ee2-110">如何執行剖析器 DLL 匯出函數。</span><span class="sxs-lookup"><span data-stu-id="71ee2-110">How to implement parser DLL export functions.</span></span>                          | [<span data-ttu-id="71ee2-111">撰寫通訊協定剖析器</span><span class="sxs-lookup"><span data-stu-id="71ee2-111">Writing a Protocol Parser</span></span>](writing-a-protocol-parser.md)             |
| <span data-ttu-id="71ee2-112">剖析器使用的特定函式和結構—參考主題。</span><span class="sxs-lookup"><span data-stu-id="71ee2-112">Specific functions and structures that parsers use — reference topics.</span></span> | [<span data-ttu-id="71ee2-113">剖析器函式和結構</span><span class="sxs-lookup"><span data-stu-id="71ee2-113">Parser Functions and Structures</span></span>](parser-functions-and-structures.md) |



 

 

 



