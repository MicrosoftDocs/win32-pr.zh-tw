---
title: ExecAction 路徑屬性
description: 針對腳本，取得或設定可執行檔的路徑。
ms.assetid: 00fea05f-4f57-47ac-9812-8cd352fe02a8
keywords:
- 路徑屬性工作排程器
- Path 屬性工作排程器，ExecAction 物件
- ExecAction 物件工作排程器，Path 屬性
topic_type:
- apiref
api_name:
- ExecAction.Path
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b20e1dcd8cd9700f961eb944c7be3168582b8c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685747"
---
# <a name="execactionpath-property"></a><span data-ttu-id="c0f17-106">ExecAction 路徑屬性</span><span class="sxs-lookup"><span data-stu-id="c0f17-106">ExecAction.Path property</span></span>

<span data-ttu-id="c0f17-107">針對腳本，取得或設定可執行檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="c0f17-107">For scripting, gets or sets the path to an executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0f17-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0f17-108">Syntax</span></span>


```VB
ExecAction.Path As String
```



## <a name="property-value"></a><span data-ttu-id="c0f17-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="c0f17-109">Property value</span></span>

<span data-ttu-id="c0f17-110">動作要執行之可執行檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="c0f17-110">The path to the executable file to be run by the action.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0f17-111">備註</span><span class="sxs-lookup"><span data-stu-id="c0f17-111">Remarks</span></span>

<span data-ttu-id="c0f17-112">此動作會執行命令列操作。</span><span class="sxs-lookup"><span data-stu-id="c0f17-112">This action performs a command-line operation.</span></span> <span data-ttu-id="c0f17-113">例如，動作可以執行腳本或啟動可執行檔。</span><span class="sxs-lookup"><span data-stu-id="c0f17-113">For example, the action could run a script or launch an executable.</span></span>

<span data-ttu-id="c0f17-114">讀取或寫入 XML 時，命令列作業路徑是在工作排程器架構的 [**command**](taskschedulerschema-command-exectype-element.md) 元素中指定。</span><span class="sxs-lookup"><span data-stu-id="c0f17-114">When reading or writing XML, the command-line operation path is specified in the [**Command**](taskschedulerschema-command-exectype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="c0f17-115">檢查此路徑以確定它在註冊工作時有效，而不是在設定這個屬性時有效。</span><span class="sxs-lookup"><span data-stu-id="c0f17-115">The path is checked to make sure it is valid when the task is registered, not when this property is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0f17-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0f17-116">Requirements</span></span>



| <span data-ttu-id="c0f17-117">需求</span><span class="sxs-lookup"><span data-stu-id="c0f17-117">Requirement</span></span> | <span data-ttu-id="c0f17-118">值</span><span class="sxs-lookup"><span data-stu-id="c0f17-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f17-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0f17-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c0f17-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0f17-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c0f17-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0f17-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c0f17-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0f17-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c0f17-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c0f17-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="c0f17-124"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c0f17-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c0f17-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c0f17-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0f17-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0f17-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0f17-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0f17-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0f17-128">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="c0f17-128">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="c0f17-129">工作排程器</span><span class="sxs-lookup"><span data-stu-id="c0f17-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





