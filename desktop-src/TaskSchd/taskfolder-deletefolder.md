---
title: TaskFolder. DeleteFolder 方法
description: 針對腳本，會從父資料夾刪除子資料夾。
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- DeleteFolder 方法工作排程器
- DeleteFolder 方法工作排程器，TaskFolder 物件
- TaskFolder 物件工作排程器，DeleteFolder 方法
topic_type:
- apiref
api_name:
- TaskFolder.DeleteFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea9b8aaa7da7710cedc49e10d6be2a203f62b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465817"
---
# <a name="taskfolderdeletefolder-method"></a><span data-ttu-id="827af-106">TaskFolder. DeleteFolder 方法</span><span class="sxs-lookup"><span data-stu-id="827af-106">TaskFolder.DeleteFolder method</span></span>

<span data-ttu-id="827af-107">針對腳本，會從父資料夾刪除子資料夾。</span><span class="sxs-lookup"><span data-stu-id="827af-107">For scripting, deletes a subfolder from the parent folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="827af-108">語法</span><span class="sxs-lookup"><span data-stu-id="827af-108">Syntax</span></span>


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="827af-109">參數</span><span class="sxs-lookup"><span data-stu-id="827af-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="827af-110">*資料夾資料夾* \[在\]</span><span class="sxs-lookup"><span data-stu-id="827af-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="827af-111">要移除之子資料夾的名稱。</span><span class="sxs-lookup"><span data-stu-id="827af-111">The name of the subfolder to be removed.</span></span> <span data-ttu-id="827af-112">根工作資料夾是以反斜線 (指定 \) 。</span><span class="sxs-lookup"><span data-stu-id="827af-112">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="827af-113">這個參數可以是您想要刪除之資料夾的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="827af-113">This parameter can be a relative path to the folder you want to delete.</span></span> <span data-ttu-id="827af-114">根工作資料夾下的工作資料夾路徑範例是 \\ MyTaskFolder。</span><span class="sxs-lookup"><span data-stu-id="827af-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="827af-115">'. ' 字元不能用來指定目前的工作資料夾與 ' ... '</span><span class="sxs-lookup"><span data-stu-id="827af-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="827af-116">字元不能用來指定路徑中的父工作資料夾。</span><span class="sxs-lookup"><span data-stu-id="827af-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="827af-117">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="827af-117">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="827af-118">不支援。</span><span class="sxs-lookup"><span data-stu-id="827af-118">Not supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="827af-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="827af-119">Return value</span></span>

<span data-ttu-id="827af-120">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="827af-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="827af-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="827af-121">Requirements</span></span>



| <span data-ttu-id="827af-122">需求</span><span class="sxs-lookup"><span data-stu-id="827af-122">Requirement</span></span> | <span data-ttu-id="827af-123">值</span><span class="sxs-lookup"><span data-stu-id="827af-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="827af-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="827af-124">Minimum supported client</span></span><br/> | <span data-ttu-id="827af-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="827af-125">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="827af-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="827af-126">Minimum supported server</span></span><br/> | <span data-ttu-id="827af-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="827af-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="827af-128">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="827af-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="827af-129"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="827af-129"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="827af-130">DLL</span><span class="sxs-lookup"><span data-stu-id="827af-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="827af-131"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="827af-131"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="827af-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="827af-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="827af-133">**TaskFolder**</span><span class="sxs-lookup"><span data-stu-id="827af-133">**TaskFolder**</span></span>](taskfolder.md)
</dt> <dt>

[<span data-ttu-id="827af-134">工作排程器</span><span class="sxs-lookup"><span data-stu-id="827af-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





