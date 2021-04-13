---
title: TaskNamedValueCollection. Create 方法
description: 針對腳本，會在集合中建立名稱/值組。
ms.assetid: f64e0548-fad3-4682-b50b-ff8ec685af36
keywords:
- 建立方法工作排程器
- 建立方法工作排程器，TaskNamedValueCollection 物件
- TaskNamedValueCollection 物件工作排程器，建立方法
topic_type:
- apiref
api_name:
- TaskNamedValueCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3926142b25cbb2d65efaa45d6b767ce2e56ba86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466425"
---
# <a name="tasknamedvaluecollectioncreate-method"></a><span data-ttu-id="28652-106">TaskNamedValueCollection. Create 方法</span><span class="sxs-lookup"><span data-stu-id="28652-106">TaskNamedValueCollection.Create method</span></span>

<span data-ttu-id="28652-107">針對腳本，會在集合中建立名稱/值組。</span><span class="sxs-lookup"><span data-stu-id="28652-107">For scripting, creates a name-value pair in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="28652-108">語法</span><span class="sxs-lookup"><span data-stu-id="28652-108">Syntax</span></span>


```VB
TaskNamedValueCollection.Create( _
  ByVal name, _
  ByVal value, _
  ByRef pair _
)
```



## <a name="parameters"></a><span data-ttu-id="28652-109">參數</span><span class="sxs-lookup"><span data-stu-id="28652-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28652-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28652-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28652-111">與名稱/值配對中的值相關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="28652-111">The name that is associated with a value in a name-value pair.</span></span>

</dd> <dt>

<span data-ttu-id="28652-112">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28652-112">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28652-113">與名稱/值配對中的名稱相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="28652-113">The value that is associated with a name in a name-value pair.</span></span>

</dd> <dt>

<span data-ttu-id="28652-114">*配對* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="28652-114">*pair* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28652-115">在集合中建立的名稱/值組。</span><span class="sxs-lookup"><span data-stu-id="28652-115">The name-value pair that is created in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28652-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="28652-116">Return value</span></span>

<span data-ttu-id="28652-117">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="28652-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="28652-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="28652-118">Requirements</span></span>



| <span data-ttu-id="28652-119">需求</span><span class="sxs-lookup"><span data-stu-id="28652-119">Requirement</span></span> | <span data-ttu-id="28652-120">值</span><span class="sxs-lookup"><span data-stu-id="28652-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28652-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28652-121">Minimum supported client</span></span><br/> | <span data-ttu-id="28652-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28652-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="28652-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28652-123">Minimum supported server</span></span><br/> | <span data-ttu-id="28652-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28652-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="28652-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="28652-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="28652-126"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="28652-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="28652-127">DLL</span><span class="sxs-lookup"><span data-stu-id="28652-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28652-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28652-128"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





