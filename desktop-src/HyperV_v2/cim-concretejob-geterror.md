---
description: 抓取由於作業失敗所造成的錯誤。
ms.assetid: d499eb91-e1cc-4792-b32d-5a8875eebbb7
title: CIM_ConcreteJob 類別的 GetError 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: aa9ed87f2d484286d91d14c4183d2ce3b6f41cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977025"
---
# <a name="geterror-method-of-the-cim_concretejob-class"></a><span data-ttu-id="fae9f-103">CIM ConcreteJob 類別的 GetError 方法 \_</span><span class="sxs-lookup"><span data-stu-id="fae9f-103">GetError method of the CIM\_ConcreteJob class</span></span>

<span data-ttu-id="fae9f-104">抓取由於作業失敗所造成的錯誤。</span><span class="sxs-lookup"><span data-stu-id="fae9f-104">Retrieves an error due to a failed job.</span></span> <span data-ttu-id="fae9f-105">當作業正在執行或已終止但沒有錯誤時，此方法不會傳回任何 [**CIM \_ 錯誤**](cim-error.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="fae9f-105">When the job is executing or has terminated without error, then this method returns no [**CIM\_Error**](cim-error.md) instance.</span></span> <span data-ttu-id="fae9f-106">但是，如果工作因為某些內部問題而失敗，或由於用戶端已終止作業，則會傳回 **CIM \_ 錯誤** 實例。</span><span class="sxs-lookup"><span data-stu-id="fae9f-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="fae9f-107">語法</span><span class="sxs-lookup"><span data-stu-id="fae9f-107">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="fae9f-108">參數</span><span class="sxs-lookup"><span data-stu-id="fae9f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fae9f-109">*錯誤* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fae9f-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fae9f-110">如果作業的 **OperationalStatus** 不是「確定」，則傳回 [**CIM \_ 錯誤**](cim-error.md)實例，否則會傳回 **null**。</span><span class="sxs-lookup"><span data-stu-id="fae9f-110">Returns a [**CIM\_Error**](cim-error.md) instance if the **OperationalStatus** on the Job is not "OK"; otherwise, returns **null**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fae9f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="fae9f-111">Return value</span></span>

<span data-ttu-id="fae9f-112">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="fae9f-112">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="fae9f-113">**成功** (0) </span><span class="sxs-lookup"><span data-stu-id="fae9f-113">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fae9f-114">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="fae9f-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fae9f-115">**未指定的錯誤** (2) </span><span class="sxs-lookup"><span data-stu-id="fae9f-115">**Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fae9f-116">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="fae9f-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fae9f-117">**失敗** (4) </span><span class="sxs-lookup"><span data-stu-id="fae9f-117">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fae9f-118">**不正確參數** (5) </span><span class="sxs-lookup"><span data-stu-id="fae9f-118">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fae9f-119">**拒絕存取** (6) </span><span class="sxs-lookup"><span data-stu-id="fae9f-119">**Access Denied** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fae9f-120">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="fae9f-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fae9f-121">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="fae9f-121">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fae9f-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="fae9f-122">Requirements</span></span>



| <span data-ttu-id="fae9f-123">需求</span><span class="sxs-lookup"><span data-stu-id="fae9f-123">Requirement</span></span> | <span data-ttu-id="fae9f-124">值</span><span class="sxs-lookup"><span data-stu-id="fae9f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fae9f-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fae9f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fae9f-126">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fae9f-126">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="fae9f-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fae9f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fae9f-128">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fae9f-128">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="fae9f-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="fae9f-129">Namespace</span></span><br/>                | <span data-ttu-id="fae9f-130">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="fae9f-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fae9f-131">MOF</span><span class="sxs-lookup"><span data-stu-id="fae9f-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fae9f-132"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="fae9f-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fae9f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fae9f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fae9f-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fae9f-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fae9f-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fae9f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fae9f-136">**CIM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="fae9f-136">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

 




