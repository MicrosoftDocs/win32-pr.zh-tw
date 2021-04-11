---
description: CIM PCMCIAController 類別的 Reset 方法會 \_ 要求重設邏輯裝置。
ms.assetid: c58e3265-2849-4154-a03e-2e1cfa9e3d30
ms.tgt_platform: multiple
title: CIM_PCMCIAController 類別的 Reset 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCMCIAController.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8576bc5c1ce291c355d2907761e5b342ea6f3bc9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187739"
---
# <a name="reset-method-of-the-cim_pcmciacontroller-class"></a><span data-ttu-id="e748c-103">CIM PCMCIAController 類別的 Reset 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e748c-103">Reset method of the CIM\_PCMCIAController class</span></span>

<span data-ttu-id="e748c-104">CIM PCMCIAController 類別的 **reset** 方法會 \_ 要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="e748c-104">The **Reset** method of the CIM\_PCMCIAController class requests a reset of the logical device.</span></span> <span data-ttu-id="e748c-105">這個方法繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="e748c-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e748c-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="e748c-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e748c-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="e748c-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e748c-108">語法</span><span class="sxs-lookup"><span data-stu-id="e748c-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="e748c-109">參數</span><span class="sxs-lookup"><span data-stu-id="e748c-109">Parameters</span></span>

<span data-ttu-id="e748c-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e748c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e748c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e748c-111">Return value</span></span>

<span data-ttu-id="e748c-112">如果要求已成功執行，則傳回 0 (零) ，如果要求不受支援則為 1 (一個) ，如果發生錯誤，則會傳回另一個值。</span><span class="sxs-lookup"><span data-stu-id="e748c-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="e748c-113">備註</span><span class="sxs-lookup"><span data-stu-id="e748c-113">Remarks</span></span>

<span data-ttu-id="e748c-114">這個方法不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="e748c-114">This method is not implemented by WMI.</span></span> <span data-ttu-id="e748c-115">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="e748c-115">To use this method, you must implement it in your own provider.</span></span> <span data-ttu-id="e748c-116">針對衍生自 [**CIM \_ PCMCIACONTROLLER**](cim-pcmciacontroller.md)的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="e748c-116">For WMI classes derived from [**CIM\_PCMCIAController**](cim-pcmciacontroller.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e748c-117">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="e748c-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e748c-118">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e748c-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e748c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e748c-119">Requirements</span></span>



| <span data-ttu-id="e748c-120">需求</span><span class="sxs-lookup"><span data-stu-id="e748c-120">Requirement</span></span> | <span data-ttu-id="e748c-121">值</span><span class="sxs-lookup"><span data-stu-id="e748c-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e748c-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e748c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e748c-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e748c-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e748c-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e748c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e748c-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e748c-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e748c-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="e748c-126">Namespace</span></span><br/>                | <span data-ttu-id="e748c-127">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e748c-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e748c-128">MOF</span><span class="sxs-lookup"><span data-stu-id="e748c-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e748c-129"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e748c-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e748c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e748c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e748c-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e748c-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e748c-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e748c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e748c-133">CIM \_ PCMCIAController</span><span class="sxs-lookup"><span data-stu-id="e748c-133">CIM\_PCMCIAController</span></span>](reset-method-in-class-cim-pcmciacontroller.md)
</dt> <dt>

[<span data-ttu-id="e748c-134">**CIM \_ PCMCIAController**</span><span class="sxs-lookup"><span data-stu-id="e748c-134">**CIM\_PCMCIAController**</span></span>](cim-pcmciacontroller.md)
</dt> </dl>

 

 




