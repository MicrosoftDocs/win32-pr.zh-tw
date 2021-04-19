---
title: Actioncollection 動作。內容屬性
description: 針對腳本，取得或設定工作主體的識別碼。
ms.assetid: 5d8ac31c-ce07-4801-a04e-e12e996b88c6
keywords:
- 內容屬性工作排程器
- CoNtext 屬性工作排程器，Actioncollection 動作物件
- Actioncollection 動作物件工作排程器、內容屬性
topic_type:
- apiref
api_name:
- ActionCollection.Context
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98318ba8332e4c3bb0e7fee6b702a7ed50533
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107001299"
---
# <a name="actioncollectioncontext-property"></a><span data-ttu-id="c52bb-106">Actioncollection 動作。內容屬性</span><span class="sxs-lookup"><span data-stu-id="c52bb-106">ActionCollection.Context property</span></span>

<span data-ttu-id="c52bb-107">針對腳本，取得或設定工作主體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c52bb-107">For scripting, gets or sets the identifier of the principal for the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="c52bb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c52bb-108">Syntax</span></span>


```VB
ActionCollection.Context As String
```



## <a name="property-value"></a><span data-ttu-id="c52bb-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="c52bb-109">Property value</span></span>

<span data-ttu-id="c52bb-110">工作主體的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c52bb-110">The identifier of the principal for the task.</span></span> <span data-ttu-id="c52bb-111">在此指定的識別碼必須符合定義主體之 IPrincipal 介面的 Id 屬性中所指定的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c52bb-111">The identifier that is specified here must match the identifier that is specified in the Id property of the IPrincipal interface that defines the principal.</span></span>

## <a name="requirements"></a><span data-ttu-id="c52bb-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="c52bb-112">Requirements</span></span>



| <span data-ttu-id="c52bb-113">需求</span><span class="sxs-lookup"><span data-stu-id="c52bb-113">Requirement</span></span> | <span data-ttu-id="c52bb-114">值</span><span class="sxs-lookup"><span data-stu-id="c52bb-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c52bb-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c52bb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c52bb-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c52bb-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c52bb-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c52bb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c52bb-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c52bb-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c52bb-119">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c52bb-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="c52bb-120"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c52bb-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c52bb-121">DLL</span><span class="sxs-lookup"><span data-stu-id="c52bb-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c52bb-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c52bb-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c52bb-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c52bb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c52bb-124">工作排程器</span><span class="sxs-lookup"><span data-stu-id="c52bb-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="c52bb-125">**Actioncollection 動作**</span><span class="sxs-lookup"><span data-stu-id="c52bb-125">**ActionCollection**</span></span>](actioncollection.md)
</dt> </dl>

 

 





