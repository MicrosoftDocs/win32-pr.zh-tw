---
title: TaskService. HighestVersion 屬性
description: 針對腳本，表示電腦支援的最高工作排程器版本。
ms.assetid: b4e55e46-6f33-4224-811b-06bf218dd1ac
keywords:
- HighestVersion 屬性工作排程器
- HighestVersion 屬性工作排程器，TaskService 物件
- TaskService 物件工作排程器、HighestVersion 屬性
topic_type:
- apiref
api_name:
- TaskService.HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b4e381326ab901fcaf8657975ce3f8401facd44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686544"
---
# <a name="taskservicehighestversion-property"></a><span data-ttu-id="d52b3-106">TaskService. HighestVersion 屬性</span><span class="sxs-lookup"><span data-stu-id="d52b3-106">TaskService.HighestVersion property</span></span>

<span data-ttu-id="d52b3-107">針對腳本，表示電腦支援的最高工作排程器版本。</span><span class="sxs-lookup"><span data-stu-id="d52b3-107">For scripting, indicates the highest version of Task Scheduler that a computer supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="d52b3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d52b3-108">Syntax</span></span>


```VB
TaskService.HighestVersion As Integer
```



## <a name="property-value"></a><span data-ttu-id="d52b3-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="d52b3-109">Property value</span></span>

<span data-ttu-id="d52b3-110">電腦支援之工作排程器的最高版本。</span><span class="sxs-lookup"><span data-stu-id="d52b3-110">The highest version of Task Scheduler that a computer supports.</span></span> <span data-ttu-id="d52b3-111">最高版本是在16位界限上分割為 MajorVersion/MinorVersion 的值。</span><span class="sxs-lookup"><span data-stu-id="d52b3-111">The highest version is a value that is split into MajorVersion/MinorVersion on the 16-bit boundary.</span></span> <span data-ttu-id="d52b3-112">工作排程器服務會針對主要版本傳回1，次要版本則傳回2。</span><span class="sxs-lookup"><span data-stu-id="d52b3-112">The Task Scheduler service returns 1 for the major version and 2 for the minor version.</span></span> <span data-ttu-id="d52b3-113">您可以使用 [CLng](/previous-versions//ck4c5842(v=vs.85)) 函數來取得屬性的整數值。</span><span class="sxs-lookup"><span data-stu-id="d52b3-113">Use the [CLng](/previous-versions//ck4c5842(v=vs.85)) function to get the integer value of the property.</span></span>

## <a name="examples"></a><span data-ttu-id="d52b3-114">範例</span><span class="sxs-lookup"><span data-stu-id="d52b3-114">Examples</span></span>

<span data-ttu-id="d52b3-115">下列程式碼會示範如何使用 [CLng](/previous-versions//ck4c5842(v=vs.85)) 函數來取得 **HighestVersion** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="d52b3-115">The following code shows how to use the [CLng](/previous-versions//ck4c5842(v=vs.85)) function to get the value of the **HighestVersion** property.</span></span>


```VB
wscript.echo service.HighestVersion
Test = clng( service.HighestVersion )
If Test <> 65538  Then
    wscript.echo "Fail"

Else
    wscript.echo "Pass"
End If
```



## <a name="requirements"></a><span data-ttu-id="d52b3-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d52b3-116">Requirements</span></span>



| <span data-ttu-id="d52b3-117">需求</span><span class="sxs-lookup"><span data-stu-id="d52b3-117">Requirement</span></span> | <span data-ttu-id="d52b3-118">值</span><span class="sxs-lookup"><span data-stu-id="d52b3-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d52b3-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d52b3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d52b3-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d52b3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d52b3-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d52b3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d52b3-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d52b3-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d52b3-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d52b3-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="d52b3-124"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d52b3-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d52b3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d52b3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d52b3-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d52b3-126"><dt>Taskschd.dll</dt></span></span> </dl> |



 

