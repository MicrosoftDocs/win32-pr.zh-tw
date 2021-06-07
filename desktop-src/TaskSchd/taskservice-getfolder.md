---
title: TaskService. GetFolder 方法
description: 針對腳本，會取得已註冊工作的資料夾。
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- GetFolder 方法工作排程器
- GetFolder 方法工作排程器，TaskService 物件
- TaskService 物件工作排程器，GetFolder 方法
topic_type:
- apiref
api_name:
- TaskService.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e58f2d930a0577b6f1be620891b7ba631f18d77
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387097"
---
# <a name="taskservicegetfolder-method"></a><span data-ttu-id="b1d10-106">TaskService. GetFolder 方法</span><span class="sxs-lookup"><span data-stu-id="b1d10-106">TaskService.GetFolder method</span></span>

<span data-ttu-id="b1d10-107">針對腳本，會取得已註冊工作的資料夾。</span><span class="sxs-lookup"><span data-stu-id="b1d10-107">For scripting, gets a folder of registered tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1d10-108">語法</span><span class="sxs-lookup"><span data-stu-id="b1d10-108">Syntax</span></span>


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a><span data-ttu-id="b1d10-109">參數</span><span class="sxs-lookup"><span data-stu-id="b1d10-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1d10-110">*路徑* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b1d10-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1d10-111">要抓取之資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="b1d10-111">The path to the folder to be retrieved.</span></span> <span data-ttu-id="b1d10-112">請勿在路徑中的最後一個資料夾名稱後面使用反斜線。</span><span class="sxs-lookup"><span data-stu-id="b1d10-112">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="b1d10-113">根工作資料夾是以反斜線 () 指定 \\ 。</span><span class="sxs-lookup"><span data-stu-id="b1d10-113">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="b1d10-114">根工作資料夾下的工作資料夾路徑範例是 \\ MyTaskFolder。</span><span class="sxs-lookup"><span data-stu-id="b1d10-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="b1d10-115">'. ' 字元不能用來指定目前的工作資料夾與 ' ... '</span><span class="sxs-lookup"><span data-stu-id="b1d10-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="b1d10-116">字元不能用來指定路徑中的父工作資料夾。</span><span class="sxs-lookup"><span data-stu-id="b1d10-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1d10-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="b1d10-117">Return value</span></span>

<span data-ttu-id="b1d10-118">所要求之資料夾的 [**TaskFolder**](taskfolder.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="b1d10-118">A [**TaskFolder**](taskfolder.md) object for the requested folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1d10-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1d10-119">Requirements</span></span>



| <span data-ttu-id="b1d10-120">需求</span><span class="sxs-lookup"><span data-stu-id="b1d10-120">Requirement</span></span> | <span data-ttu-id="b1d10-121">值</span><span class="sxs-lookup"><span data-stu-id="b1d10-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1d10-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b1d10-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b1d10-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1d10-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b1d10-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b1d10-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b1d10-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b1d10-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b1d10-126">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="b1d10-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="b1d10-127"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b1d10-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b1d10-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b1d10-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1d10-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1d10-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1d10-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1d10-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1d10-131">工作排程器</span><span class="sxs-lookup"><span data-stu-id="b1d10-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





