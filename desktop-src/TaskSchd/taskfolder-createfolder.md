---
title: TaskFolder. CreateFolder 方法
description: 針對腳本，建立相關工作的資料夾。
ms.assetid: 4fdc96bc-8c85-4b36-b3ea-bad7a46c3d35
keywords:
- CreateFolder 方法工作排程器
- CreateFolder 方法工作排程器，TaskFolder 物件
- TaskFolder 物件工作排程器，CreateFolder 方法
topic_type:
- apiref
api_name:
- TaskFolder.CreateFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a873ef59ea9d099a7a739e5238c722f4b908fd
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387076"
---
# <a name="taskfoldercreatefolder-method"></a><span data-ttu-id="3d30c-106">TaskFolder. CreateFolder 方法</span><span class="sxs-lookup"><span data-stu-id="3d30c-106">TaskFolder.CreateFolder method</span></span>

<span data-ttu-id="3d30c-107">針對腳本，建立相關工作的資料夾。</span><span class="sxs-lookup"><span data-stu-id="3d30c-107">For scripting, creates a folder for related tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d30c-108">語法</span><span class="sxs-lookup"><span data-stu-id="3d30c-108">Syntax</span></span>


```VB
ppFolder = .CreateFolder( _
  ByVal folderName, _
  ByVal sddl _
)
```



## <a name="parameters"></a><span data-ttu-id="3d30c-109">參數</span><span class="sxs-lookup"><span data-stu-id="3d30c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d30c-110">*資料夾資料夾* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d30c-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d30c-111">用來識別資料夾的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d30c-111">The name that is used to identify the folder.</span></span> <span data-ttu-id="3d30c-112">如果指定了 " \\ SubFolder1 \\ SubFolder2"，則如果資料夾不存在，就會建立整個資料夾樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="3d30c-112">If "FolderName\\SubFolder1\\SubFolder2" is specified, the entire folder tree will be created if the folders do not exist.</span></span> <span data-ttu-id="3d30c-113">這個參數可以是目前 [**TaskFolder**](taskfolder.md) 實例的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="3d30c-113">This parameter can be a relative path to the current [**TaskFolder**](taskfolder.md) instance.</span></span> <span data-ttu-id="3d30c-114">根工作資料夾是以反斜線 () 指定 \\ 。</span><span class="sxs-lookup"><span data-stu-id="3d30c-114">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="3d30c-115">根工作資料夾下的工作資料夾路徑範例是 \\ MyTaskFolder。</span><span class="sxs-lookup"><span data-stu-id="3d30c-115">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="3d30c-116">'. ' 字元不能用來指定目前的工作資料夾與 ' ... '</span><span class="sxs-lookup"><span data-stu-id="3d30c-116">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="3d30c-117">字元不能用來指定路徑中的父工作資料夾。</span><span class="sxs-lookup"><span data-stu-id="3d30c-117">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="3d30c-118">*sddl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d30c-118">*sddl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d30c-119">與資料夾相關聯的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="3d30c-119">The security descriptor that is associated with the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d30c-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="3d30c-120">Return value</span></span>

<span data-ttu-id="3d30c-121">[**TaskFolder**](taskfolder.md)物件，表示新的子資料夾。</span><span class="sxs-lookup"><span data-stu-id="3d30c-121">A [**TaskFolder**](taskfolder.md) object that represents the new subfolder.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d30c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d30c-122">Requirements</span></span>



| <span data-ttu-id="3d30c-123">需求</span><span class="sxs-lookup"><span data-stu-id="3d30c-123">Requirement</span></span> | <span data-ttu-id="3d30c-124">值</span><span class="sxs-lookup"><span data-stu-id="3d30c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d30c-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d30c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3d30c-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d30c-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3d30c-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d30c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3d30c-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3d30c-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3d30c-129">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="3d30c-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="3d30c-130"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3d30c-130"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3d30c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3d30c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d30c-132"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d30c-132"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d30c-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d30c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d30c-134">工作排程器</span><span class="sxs-lookup"><span data-stu-id="3d30c-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





