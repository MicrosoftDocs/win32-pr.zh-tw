---
description: 停止衍生自 CIM ClusteringService 的物件所代表的服務 \_ 。
ms.assetid: b8dbaeeb-819b-469b-9f5e-d658e88d1a6e
ms.tgt_platform: multiple
title: 'CIM_ClusteringService 類別的 StopService 方法 (Sdoias) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3a55f7b0a9527092e51156d55c7513ee59c4861
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847326"
---
# <a name="stopservice-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="866d7-103">CIM ClusteringService 類別的 StopService 方法 \_</span><span class="sxs-lookup"><span data-stu-id="866d7-103">StopService method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="866d7-104">**StopService** 方法會停止衍生自 [**CIM \_ ClusteringService**](cim-clusteringservice.md)的物件所代表的服務。</span><span class="sxs-lookup"><span data-stu-id="866d7-104">The **StopService** method stops the service represented by the object derived from [**CIM\_ClusteringService**](cim-clusteringservice.md).</span></span> <span data-ttu-id="866d7-105">這個方法繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="866d7-105">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="866d7-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="866d7-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="866d7-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="866d7-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="866d7-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="866d7-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="866d7-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="866d7-109">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="866d7-110">語法</span><span class="sxs-lookup"><span data-stu-id="866d7-110">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="866d7-111">參數</span><span class="sxs-lookup"><span data-stu-id="866d7-111">Parameters</span></span>

<span data-ttu-id="866d7-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="866d7-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="866d7-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="866d7-113">Return value</span></span>

<span data-ttu-id="866d7-114">如果成功停止服務，則傳回 0 (零) 的值; 如果不支援要求，則傳回 1 (一個) ，以及指定錯誤的任何其他數位。</span><span class="sxs-lookup"><span data-stu-id="866d7-114">Returns a value of 0 (zero) if the service was successfully stopped, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="866d7-115">備註</span><span class="sxs-lookup"><span data-stu-id="866d7-115">Remarks</span></span>

<span data-ttu-id="866d7-116">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="866d7-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="866d7-117">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="866d7-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="866d7-118">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="866d7-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="866d7-119">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="866d7-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="866d7-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="866d7-120">Requirements</span></span>



| <span data-ttu-id="866d7-121">需求</span><span class="sxs-lookup"><span data-stu-id="866d7-121">Requirement</span></span> | <span data-ttu-id="866d7-122">值</span><span class="sxs-lookup"><span data-stu-id="866d7-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="866d7-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="866d7-123">Minimum supported client</span></span><br/> | <span data-ttu-id="866d7-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="866d7-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="866d7-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="866d7-125">Minimum supported server</span></span><br/> | <span data-ttu-id="866d7-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="866d7-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="866d7-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="866d7-127">Namespace</span></span><br/>                | <span data-ttu-id="866d7-128">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="866d7-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="866d7-129">標頭</span><span class="sxs-lookup"><span data-stu-id="866d7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="866d7-130"><dt>Sdoias。h</dt></span><span class="sxs-lookup"><span data-stu-id="866d7-130"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="866d7-131">MOF</span><span class="sxs-lookup"><span data-stu-id="866d7-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="866d7-132"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="866d7-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="866d7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="866d7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="866d7-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="866d7-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="866d7-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="866d7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="866d7-136">**CIM \_ ClusteringService**</span><span class="sxs-lookup"><span data-stu-id="866d7-136">**CIM\_ClusteringService**</span></span>](stopservice-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="866d7-137">**CIM \_ ClusteringService**</span><span class="sxs-lookup"><span data-stu-id="866d7-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

