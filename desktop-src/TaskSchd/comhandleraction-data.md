---
title: ComHandlerAction 屬性
description: 針對腳本，取得或設定與處理常式相關聯的其他資料。
ms.assetid: bf4d3e77-4b2b-4622-b26b-a8f7e9aa687b
keywords:
- 資料屬性工作排程器
- Data 屬性工作排程器，ComHandlerAction 物件
- ComHandlerAction 物件工作排程器、Data 屬性
topic_type:
- apiref
api_name:
- ComHandlerAction.Data
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15743c3f787a591a4644081fdd63189829d2eab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385130"
---
# <a name="comhandleractiondata-property"></a><span data-ttu-id="b91ed-106">ComHandlerAction 屬性</span><span class="sxs-lookup"><span data-stu-id="b91ed-106">ComHandlerAction.Data property</span></span>

<span data-ttu-id="b91ed-107">針對腳本，取得或設定與處理常式相關聯的其他資料。</span><span class="sxs-lookup"><span data-stu-id="b91ed-107">For scripting, gets or sets additional data that is associated with the handler.</span></span>

## <a name="syntax"></a><span data-ttu-id="b91ed-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b91ed-108">Syntax</span></span>


```VB
ComHandlerAction.Data As String
```



## <a name="property-value"></a><span data-ttu-id="b91ed-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="b91ed-109">Property value</span></span>

<span data-ttu-id="b91ed-110">處理常式所需的引數。</span><span class="sxs-lookup"><span data-stu-id="b91ed-110">The arguments that are needed by the handler.</span></span>

## <a name="remarks"></a><span data-ttu-id="b91ed-111">備註</span><span class="sxs-lookup"><span data-stu-id="b91ed-111">Remarks</span></span>

<span data-ttu-id="b91ed-112">讀取或寫入 XML 時，會在工作排程器架構的 [**資料**](taskschedulerschema-data-comhandlertype-element.md) 元素中指定 COM 處理常式的資料。</span><span class="sxs-lookup"><span data-stu-id="b91ed-112">When reading or writing XML, the data of a COM handler is specified in the [**Data**](taskschedulerschema-data-comhandlertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="b91ed-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b91ed-113">Requirements</span></span>



| <span data-ttu-id="b91ed-114">需求</span><span class="sxs-lookup"><span data-stu-id="b91ed-114">Requirement</span></span> | <span data-ttu-id="b91ed-115">值</span><span class="sxs-lookup"><span data-stu-id="b91ed-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b91ed-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b91ed-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b91ed-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b91ed-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b91ed-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b91ed-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b91ed-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b91ed-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b91ed-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="b91ed-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="b91ed-121"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b91ed-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b91ed-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b91ed-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b91ed-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b91ed-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b91ed-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b91ed-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b91ed-125">工作排程器</span><span class="sxs-lookup"><span data-stu-id="b91ed-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="b91ed-126">**ComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="b91ed-126">**ComHandlerAction**</span></span>](comhandleraction.md)
</dt> </dl>

 

 





