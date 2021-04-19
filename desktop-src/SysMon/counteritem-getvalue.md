---
title: CounterItem. GetValue 方法
description: 抓取計數器的最後一個值。
ms.assetid: cf50d878-a119-42b0-bc59-b0e37ed15321
keywords:
- GetValue 方法 SysMon
- GetValue 方法 SysMon，CounterItem 類別
- CounterItem 類別 SysMon、GetValue 方法
topic_type:
- apiref
api_name:
- CounterItem.GetValue
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e40950ce4a8bf24a6a4301db133779b34ce4ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106999820"
---
# <a name="counteritemgetvalue-method"></a><span data-ttu-id="62537-106">CounterItem. GetValue 方法</span><span class="sxs-lookup"><span data-stu-id="62537-106">CounterItem.GetValue method</span></span>

<span data-ttu-id="62537-107">抓取計數器的最後一個值。</span><span class="sxs-lookup"><span data-stu-id="62537-107">Retrieves the last value of the counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="62537-108">語法</span><span class="sxs-lookup"><span data-stu-id="62537-108">Syntax</span></span>


```VB
CounterItem.GetValue( _
  ByRef value As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="62537-109">參數</span><span class="sxs-lookup"><span data-stu-id="62537-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62537-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="62537-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62537-111">計數器的上次取樣值。</span><span class="sxs-lookup"><span data-stu-id="62537-111">Last sampled value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="62537-112">*狀態* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="62537-112">*status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62537-113">指出值是否有效。</span><span class="sxs-lookup"><span data-stu-id="62537-113">Indicates if the value is valid.</span></span>



| <span data-ttu-id="62537-114">值</span><span class="sxs-lookup"><span data-stu-id="62537-114">Value</span></span>                                                                                              | <span data-ttu-id="62537-115">意義</span><span class="sxs-lookup"><span data-stu-id="62537-115">Meaning</span></span>                            |
|----------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="62537-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="62537-116"><dt>0</dt></span></span> </dl>                       | <span data-ttu-id="62537-117">值有效。</span><span class="sxs-lookup"><span data-stu-id="62537-117">The value is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="62537-118"><dt>0xC0000BBA (3221228474) </dt></span><span class="sxs-lookup"><span data-stu-id="62537-118"><dt>0xC0000BBA (3221228474)</dt></span></span> </dl> | <span data-ttu-id="62537-119">值無效。</span><span class="sxs-lookup"><span data-stu-id="62537-119">The value is not valid.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62537-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="62537-120">Return value</span></span>

<span data-ttu-id="62537-121">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="62537-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62537-122">備註</span><span class="sxs-lookup"><span data-stu-id="62537-122">Remarks</span></span>

<span data-ttu-id="62537-123">如果計數器資料的來源來自記錄檔，則此值會是記錄檔中的最後一個計數器值。</span><span class="sxs-lookup"><span data-stu-id="62537-123">If the source of the counter data is from a log file, the value is the last counter value in the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="62537-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="62537-124">Requirements</span></span>



| <span data-ttu-id="62537-125">需求</span><span class="sxs-lookup"><span data-stu-id="62537-125">Requirement</span></span> | <span data-ttu-id="62537-126">值</span><span class="sxs-lookup"><span data-stu-id="62537-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62537-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62537-127">Minimum supported client</span></span><br/> | <span data-ttu-id="62537-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62537-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="62537-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62537-129">Minimum supported server</span></span><br/> | <span data-ttu-id="62537-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62537-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62537-131">DLL</span><span class="sxs-lookup"><span data-stu-id="62537-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62537-132"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="62537-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62537-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62537-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62537-134">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="62537-134">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="62537-135">**CounterItem.GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="62537-135">**CounterItem.GetStatistics**</span></span>](counteritem-getstatistics.md)
</dt> <dt>

[<span data-ttu-id="62537-136">**CounterItem。值**</span><span class="sxs-lookup"><span data-stu-id="62537-136">**CounterItem.Value**</span></span>](counteritem-value.md)
</dt> </dl>

 

 





