---
title: TaskFolder. GetFolder 屬性
description: 針對腳本，取得包含指定位置之工作的資料夾。
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- GetFolder 屬性工作排程器
- GetFolder 屬性工作排程器，TaskFolder 物件
- TaskFolder 物件工作排程器、GetFolder 屬性
topic_type:
- apiref
api_name:
- TaskFolder.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c65b3f50cc5b8ab75bb041a61b36ad66bb35891
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387027"
---
# <a name="taskfoldergetfolder-property"></a><span data-ttu-id="59dbd-106">TaskFolder. GetFolder 屬性</span><span class="sxs-lookup"><span data-stu-id="59dbd-106">TaskFolder.GetFolder property</span></span>

<span data-ttu-id="59dbd-107">針對腳本，取得包含指定位置之工作的資料夾。</span><span class="sxs-lookup"><span data-stu-id="59dbd-107">For scripting, gets a folder that contains tasks at a specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="59dbd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="59dbd-108">Syntax</span></span>


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="59dbd-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="59dbd-109">Property value</span></span>

<span data-ttu-id="59dbd-110">資料夾) 路徑 (位置。</span><span class="sxs-lookup"><span data-stu-id="59dbd-110">The path (location) to the folder.</span></span> <span data-ttu-id="59dbd-111">請勿在路徑中的最後一個資料夾名稱後面使用反斜線。</span><span class="sxs-lookup"><span data-stu-id="59dbd-111">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="59dbd-112">根工作資料夾是以反斜線 () 指定 \\ 。</span><span class="sxs-lookup"><span data-stu-id="59dbd-112">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="59dbd-113">根工作資料夾下的工作資料夾路徑範例是 \\ MyTaskFolder。</span><span class="sxs-lookup"><span data-stu-id="59dbd-113">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="59dbd-114">'. ' 字元不能用來指定目前的工作資料夾與 ' ... '</span><span class="sxs-lookup"><span data-stu-id="59dbd-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="59dbd-115">字元不能用來指定路徑中的父工作資料夾。</span><span class="sxs-lookup"><span data-stu-id="59dbd-115">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="59dbd-116">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="59dbd-116">Error codes</span></span>

<span data-ttu-id="59dbd-117">位於指定位置的資料夾。</span><span class="sxs-lookup"><span data-stu-id="59dbd-117">The folder at the specified location.</span></span> <span data-ttu-id="59dbd-118">資料夾是 [**TaskFolder**](taskfolder.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="59dbd-118">The folder is a [**TaskFolder**](taskfolder.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="59dbd-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="59dbd-119">Requirements</span></span>



| <span data-ttu-id="59dbd-120">需求</span><span class="sxs-lookup"><span data-stu-id="59dbd-120">Requirement</span></span> | <span data-ttu-id="59dbd-121">值</span><span class="sxs-lookup"><span data-stu-id="59dbd-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="59dbd-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59dbd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="59dbd-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59dbd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="59dbd-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59dbd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="59dbd-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59dbd-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="59dbd-126">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="59dbd-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="59dbd-127"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="59dbd-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="59dbd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="59dbd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59dbd-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59dbd-129"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





