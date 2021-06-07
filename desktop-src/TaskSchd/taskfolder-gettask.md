---
title: TaskFolder. GetTask 屬性
description: 針對腳本，取得資料夾中位於指定位置的工作。
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- GetTask 屬性工作排程器
- GetTask 屬性工作排程器，TaskFolder 物件
- TaskFolder 物件工作排程器、GetTask 屬性
topic_type:
- apiref
api_name:
- TaskFolder.GetTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b697b8fa2d0715dcf0282c5f32490bfccec79fec
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387674"
---
# <a name="taskfoldergettask-property"></a><span data-ttu-id="89783-106">TaskFolder. GetTask 屬性</span><span class="sxs-lookup"><span data-stu-id="89783-106">TaskFolder.GetTask property</span></span>

<span data-ttu-id="89783-107">針對腳本，取得資料夾中位於指定位置的工作。</span><span class="sxs-lookup"><span data-stu-id="89783-107">For scripting, gets a task at a specified location in a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="89783-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="89783-108">Syntax</span></span>


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="89783-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="89783-109">Property value</span></span>

<span data-ttu-id="89783-110">路徑 (位置) 至資料夾中的工作。</span><span class="sxs-lookup"><span data-stu-id="89783-110">The path (location) to the task in a folder.</span></span> <span data-ttu-id="89783-111">根工作資料夾是以反斜線 () 指定 \\ 。</span><span class="sxs-lookup"><span data-stu-id="89783-111">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="89783-112">根工作資料夾下的工作資料夾路徑範例是 \\ MyTaskFolder。</span><span class="sxs-lookup"><span data-stu-id="89783-112">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="89783-113">'. ' 字元不能用來指定目前的工作資料夾與 ' ... '</span><span class="sxs-lookup"><span data-stu-id="89783-113">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="89783-114">字元不能用來指定路徑中的父工作資料夾。</span><span class="sxs-lookup"><span data-stu-id="89783-114">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="89783-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="89783-115">Error codes</span></span>

<span data-ttu-id="89783-116">指定位置的工作。</span><span class="sxs-lookup"><span data-stu-id="89783-116">The task at the specified location.</span></span> <span data-ttu-id="89783-117">此工作是 [**RegisteredTask**](registeredtask.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="89783-117">The task is a [**RegisteredTask**](registeredtask.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="89783-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="89783-118">Requirements</span></span>



| <span data-ttu-id="89783-119">需求</span><span class="sxs-lookup"><span data-stu-id="89783-119">Requirement</span></span> | <span data-ttu-id="89783-120">值</span><span class="sxs-lookup"><span data-stu-id="89783-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89783-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89783-121">Minimum supported client</span></span><br/> | <span data-ttu-id="89783-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89783-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="89783-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89783-123">Minimum supported server</span></span><br/> | <span data-ttu-id="89783-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89783-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="89783-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="89783-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="89783-126"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="89783-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="89783-127">DLL</span><span class="sxs-lookup"><span data-stu-id="89783-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89783-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89783-128"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





