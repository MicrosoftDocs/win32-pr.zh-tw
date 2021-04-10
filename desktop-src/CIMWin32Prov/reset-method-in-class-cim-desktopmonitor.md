---
description: CIM DesktopMonitor 類別的 Reset 方法會 \_ 要求重設邏輯裝置。
ms.assetid: 75fb6290-13b4-4831-9c61-81e950d53472
ms.tgt_platform: multiple
title: CIM_DesktopMonitor 類別的 Reset 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DesktopMonitor.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b59367e616b5320974075352ef4c845265dff61
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110032"
---
# <a name="reset-method-of-the-cim_desktopmonitor-class"></a><span data-ttu-id="d6446-103">CIM DesktopMonitor 類別的 Reset 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d6446-103">Reset method of the CIM\_DesktopMonitor class</span></span>

<span data-ttu-id="d6446-104">CIM DesktopMonitor 類別的 **reset** 方法會 \_ 要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="d6446-104">The **Reset** method of the CIM\_DesktopMonitor class requests a reset of the logical device.</span></span> <span data-ttu-id="d6446-105">這個方法繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="d6446-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d6446-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="d6446-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d6446-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="d6446-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d6446-108">語法</span><span class="sxs-lookup"><span data-stu-id="d6446-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="d6446-109">參數</span><span class="sxs-lookup"><span data-stu-id="d6446-109">Parameters</span></span>

<span data-ttu-id="d6446-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d6446-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d6446-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6446-111">Return value</span></span>

<span data-ttu-id="d6446-112">如果要求已成功執行，則傳回 0 (零) ，如果要求不受支援則為 1 (一個) ，如果發生錯誤，則會傳回另一個值。</span><span class="sxs-lookup"><span data-stu-id="d6446-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6446-113">備註</span><span class="sxs-lookup"><span data-stu-id="d6446-113">Remarks</span></span>

<span data-ttu-id="d6446-114">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="d6446-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="d6446-115">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="d6446-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="d6446-116">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="d6446-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d6446-117">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d6446-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6446-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6446-118">Requirements</span></span>



| <span data-ttu-id="d6446-119">需求</span><span class="sxs-lookup"><span data-stu-id="d6446-119">Requirement</span></span> | <span data-ttu-id="d6446-120">值</span><span class="sxs-lookup"><span data-stu-id="d6446-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6446-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d6446-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d6446-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6446-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d6446-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d6446-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d6446-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6446-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d6446-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="d6446-125">Namespace</span></span><br/>                | <span data-ttu-id="d6446-126">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d6446-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d6446-127">MOF</span><span class="sxs-lookup"><span data-stu-id="d6446-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6446-128"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6446-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6446-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d6446-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6446-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6446-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6446-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6446-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6446-132">CIM \_ DesktopMonitor</span><span class="sxs-lookup"><span data-stu-id="d6446-132">CIM\_DesktopMonitor</span></span>](reset-method-in-class-cim-desktopmonitor.md)
</dt> <dt>

[<span data-ttu-id="d6446-133">**CIM \_ DesktopMonitor**</span><span class="sxs-lookup"><span data-stu-id="d6446-133">**CIM\_DesktopMonitor**</span></span>](cim-desktopmonitor.md)
</dt> </dl>

 

 




