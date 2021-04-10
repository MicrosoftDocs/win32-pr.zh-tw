---
description: StartService 方法會將服務置於啟動狀態。
ms.assetid: 2efd2a06-a03c-4f4c-b2fa-889f84faac0f
ms.tgt_platform: multiple
title: CIM_ClusteringService 類別的 StartService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b8abdeffa234461952f99013524042dcbba6e682
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187735"
---
# <a name="startservice-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="1113e-103">CIM ClusteringService 類別的 StartService 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1113e-103">StartService method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="1113e-104">**StartService** 方法會將服務置於啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="1113e-104">The **StartService** method puts the service in a started state.</span></span> <span data-ttu-id="1113e-105">在子類別中，可以使用方法上的 **ValueMap** 辨識符號來指定可能的傳回碼組。</span><span class="sxs-lookup"><span data-stu-id="1113e-105">In a subclass, the set of possible return codes can be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="1113e-106">您也可以在子類別中，以 **值** 陣列限定詞的形式指定要轉譯之 **ValueMap** 內容的字串。</span><span class="sxs-lookup"><span data-stu-id="1113e-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="1113e-107">這個方法繼承自 [**CIM \_ 服務**](cim-service.md)。</span><span class="sxs-lookup"><span data-stu-id="1113e-107">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1113e-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="1113e-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1113e-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="1113e-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1113e-110">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="1113e-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1113e-111">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="1113e-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1113e-112">語法</span><span class="sxs-lookup"><span data-stu-id="1113e-112">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="1113e-113">參數</span><span class="sxs-lookup"><span data-stu-id="1113e-113">Parameters</span></span>

<span data-ttu-id="1113e-114">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1113e-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1113e-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="1113e-115">Return value</span></span>

<span data-ttu-id="1113e-116">如果服務成功啟動，則傳回 0 (零) 的值，如果不支援要求，則傳回 1 (一個) ，以及指定錯誤的任何其他數位。</span><span class="sxs-lookup"><span data-stu-id="1113e-116">Returns a value of 0 (zero) if the service was successfully started, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="1113e-117">備註</span><span class="sxs-lookup"><span data-stu-id="1113e-117">Remarks</span></span>

<span data-ttu-id="1113e-118">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="1113e-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="1113e-119">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="1113e-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="1113e-120">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="1113e-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1113e-121">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1113e-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1113e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="1113e-122">Requirements</span></span>



| <span data-ttu-id="1113e-123">需求</span><span class="sxs-lookup"><span data-stu-id="1113e-123">Requirement</span></span> | <span data-ttu-id="1113e-124">值</span><span class="sxs-lookup"><span data-stu-id="1113e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1113e-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1113e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1113e-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1113e-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1113e-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1113e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1113e-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1113e-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1113e-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="1113e-129">Namespace</span></span><br/>                | <span data-ttu-id="1113e-130">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1113e-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1113e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="1113e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1113e-132"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="1113e-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1113e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1113e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1113e-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1113e-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1113e-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1113e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1113e-136">CIM \_ ClusteringService</span><span class="sxs-lookup"><span data-stu-id="1113e-136">CIM\_ClusteringService</span></span>](startservice-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="1113e-137">**CIM \_ ClusteringService**</span><span class="sxs-lookup"><span data-stu-id="1113e-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

