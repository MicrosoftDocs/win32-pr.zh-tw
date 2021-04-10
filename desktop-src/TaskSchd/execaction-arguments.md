---
title: ExecAction. Arguments 屬性
description: 針對腳本，取得或設定與命令列操作相關聯的引數。
ms.assetid: 911e720f-ea7b-474d-ac75-4cd4f9adee55
keywords:
- Arguments 屬性工作排程器
- Arguments 屬性工作排程器，ExecAction 物件
- ExecAction 物件工作排程器、Arguments 屬性
topic_type:
- apiref
api_name:
- ExecAction.Arguments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4207a9fbfb60d9e45c15e174a33e7d6ab66e5fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934145"
---
# <a name="execactionarguments-property"></a><span data-ttu-id="e8bf7-106">ExecAction. Arguments 屬性</span><span class="sxs-lookup"><span data-stu-id="e8bf7-106">ExecAction.Arguments property</span></span>

<span data-ttu-id="e8bf7-107">針對腳本，取得或設定與命令列操作相關聯的引數。</span><span class="sxs-lookup"><span data-stu-id="e8bf7-107">For scripting, gets or sets the arguments associated with the command-line operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8bf7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8bf7-108">Syntax</span></span>


```VB
ExecAction.Arguments As String
```



## <a name="property-value"></a><span data-ttu-id="e8bf7-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="e8bf7-109">Property value</span></span>

<span data-ttu-id="e8bf7-110">命令列操作所需的引數。</span><span class="sxs-lookup"><span data-stu-id="e8bf7-110">The arguments that are needed by the command-line operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8bf7-111">備註</span><span class="sxs-lookup"><span data-stu-id="e8bf7-111">Remarks</span></span>

<span data-ttu-id="e8bf7-112">讀取或寫入 XML 時，命令列作業引數是在工作排程器架構的 [**引數**](taskschedulerschema-arguments-exectype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="e8bf7-112">When reading or writing XML, the command-line operation arguments are specified in the [**Arguments**](taskschedulerschema-arguments-exectype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8bf7-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8bf7-113">Requirements</span></span>



| <span data-ttu-id="e8bf7-114">需求</span><span class="sxs-lookup"><span data-stu-id="e8bf7-114">Requirement</span></span> | <span data-ttu-id="e8bf7-115">值</span><span class="sxs-lookup"><span data-stu-id="e8bf7-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8bf7-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8bf7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e8bf7-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8bf7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e8bf7-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8bf7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e8bf7-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8bf7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e8bf7-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e8bf7-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="e8bf7-121"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e8bf7-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e8bf7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e8bf7-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8bf7-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8bf7-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8bf7-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8bf7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8bf7-125">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="e8bf7-125">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="e8bf7-126">工作排程器</span><span class="sxs-lookup"><span data-stu-id="e8bf7-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





