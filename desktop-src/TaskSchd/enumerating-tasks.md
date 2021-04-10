---
title: 列舉工作
description: 工作排程器1.0 提供列舉物件來列舉 [排定的工作] 資料夾中的工作。
ms.assetid: ccd140a1-06f6-4e6b-afa6-f7ac9b9ff904
keywords:
- 列舉工作工作排程器
- 列舉工作工作排程器，說明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dda98cf40bc1ea360d20bcf13084faa692aa22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021743"
---
# <a name="enumerating-tasks"></a><span data-ttu-id="23c08-105">列舉工作</span><span class="sxs-lookup"><span data-stu-id="23c08-105">Enumerating Tasks</span></span>

<span data-ttu-id="23c08-106">工作排程器1.0 提供列舉物件來列舉 [排定的工作] [*資料夾*](s.md)中的工作。</span><span class="sxs-lookup"><span data-stu-id="23c08-106">Task Scheduler 1.0 provides an enumeration object for enumerating the tasks in the [*Scheduled Tasks folder*](s.md).</span></span>

> [!Note]  
> <span data-ttu-id="23c08-107">若為 Windows Server 2003、Windows XP 或 Windows 2000 電腦，可在 Windows Vista 電腦上建立、監視或控制工作，則必須在 Windows Vista 電腦上完成某些作業。</span><span class="sxs-lookup"><span data-stu-id="23c08-107">For a Windows Server 2003, Windows XP, or Windows 2000 computer to create, monitor, or control tasks on a Windows Vista computer, certain operations must be completed on the Windows Vista computer.</span></span> <span data-ttu-id="23c08-108">如需詳細資訊，請參閱[工作](tasks.md)。</span><span class="sxs-lookup"><span data-stu-id="23c08-108">For more information, see [Tasks](tasks.md).</span></span>

 

## <a name="using-the-enumeration-object"></a><span data-ttu-id="23c08-109">使用列舉物件</span><span class="sxs-lookup"><span data-stu-id="23c08-109">Using the Enumeration Object</span></span>

<span data-ttu-id="23c08-110">這個物件的 [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) 介面會提供方法來列舉資料夾中的工作、將列舉順序重設為清單的開頭、略過工作，以及建立目前列舉物件的複本以供稍後使用。</span><span class="sxs-lookup"><span data-stu-id="23c08-110">The [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) interface of this object provides methods for enumerating the tasks in the folder, resetting the enumeration sequence to the start of the list, skipping tasks, and making a copy of the current enumeration object for later use.</span></span>

<span data-ttu-id="23c08-111">如需列舉 [排定的工作] 資料夾中之工作的詳細資訊，請參閱 [**IEnumWorkItems：： Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next)。</span><span class="sxs-lookup"><span data-stu-id="23c08-111">For information about enumerating the tasks in the Scheduled tasks folder, see [**IEnumWorkItems::Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next).</span></span>

<span data-ttu-id="23c08-112">如需將列舉值重設為清單開頭的詳細資訊，請參閱 [**IEnumWorkItems：： Reset**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset)。</span><span class="sxs-lookup"><span data-stu-id="23c08-112">For information about resetting the enumeration to the start of the list, see [**IEnumWorkItems::Reset**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset).</span></span>

<span data-ttu-id="23c08-113">如需略過工作的詳細資訊，請參閱 [**IEnumWorkItems：： Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip)。</span><span class="sxs-lookup"><span data-stu-id="23c08-113">For information about skipping tasks, see [**IEnumWorkItems::Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip).</span></span>

<span data-ttu-id="23c08-114">如需建立目前列舉物件複本的詳細資訊，請參閱 [**IEnumWorkItems：： Clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone)。</span><span class="sxs-lookup"><span data-stu-id="23c08-114">For information about making a copy of the current enumeration object, see [**IEnumWorkItems::Clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone).</span></span>

<span data-ttu-id="23c08-115">如需列舉 [排定的工作] 資料夾中之工作的範例，請參閱 [列舉工作範例](enumerating-tasks-example.md)。</span><span class="sxs-lookup"><span data-stu-id="23c08-115">For an example of enumerating the tasks in the Scheduled Tasks folder, see [Enumerating Tasks Example](enumerating-tasks-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="23c08-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="23c08-116">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="23c08-117">**概念**</span><span class="sxs-lookup"><span data-stu-id="23c08-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="23c08-118">工作排程器1.0 工作資訊</span><span class="sxs-lookup"><span data-stu-id="23c08-118">Task Scheduler 1.0 Task Information</span></span>](task-scheduler-1-0-task-informatation.md)
</dt> </dl>

 

 




