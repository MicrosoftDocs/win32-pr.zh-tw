---
title: TaskService. TargetServer 屬性
description: 若為腳本，會取得正在執行使用者所連接之工作排程器服務的電腦名稱稱。
ms.assetid: 8b0edf18-2a79-46f2-9b90-2c4726db881e
keywords:
- TargetServer 屬性工作排程器
- TargetServer 屬性工作排程器，TaskService 物件
- TaskService 物件工作排程器、TargetServer 屬性
topic_type:
- apiref
api_name:
- TaskService.TargetServer
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4347915fae57585716a64a6a4ca549ccc1c299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509436"
---
# <a name="taskservicetargetserver-property"></a><span data-ttu-id="99c6e-106">TaskService. TargetServer 屬性</span><span class="sxs-lookup"><span data-stu-id="99c6e-106">TaskService.TargetServer property</span></span>

<span data-ttu-id="99c6e-107">若為腳本，會取得正在執行使用者所連接之工作排程器服務的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="99c6e-107">For scripting, gets the name of the computer that is running the Task Scheduler service that the user is connected to.</span></span>

## <a name="syntax"></a><span data-ttu-id="99c6e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="99c6e-108">Syntax</span></span>


```VB
TaskService.TargetServer As String
```



## <a name="property-value"></a><span data-ttu-id="99c6e-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="99c6e-109">Property value</span></span>

<span data-ttu-id="99c6e-110">正在執行使用者所連接之工作排程器服務的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="99c6e-110">The name of the computer that is running the Task Scheduler service that the user is connected to.</span></span>

## <a name="remarks"></a><span data-ttu-id="99c6e-111">備註</span><span class="sxs-lookup"><span data-stu-id="99c6e-111">Remarks</span></span>

<span data-ttu-id="99c6e-112">當使用者傳遞 IP 位址、Localhost 或 '. ' 作為參數時，這個屬性會傳回空字串，而且當使用者未傳遞任何參數值時，它會傳回執行工作排程器服務的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="99c6e-112">This property returns an empty string when the user passes an IP address, Localhost, or '.' as a parameter, and it returns the name of the computer that is running the Task Scheduler service when the user does not pass any parameter value.</span></span>

## <a name="requirements"></a><span data-ttu-id="99c6e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="99c6e-113">Requirements</span></span>



| <span data-ttu-id="99c6e-114">需求</span><span class="sxs-lookup"><span data-stu-id="99c6e-114">Requirement</span></span> | <span data-ttu-id="99c6e-115">值</span><span class="sxs-lookup"><span data-stu-id="99c6e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99c6e-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99c6e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="99c6e-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99c6e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="99c6e-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99c6e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="99c6e-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99c6e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="99c6e-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="99c6e-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="99c6e-121"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="99c6e-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="99c6e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="99c6e-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99c6e-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99c6e-123"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





