---
title: TaskFolder 路徑屬性
description: 針對腳本，取得資料夾儲存位置的路徑。
ms.assetid: a0b28527-4875-4fe4-b2dd-08abbdc87ccc
keywords:
- 路徑屬性工作排程器
- Path 屬性工作排程器，TaskFolder 物件
- TaskFolder 物件工作排程器，Path 屬性
topic_type:
- apiref
api_name:
- TaskFolder.Path
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6733c79d19bbb3d55531f05412a8c9263d76eb90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934074"
---
# <a name="taskfolderpath-property"></a><span data-ttu-id="e9169-106">TaskFolder 路徑屬性</span><span class="sxs-lookup"><span data-stu-id="e9169-106">TaskFolder.Path property</span></span>

<span data-ttu-id="e9169-107">針對腳本，取得資料夾儲存位置的路徑。</span><span class="sxs-lookup"><span data-stu-id="e9169-107">For scripting, gets the path to where the folder is stored.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9169-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9169-108">Syntax</span></span>


```VB
TaskFolder.Path As String
```



## <a name="property-value"></a><span data-ttu-id="e9169-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="e9169-109">Property value</span></span>

<span data-ttu-id="e9169-110">資料夾儲存位置的路徑。</span><span class="sxs-lookup"><span data-stu-id="e9169-110">The path to where the folder is stored.</span></span> <span data-ttu-id="e9169-111">根工作資料夾是以反斜線 (指定 \) 。</span><span class="sxs-lookup"><span data-stu-id="e9169-111">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="e9169-112">根工作資料夾下的工作資料夾路徑範例是 \\ MyTaskFolder。</span><span class="sxs-lookup"><span data-stu-id="e9169-112">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9169-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9169-113">Requirements</span></span>



| <span data-ttu-id="e9169-114">需求</span><span class="sxs-lookup"><span data-stu-id="e9169-114">Requirement</span></span> | <span data-ttu-id="e9169-115">值</span><span class="sxs-lookup"><span data-stu-id="e9169-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9169-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9169-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e9169-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9169-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e9169-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9169-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e9169-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9169-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e9169-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e9169-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="e9169-121"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e9169-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e9169-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e9169-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9169-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9169-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9169-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9169-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9169-125">工作排程器</span><span class="sxs-lookup"><span data-stu-id="e9169-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





