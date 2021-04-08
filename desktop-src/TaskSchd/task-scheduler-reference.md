---
title: 工作排程器參考
description: 本節說明工作排程器所提供的 Api、腳本物件和 XML 架構。
ms.assetid: e3b5a1e1-4d18-44b7-aaa6-ebec11892bec
keywords:
- 工作排程器工作排程器，參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb22306266054b8ec19a90f188c43e5eb7e4393b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673239"
---
# <a name="task-scheduler-reference"></a><span data-ttu-id="e432c-104">工作排程器參考</span><span class="sxs-lookup"><span data-stu-id="e432c-104">Task Scheduler Reference</span></span>

<span data-ttu-id="e432c-105">本節說明工作排程器所提供的 Api、腳本物件和 XML 架構。</span><span class="sxs-lookup"><span data-stu-id="e432c-105">This section describes the APIs, scripting objects, and XML schema that are provided by the Task Scheduler.</span></span>

<span data-ttu-id="e432c-106">API 主題包含 API 的描述、API 的宣告語法、描述 API 特殊條件的備註，以及描述需要哪些平臺、標頭檔和程式庫的需求區塊。</span><span class="sxs-lookup"><span data-stu-id="e432c-106">API topics include a description of the API, the declaration syntax of the API, remarks that describe special conditions for the API, and a requirements block that describes what platform, header files, and libraries are required.</span></span>

<span data-ttu-id="e432c-107">腳本物件主題包含物件的描述、物件的宣告語法、描述物件特殊條件的備註，以及描述所需的平臺和類型程式庫的需求區塊。</span><span class="sxs-lookup"><span data-stu-id="e432c-107">Scripting object topics include a description of the object, the declaration syntax of the object, remarks that describe special conditions for the object, and a requirements block that describes what platform and type libraries are required.</span></span>

<span data-ttu-id="e432c-108">XML 架構主題包含元素、父系、子系和屬性資訊的描述，以及描述特殊條件的備註。</span><span class="sxs-lookup"><span data-stu-id="e432c-108">XML schema topics include a description of the element, parent, child, and attribute information, and remarks that describe special conditions.</span></span>



| <span data-ttu-id="e432c-109">請參閱</span><span class="sxs-lookup"><span data-stu-id="e432c-109">See</span></span>                                                                                          | <span data-ttu-id="e432c-110">如需相關資訊</span><span class="sxs-lookup"><span data-stu-id="e432c-110">For information on</span></span>                                                                                                                            |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e432c-111">工作排程器物件</span><span class="sxs-lookup"><span data-stu-id="e432c-111">Task Scheduler Objects</span></span>](task-scheduler-objects.md)                                         | <span data-ttu-id="e432c-112">編寫物件及其方法和屬性的腳本。</span><span class="sxs-lookup"><span data-stu-id="e432c-112">Scripting objects and their methods and properties.</span></span>                                                                                           |
| [<span data-ttu-id="e432c-113">工作排程器介面</span><span class="sxs-lookup"><span data-stu-id="e432c-113">Task Scheduler Interfaces</span></span>](task-scheduler-interfaces.md)                                   | <span data-ttu-id="e432c-114">介面及其方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="e432c-114">Interfaces and their methods and properties.</span></span>                                                                                                  |
| [<span data-ttu-id="e432c-115">工作排程器結構和等位</span><span class="sxs-lookup"><span data-stu-id="e432c-115">Task Scheduler Structures and Unions</span></span>](task-scheduler-structures-and-unions.md)             | <span data-ttu-id="e432c-116">結構和等位。</span><span class="sxs-lookup"><span data-stu-id="e432c-116">Structures and unions.</span></span>                                                                                                                        |
| [<span data-ttu-id="e432c-117">工作排程器列舉類型</span><span class="sxs-lookup"><span data-stu-id="e432c-117">Task Scheduler Enumerated Types</span></span>](task-scheduler-enumerated-types.md)                       | <span data-ttu-id="e432c-118">枚舉器定義的常數。</span><span class="sxs-lookup"><span data-stu-id="e432c-118">Constants defined by enumerators.</span></span>                                                                                                             |
| [<span data-ttu-id="e432c-119">工作排程器架構</span><span class="sxs-lookup"><span data-stu-id="e432c-119">Task Scheduler Schema</span></span>](task-scheduler-schema.md)                                           | <span data-ttu-id="e432c-120">由架構定義的元素、簡單類型、複雜類型和屬性群組。</span><span class="sxs-lookup"><span data-stu-id="e432c-120">Elements, simple types, complex types, and attribute groups defined by the schema.</span></span>                                                            |
| [<span data-ttu-id="e432c-121">工作排程器錯誤和成功常數</span><span class="sxs-lookup"><span data-stu-id="e432c-121">Task Scheduler Error and Success Constants</span></span>](task-scheduler-error-and-success-constants.md) | <span data-ttu-id="e432c-122">工作排程器 Api 所傳回的錯誤和成功常數。</span><span class="sxs-lookup"><span data-stu-id="e432c-122">Error and success constants returned by Task Scheduler APIs.</span></span>                                                                                  |
| [<span data-ttu-id="e432c-123">**Schtasks.exe**</span><span class="sxs-lookup"><span data-stu-id="e432c-123">**Schtasks.exe**</span></span>](schtasks.md)                                                             | <span data-ttu-id="e432c-124">Schtasks.exe 命令列工具，可用來在本機或遠端電腦上建立、刪除、查詢、變更、執行和結束排定的工作。</span><span class="sxs-lookup"><span data-stu-id="e432c-124">The Schtasks.exe command line tool that is used to create, delete, query, change, run, and end scheduled tasks on a local or remote computer.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e432c-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="e432c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e432c-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="e432c-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 




