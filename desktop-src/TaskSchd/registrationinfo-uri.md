---
title: RegistrationInfo URI 屬性
description: 針對腳本，取得或設定工作的 URI。
ms.assetid: 49085ee4-65e1-412c-ac1c-9c0f9efe5679
keywords:
- URI 屬性工作排程器
- URI 屬性工作排程器，RegistrationInfo 物件
- RegistrationInfo 物件工作排程器，URI 屬性
topic_type:
- apiref
api_name:
- RegistrationInfo.URI
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77598d556fdec29f41004529471c8098314a6faf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509052"
---
# <a name="registrationinfouri-property"></a><span data-ttu-id="ff182-106">RegistrationInfo URI 屬性</span><span class="sxs-lookup"><span data-stu-id="ff182-106">RegistrationInfo.URI property</span></span>

<span data-ttu-id="ff182-107">針對腳本，取得或設定工作的 URI。</span><span class="sxs-lookup"><span data-stu-id="ff182-107">For scripting, gets or sets the URI of the task.</span></span>

<span data-ttu-id="ff182-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="ff182-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff182-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff182-109">Syntax</span></span>


```VB
RegistrationInfo.URI As String
```



## <a name="property-value"></a><span data-ttu-id="ff182-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="ff182-110">Property value</span></span>

<span data-ttu-id="ff182-111">工作的 URI。</span><span class="sxs-lookup"><span data-stu-id="ff182-111">The URI of the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff182-112">備註</span><span class="sxs-lookup"><span data-stu-id="ff182-112">Remarks</span></span>

<span data-ttu-id="ff182-113">讀取或寫入工作的 XML 時，會使用工作排程器架構的 [**URI**](taskschedulerschema-uri-registrationinfotype-element.md) 元素來指定工作 URI。</span><span class="sxs-lookup"><span data-stu-id="ff182-113">When reading or writing XML for a task, the task URI is specified using the [**URI**](taskschedulerschema-uri-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff182-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff182-114">Requirements</span></span>



| <span data-ttu-id="ff182-115">需求</span><span class="sxs-lookup"><span data-stu-id="ff182-115">Requirement</span></span> | <span data-ttu-id="ff182-116">值</span><span class="sxs-lookup"><span data-stu-id="ff182-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff182-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff182-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ff182-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff182-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ff182-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff182-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ff182-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff182-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ff182-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ff182-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="ff182-122"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ff182-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ff182-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ff182-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff182-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff182-124"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





