---
description: EvictNode 方法會從叢集中移除電腦系統。 要收回的節點會指定為方法的參數。
ms.assetid: 4691d536-ade3-4a02-bc28-e31ebaf5d9e4
ms.tgt_platform: multiple
title: CIM_ClusteringService 類別的 EvictNode 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.EvictNode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d68ddc1adc0af335dcf2d4139cf7c1f0a381d986
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688747"
---
# <a name="evictnode-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="30f91-104">CIM ClusteringService 類別的 EvictNode 方法 \_</span><span class="sxs-lookup"><span data-stu-id="30f91-104">EvictNode method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="30f91-105">**EvictNode** 方法會從叢集中移除電腦系統。</span><span class="sxs-lookup"><span data-stu-id="30f91-105">The **EvictNode** method removes a computer system from a cluster.</span></span> <span data-ttu-id="30f91-106">要收回的節點會指定為方法的參數。</span><span class="sxs-lookup"><span data-stu-id="30f91-106">The node to be evicted is specified as a parameter to the method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="30f91-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="30f91-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="30f91-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="30f91-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="30f91-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="30f91-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="30f91-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="30f91-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="30f91-111">語法</span><span class="sxs-lookup"><span data-stu-id="30f91-111">Syntax</span></span>


```mof
uint32 EvictNode(
  [in] CIM_ComputerSystem REF CS
);
```



## <a name="parameters"></a><span data-ttu-id="30f91-112">參數</span><span class="sxs-lookup"><span data-stu-id="30f91-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30f91-113">*CS* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30f91-113">*CS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30f91-114">要從叢集中移除的電腦系統參考。</span><span class="sxs-lookup"><span data-stu-id="30f91-114">Reference to the computer system to remove from the cluster.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30f91-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="30f91-115">Return value</span></span>

<span data-ttu-id="30f91-116">如果成功收回電腦系統，則會傳回 0 (零) ; 如果不支援此方法，則傳回 1 (一個) ，如果發生錯誤，則傳回任何其他數位。</span><span class="sxs-lookup"><span data-stu-id="30f91-116">Returns 0 (zero) if the computer system is successfully evicted, 1 (one) if the method is not supported, and any other number if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="30f91-117">備註</span><span class="sxs-lookup"><span data-stu-id="30f91-117">Remarks</span></span>

<span data-ttu-id="30f91-118">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="30f91-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="30f91-119">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="30f91-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="30f91-120">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="30f91-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="30f91-121">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="30f91-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="30f91-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="30f91-122">Requirements</span></span>



| <span data-ttu-id="30f91-123">需求</span><span class="sxs-lookup"><span data-stu-id="30f91-123">Requirement</span></span> | <span data-ttu-id="30f91-124">值</span><span class="sxs-lookup"><span data-stu-id="30f91-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30f91-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30f91-125">Minimum supported client</span></span><br/> | <span data-ttu-id="30f91-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30f91-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="30f91-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30f91-127">Minimum supported server</span></span><br/> | <span data-ttu-id="30f91-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30f91-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="30f91-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="30f91-129">Namespace</span></span><br/>                | <span data-ttu-id="30f91-130">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="30f91-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="30f91-131">MOF</span><span class="sxs-lookup"><span data-stu-id="30f91-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30f91-132"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="30f91-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="30f91-133">DLL</span><span class="sxs-lookup"><span data-stu-id="30f91-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30f91-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30f91-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30f91-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30f91-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30f91-136">**CIM \_ ClusteringService**</span><span class="sxs-lookup"><span data-stu-id="30f91-136">**CIM\_ClusteringService**</span></span>](evictnode-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="30f91-137">**CIM \_ ClusteringService**</span><span class="sxs-lookup"><span data-stu-id="30f91-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

