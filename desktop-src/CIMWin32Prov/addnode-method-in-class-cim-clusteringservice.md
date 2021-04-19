---
description: 將新的電腦系統帶入叢集中。
ms.assetid: 26d9428e-99de-4dcb-96ed-d773f28e015a
ms.tgt_platform: multiple
title: CIM_ClusteringService 類別的 AddNode 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.AddNode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1769ebb876fd2ae99c800a61b80d339a850ab232
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972338"
---
# <a name="addnode-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="06dd6-103">CIM ClusteringService 類別的 AddNode 方法 \_</span><span class="sxs-lookup"><span data-stu-id="06dd6-103">AddNode method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="06dd6-104">**AddNode** 方法會將新的電腦系統帶入叢集中。</span><span class="sxs-lookup"><span data-stu-id="06dd6-104">The **AddNode** method brings a new computer system into a cluster.</span></span> <span data-ttu-id="06dd6-105">要加入的節點會指定為方法的參數。</span><span class="sxs-lookup"><span data-stu-id="06dd6-105">The node to be added is specified as a parameter to the method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06dd6-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="06dd6-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="06dd6-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="06dd6-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="06dd6-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="06dd6-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="06dd6-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="06dd6-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="06dd6-110">語法</span><span class="sxs-lookup"><span data-stu-id="06dd6-110">Syntax</span></span>


```mof
uint32 AddNode(
  [in] CIM_ComputerSystem REF CS
);
```



## <a name="parameters"></a><span data-ttu-id="06dd6-111">參數</span><span class="sxs-lookup"><span data-stu-id="06dd6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06dd6-112">*CS* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06dd6-112">*CS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06dd6-113">要新增至叢集的電腦系統參考。</span><span class="sxs-lookup"><span data-stu-id="06dd6-113">Reference to the computer system to add to the cluster.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06dd6-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="06dd6-114">Return value</span></span>

<span data-ttu-id="06dd6-115">在成功時傳回 0 (零) 的值，如果不支援此作業，則傳回 1 (一個) ，以及表示錯誤的其他任何數位。</span><span class="sxs-lookup"><span data-stu-id="06dd6-115">Returns a value of 0 (zero) on success, 1 (one) if the operation is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="06dd6-116">備註</span><span class="sxs-lookup"><span data-stu-id="06dd6-116">Remarks</span></span>

<span data-ttu-id="06dd6-117">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="06dd6-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="06dd6-118">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="06dd6-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="06dd6-119">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="06dd6-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="06dd6-120">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="06dd6-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="06dd6-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="06dd6-121">Requirements</span></span>



| <span data-ttu-id="06dd6-122">需求</span><span class="sxs-lookup"><span data-stu-id="06dd6-122">Requirement</span></span> | <span data-ttu-id="06dd6-123">值</span><span class="sxs-lookup"><span data-stu-id="06dd6-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06dd6-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06dd6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="06dd6-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06dd6-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="06dd6-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06dd6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="06dd6-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06dd6-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="06dd6-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="06dd6-128">Namespace</span></span><br/>                | <span data-ttu-id="06dd6-129">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="06dd6-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="06dd6-130">MOF</span><span class="sxs-lookup"><span data-stu-id="06dd6-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06dd6-131"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="06dd6-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="06dd6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="06dd6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06dd6-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06dd6-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06dd6-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06dd6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06dd6-135">**CIM \_ ClusteringService**</span><span class="sxs-lookup"><span data-stu-id="06dd6-135">**CIM\_ClusteringService**</span></span>](addnode-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="06dd6-136">**CIM \_ ClusteringService**</span><span class="sxs-lookup"><span data-stu-id="06dd6-136">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

