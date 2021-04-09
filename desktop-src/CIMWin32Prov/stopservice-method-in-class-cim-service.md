---
description: 停止衍生自 CIM 服務的物件所代表的服務 \_ 。
ms.assetid: f9eedde7-8d71-40a2-b1e9-7ba97e634f64
ms.tgt_platform: multiple
title: 'CIM_Service 類別的 StopService 方法 (Sdoias) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 14a7d378b514a93906c3be4f711bd6ab5b88bf17
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110733"
---
# <a name="stopservice-method-of-the-cim_service-class-sdoiash"></a><span data-ttu-id="1f284-103">CIM_Service 類別的 StopService 方法 (Sdoias) </span><span class="sxs-lookup"><span data-stu-id="1f284-103">StopService method of the CIM_Service class (Sdoias.h)</span></span>

<span data-ttu-id="1f284-104">**StopService** 方法會停止衍生自 [**CIM \_ 服務**](cim-service.md)的物件所代表的服務。</span><span class="sxs-lookup"><span data-stu-id="1f284-104">The **StopService** method stops the service represented by the object derived from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1f284-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="1f284-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1f284-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="1f284-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1f284-107">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="1f284-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1f284-108">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="1f284-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1f284-109">語法</span><span class="sxs-lookup"><span data-stu-id="1f284-109">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="1f284-110">參數</span><span class="sxs-lookup"><span data-stu-id="1f284-110">Parameters</span></span>

<span data-ttu-id="1f284-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1f284-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1f284-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1f284-112">Return value</span></span>

<span data-ttu-id="1f284-113">如果成功停止服務，則傳回 0 (零) 的值; 如果不支援要求，則傳回 1 (一個) ，以及指定錯誤的任何其他數位。</span><span class="sxs-lookup"><span data-stu-id="1f284-113">Returns a value of 0 (zero) if the service was successfully stopped, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f284-114">備註</span><span class="sxs-lookup"><span data-stu-id="1f284-114">Remarks</span></span>

<span data-ttu-id="1f284-115">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="1f284-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="1f284-116">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="1f284-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="1f284-117">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="1f284-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1f284-118">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1f284-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f284-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f284-119">Requirements</span></span>



| <span data-ttu-id="1f284-120">需求</span><span class="sxs-lookup"><span data-stu-id="1f284-120">Requirement</span></span> | <span data-ttu-id="1f284-121">值</span><span class="sxs-lookup"><span data-stu-id="1f284-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f284-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1f284-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1f284-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f284-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1f284-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1f284-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1f284-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f284-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1f284-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="1f284-126">Namespace</span></span><br/>                | <span data-ttu-id="1f284-127">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1f284-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1f284-128">標頭</span><span class="sxs-lookup"><span data-stu-id="1f284-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f284-129"><dt>Sdoias。h</dt></span><span class="sxs-lookup"><span data-stu-id="1f284-129"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="1f284-130">MOF</span><span class="sxs-lookup"><span data-stu-id="1f284-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f284-131"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f284-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f284-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1f284-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f284-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f284-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f284-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f284-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f284-135">CIM \_ 服務</span><span class="sxs-lookup"><span data-stu-id="1f284-135">CIM\_Service</span></span>](stopservice-method-in-class-cim-service.md)
</dt> <dt>

[<span data-ttu-id="1f284-136">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="1f284-136">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

