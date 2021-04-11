---
description: Reset 方法會要求重設邏輯裝置。 這個方法繼承自 CIM \_ LogicalDevice。
ms.assetid: 4ddbad2a-e586-434a-a33e-7d60dcb67b3a
ms.tgt_platform: multiple
title: CIM_DiscreteSensor 類別的 Reset 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiscreteSensor.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d45544e62144c2d3aa14d898b5d595d3ea5b34f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688560"
---
# <a name="reset-method-of-the-cim_discretesensor-class"></a><span data-ttu-id="afc69-104">CIM DiscreteSensor 類別的 Reset 方法 \_</span><span class="sxs-lookup"><span data-stu-id="afc69-104">Reset method of the CIM\_DiscreteSensor class</span></span>

<span data-ttu-id="afc69-105">**Reset** 方法會要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="afc69-105">The **Reset** method requests a reset of the logical device.</span></span> <span data-ttu-id="afc69-106">這個方法繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="afc69-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="afc69-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="afc69-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="afc69-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="afc69-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="afc69-109">語法</span><span class="sxs-lookup"><span data-stu-id="afc69-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="afc69-110">參數</span><span class="sxs-lookup"><span data-stu-id="afc69-110">Parameters</span></span>

<span data-ttu-id="afc69-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="afc69-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="afc69-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="afc69-112">Return value</span></span>

<span data-ttu-id="afc69-113">如果要求已成功執行，則傳回 0 (零) ，如果要求不受支援則為 1 (一個) ，如果發生錯誤，則會傳回另一個值。</span><span class="sxs-lookup"><span data-stu-id="afc69-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="afc69-114">備註</span><span class="sxs-lookup"><span data-stu-id="afc69-114">Remarks</span></span>

<span data-ttu-id="afc69-115">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="afc69-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="afc69-116">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="afc69-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="afc69-117">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="afc69-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="afc69-118">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="afc69-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="afc69-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="afc69-119">Requirements</span></span>



| <span data-ttu-id="afc69-120">需求</span><span class="sxs-lookup"><span data-stu-id="afc69-120">Requirement</span></span> | <span data-ttu-id="afc69-121">值</span><span class="sxs-lookup"><span data-stu-id="afc69-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afc69-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="afc69-122">Minimum supported client</span></span><br/> | <span data-ttu-id="afc69-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="afc69-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="afc69-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="afc69-124">Minimum supported server</span></span><br/> | <span data-ttu-id="afc69-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afc69-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="afc69-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="afc69-126">Namespace</span></span><br/>                | <span data-ttu-id="afc69-127">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="afc69-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="afc69-128">MOF</span><span class="sxs-lookup"><span data-stu-id="afc69-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="afc69-129"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="afc69-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="afc69-130">DLL</span><span class="sxs-lookup"><span data-stu-id="afc69-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afc69-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afc69-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afc69-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afc69-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afc69-133">CIM \_ DiscreteSensor</span><span class="sxs-lookup"><span data-stu-id="afc69-133">CIM\_DiscreteSensor</span></span>](reset-method-in-class-cim-discretesensor.md)
</dt> <dt>

[<span data-ttu-id="afc69-134">**CIM \_ DiscreteSensor**</span><span class="sxs-lookup"><span data-stu-id="afc69-134">**CIM\_DiscreteSensor**</span></span>](cim-discretesensor.md)
</dt> </dl>

 

 




