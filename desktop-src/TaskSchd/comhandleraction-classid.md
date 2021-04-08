---
title: ComHandlerAction 的 ClassId 屬性
description: 針對腳本，取得或設定處理常式類別的識別碼。
ms.assetid: 0b5de9ca-2ce2-4f77-bde9-8b8312753c37
keywords:
- ClassId 屬性工作排程器
- ClassId 屬性工作排程器，ComHandlerAction 物件
- ComHandlerAction 物件工作排程器，ClassId 屬性
topic_type:
- apiref
api_name:
- ComHandlerAction.ClassId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30409d5ea8067d1148bf42c88e2a3d1bb6f65ad1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685749"
---
# <a name="comhandleractionclassid-property"></a><span data-ttu-id="0e359-106">ComHandlerAction 的 ClassId 屬性</span><span class="sxs-lookup"><span data-stu-id="0e359-106">ComHandlerAction.ClassId property</span></span>

<span data-ttu-id="0e359-107">針對腳本，取得或設定處理常式類別的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e359-107">For scripting, gets or sets the identifier of the handler class.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e359-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e359-108">Syntax</span></span>


```VB
ComHandlerAction.ClassId As String
```



## <a name="property-value"></a><span data-ttu-id="0e359-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="0e359-109">Property value</span></span>

<span data-ttu-id="0e359-110">類別的識別碼，這個類別會定義要引發的處理常式。</span><span class="sxs-lookup"><span data-stu-id="0e359-110">The identifier of the class that defines the handler to be fired.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e359-111">備註</span><span class="sxs-lookup"><span data-stu-id="0e359-111">Remarks</span></span>

<span data-ttu-id="0e359-112">讀取或寫入 XML 時，會在工作排程器架構的 [**ClassId**](taskschedulerschema-classid-comhandlertype-element.md) 元素中指定 COM 處理常式的類別。</span><span class="sxs-lookup"><span data-stu-id="0e359-112">When reading or writing XML, the class of a COM handler is specified in the [**ClassId**](taskschedulerschema-classid-comhandlertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e359-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e359-113">Requirements</span></span>



| <span data-ttu-id="0e359-114">需求</span><span class="sxs-lookup"><span data-stu-id="0e359-114">Requirement</span></span> | <span data-ttu-id="0e359-115">值</span><span class="sxs-lookup"><span data-stu-id="0e359-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e359-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e359-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0e359-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e359-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0e359-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e359-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0e359-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e359-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0e359-120">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0e359-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="0e359-121"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0e359-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0e359-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0e359-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e359-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e359-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e359-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e359-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e359-125">工作排程器</span><span class="sxs-lookup"><span data-stu-id="0e359-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="0e359-126">**ComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="0e359-126">**ComHandlerAction**</span></span>](comhandleraction.md)
</dt> </dl>

 

 





