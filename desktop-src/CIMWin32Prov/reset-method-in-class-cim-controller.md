---
description: CIM 控制器類別的 Reset 方法會 \_ 要求重設邏輯裝置。
ms.assetid: 98ec2010-4ce1-4aa8-941f-947714de8e7b
ms.tgt_platform: multiple
title: CIM_Controller 類別的 Reset 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Controller.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a1585f153e16e7ffa7133871064f4ff7e1277243
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989895"
---
# <a name="reset-method-of-the-cim_controller-class"></a><span data-ttu-id="7f2f6-103">CIM 控制器類別的 Reset 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7f2f6-103">Reset method of the CIM\_Controller class</span></span>

<span data-ttu-id="7f2f6-104">CIM 控制器類別的 **reset** 方法會 \_ 要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="7f2f6-104">The **Reset** method of the CIM\_Controller class requests a reset of the logical device.</span></span> <span data-ttu-id="7f2f6-105">這個方法繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="7f2f6-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f2f6-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="7f2f6-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7f2f6-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="7f2f6-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7f2f6-108">語法</span><span class="sxs-lookup"><span data-stu-id="7f2f6-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="7f2f6-109">參數</span><span class="sxs-lookup"><span data-stu-id="7f2f6-109">Parameters</span></span>

<span data-ttu-id="7f2f6-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7f2f6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7f2f6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f2f6-111">Return value</span></span>

<span data-ttu-id="7f2f6-112">如果要求已成功執行，則傳回 0 (零) ，如果要求不受支援則為 1 (一個) ，如果發生錯誤，則會傳回另一個值。</span><span class="sxs-lookup"><span data-stu-id="7f2f6-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f2f6-113">備註</span><span class="sxs-lookup"><span data-stu-id="7f2f6-113">Remarks</span></span>

<span data-ttu-id="7f2f6-114">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="7f2f6-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="7f2f6-115">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="7f2f6-115">To use this method, you must implement it in your own provider.</span></span> <span data-ttu-id="7f2f6-116">如需詳細資訊，請參閱 [建立 WMI 提供者](/windows/desktop/WmiSdk/creating-wmi-providers)。</span><span class="sxs-lookup"><span data-stu-id="7f2f6-116">For more information, see [Creating WMI Providers](/windows/desktop/WmiSdk/creating-wmi-providers).</span></span>

<span data-ttu-id="7f2f6-117">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="7f2f6-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7f2f6-118">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="7f2f6-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f2f6-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f2f6-119">Requirements</span></span>



| <span data-ttu-id="7f2f6-120">需求</span><span class="sxs-lookup"><span data-stu-id="7f2f6-120">Requirement</span></span> | <span data-ttu-id="7f2f6-121">值</span><span class="sxs-lookup"><span data-stu-id="7f2f6-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f2f6-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f2f6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7f2f6-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f2f6-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7f2f6-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f2f6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7f2f6-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f2f6-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7f2f6-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="7f2f6-126">Namespace</span></span><br/>                | <span data-ttu-id="7f2f6-127">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7f2f6-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7f2f6-128">MOF</span><span class="sxs-lookup"><span data-stu-id="7f2f6-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f2f6-129"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f2f6-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f2f6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7f2f6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f2f6-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f2f6-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f2f6-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f2f6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f2f6-133">CIM \_ 控制器</span><span class="sxs-lookup"><span data-stu-id="7f2f6-133">CIM\_Controller</span></span>](reset-method-in-class-cim-controller.md)
</dt> <dt>

[<span data-ttu-id="7f2f6-134">**CIM \_ 控制器**</span><span class="sxs-lookup"><span data-stu-id="7f2f6-134">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

