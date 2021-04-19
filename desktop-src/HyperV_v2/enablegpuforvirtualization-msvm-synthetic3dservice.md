---
description: 啟用實體 GPU 以進行虛擬化。
ms.assetid: 700cb46b-97f1-40cf-88d2-64242f4bd2c6
title: Msvm_Synthetic3DService 類別的 EnableGPUForVirtualization 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService.EnableGPUForVirtualization
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 16cf21424e9af8398cd435dce409bccde03543a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980417"
---
# <a name="enablegpuforvirtualization-method-of-the-msvm_synthetic3dservice-class"></a><span data-ttu-id="edba2-103">Msvm Synthetic3DService 類別的 EnableGPUForVirtualization 方法 \_</span><span class="sxs-lookup"><span data-stu-id="edba2-103">EnableGPUForVirtualization method of the Msvm\_Synthetic3DService class</span></span>

<span data-ttu-id="edba2-104">啟用實體 GPU 以進行虛擬化。</span><span class="sxs-lookup"><span data-stu-id="edba2-104">Enables a physical GPU for virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="edba2-105">語法</span><span class="sxs-lookup"><span data-stu-id="edba2-105">Syntax</span></span>


```mof
uint32 EnableGPUForVirtualization(
  [in]  Msvm_Physical3dGraphicsProcessor REF PhysicalGPU,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="edba2-106">參數</span><span class="sxs-lookup"><span data-stu-id="edba2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edba2-107">*PhysicalGPU* \[在\]</span><span class="sxs-lookup"><span data-stu-id="edba2-107">*PhysicalGPU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edba2-108">[**Msvm \_ Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md)類別實例的參考，代表要啟用的實體 GPU。</span><span class="sxs-lookup"><span data-stu-id="edba2-108">A reference to an instance of the [**Msvm\_Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) class that represents the physical GPU to be enabled.</span></span>

</dd> <dt>

<span data-ttu-id="edba2-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="edba2-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edba2-110">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="edba2-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edba2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="edba2-111">Return value</span></span>

<span data-ttu-id="edba2-112">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="edba2-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="edba2-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="edba2-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="edba2-114">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="edba2-114">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="edba2-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="edba2-115">Requirements</span></span>



| <span data-ttu-id="edba2-116">需求</span><span class="sxs-lookup"><span data-stu-id="edba2-116">Requirement</span></span> | <span data-ttu-id="edba2-117">值</span><span class="sxs-lookup"><span data-stu-id="edba2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edba2-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="edba2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="edba2-119">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="edba2-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="edba2-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="edba2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="edba2-121">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="edba2-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="edba2-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="edba2-122">Namespace</span></span><br/>                | <span data-ttu-id="edba2-123">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="edba2-123">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="edba2-124">MOF</span><span class="sxs-lookup"><span data-stu-id="edba2-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="edba2-125"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="edba2-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="edba2-126">DLL</span><span class="sxs-lookup"><span data-stu-id="edba2-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edba2-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="edba2-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="edba2-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="edba2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edba2-129">**Msvm \_ Synthetic3DService**</span><span class="sxs-lookup"><span data-stu-id="edba2-129">**Msvm\_Synthetic3DService**</span></span>](msvm-synthetic3dservice.md)
</dt> </dl>

 

