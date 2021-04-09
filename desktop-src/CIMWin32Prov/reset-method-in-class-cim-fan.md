---
description: CIM 風扇類別的 Reset 方法會 \_ 要求重設邏輯裝置。
ms.assetid: f7755cf6-cc16-4559-ac72-60d3a782f267
ms.tgt_platform: multiple
title: CIM_Fan 類別的 Reset 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Fan.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4ae819960183b644e7dc8dddd93050c316e60eef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110028"
---
# <a name="reset-method-of-the-cim_fan-class"></a><span data-ttu-id="39bb6-103">CIM 風扇類別的 Reset 方法 \_</span><span class="sxs-lookup"><span data-stu-id="39bb6-103">Reset method of the CIM\_Fan class</span></span>

<span data-ttu-id="39bb6-104">CIM 風扇類別的 **reset** 方法會 \_ 要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="39bb6-104">The **Reset** method of the CIM\_Fan class requests a reset of the logical device.</span></span> <span data-ttu-id="39bb6-105">這個方法繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="39bb6-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39bb6-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="39bb6-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="39bb6-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="39bb6-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="39bb6-108">語法</span><span class="sxs-lookup"><span data-stu-id="39bb6-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="39bb6-109">參數</span><span class="sxs-lookup"><span data-stu-id="39bb6-109">Parameters</span></span>

<span data-ttu-id="39bb6-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="39bb6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="39bb6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="39bb6-111">Return value</span></span>

<span data-ttu-id="39bb6-112">如果要求已成功執行，則傳回 0 (零) ，如果要求不受支援則為 1 (一個) ，如果發生錯誤，則會傳回另一個值。</span><span class="sxs-lookup"><span data-stu-id="39bb6-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="39bb6-113">備註</span><span class="sxs-lookup"><span data-stu-id="39bb6-113">Remarks</span></span>

<span data-ttu-id="39bb6-114">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="39bb6-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="39bb6-115">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="39bb6-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="39bb6-116">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="39bb6-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="39bb6-117">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="39bb6-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="39bb6-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="39bb6-118">Requirements</span></span>



| <span data-ttu-id="39bb6-119">需求</span><span class="sxs-lookup"><span data-stu-id="39bb6-119">Requirement</span></span> | <span data-ttu-id="39bb6-120">值</span><span class="sxs-lookup"><span data-stu-id="39bb6-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39bb6-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39bb6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="39bb6-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39bb6-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="39bb6-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39bb6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="39bb6-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39bb6-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="39bb6-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="39bb6-125">Namespace</span></span><br/>                | <span data-ttu-id="39bb6-126">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="39bb6-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="39bb6-127">MOF</span><span class="sxs-lookup"><span data-stu-id="39bb6-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39bb6-128"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="39bb6-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="39bb6-129">DLL</span><span class="sxs-lookup"><span data-stu-id="39bb6-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39bb6-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39bb6-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39bb6-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39bb6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39bb6-132">CIM \_ 風扇</span><span class="sxs-lookup"><span data-stu-id="39bb6-132">CIM\_Fan</span></span>](reset-method-in-class-cim-fan.md)
</dt> <dt>

[<span data-ttu-id="39bb6-133">**CIM \_ 風扇**</span><span class="sxs-lookup"><span data-stu-id="39bb6-133">**CIM\_Fan**</span></span>](cim-fan.md)
</dt> </dl>

 

 




