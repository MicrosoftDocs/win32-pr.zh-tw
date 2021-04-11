---
description: CIM Disable-tapedrive 類別的 Reset 方法會 \_ 要求重設邏輯裝置。
ms.assetid: 48097e0d-7986-46b9-884d-7534f3848dd7
ms.tgt_platform: multiple
title: CIM_TapeDrive 類別的 Reset 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e5fd76d038e743ba5148f4c82555d50f0a5dde5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847543"
---
# <a name="reset-method-of-the-cim_tapedrive-class"></a><span data-ttu-id="03f72-103">CIM Disable-tapedrive 類別的 Reset 方法 \_</span><span class="sxs-lookup"><span data-stu-id="03f72-103">Reset method of the CIM\_TapeDrive class</span></span>

<span data-ttu-id="03f72-104">CIM Disable-tapedrive 類別的 **reset** 方法會 \_ 要求重設邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="03f72-104">The **Reset** method of the CIM\_TapeDrive class requests a reset of the logical device.</span></span> <span data-ttu-id="03f72-105">這個方法繼承自 [**CIM \_ LogicalDevice**](cim-logicaldevice.md)。</span><span class="sxs-lookup"><span data-stu-id="03f72-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="03f72-106">語法</span><span class="sxs-lookup"><span data-stu-id="03f72-106">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="03f72-107">參數</span><span class="sxs-lookup"><span data-stu-id="03f72-107">Parameters</span></span>

<span data-ttu-id="03f72-108">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="03f72-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03f72-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="03f72-109">Return value</span></span>

<span data-ttu-id="03f72-110">如果要求已成功執行，則傳回 0 (零) ，如果要求不受支援則為 1 (一個) ，如果發生錯誤，則會傳回另一個值。</span><span class="sxs-lookup"><span data-stu-id="03f72-110">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="03f72-111">備註</span><span class="sxs-lookup"><span data-stu-id="03f72-111">Remarks</span></span>

<span data-ttu-id="03f72-112">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="03f72-112">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="03f72-113">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="03f72-113">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="03f72-114">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="03f72-114">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="03f72-115">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="03f72-115">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="03f72-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="03f72-116">Requirements</span></span>



| <span data-ttu-id="03f72-117">需求</span><span class="sxs-lookup"><span data-stu-id="03f72-117">Requirement</span></span> | <span data-ttu-id="03f72-118">值</span><span class="sxs-lookup"><span data-stu-id="03f72-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03f72-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03f72-119">Minimum supported client</span></span><br/> | <span data-ttu-id="03f72-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03f72-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03f72-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03f72-121">Minimum supported server</span></span><br/> | <span data-ttu-id="03f72-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03f72-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03f72-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="03f72-123">Namespace</span></span><br/>                | <span data-ttu-id="03f72-124">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="03f72-124">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="03f72-125">MOF</span><span class="sxs-lookup"><span data-stu-id="03f72-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03f72-126"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="03f72-126"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="03f72-127">DLL</span><span class="sxs-lookup"><span data-stu-id="03f72-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03f72-128"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03f72-128"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03f72-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03f72-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03f72-130">CIM \_ disable-tapedrive</span><span class="sxs-lookup"><span data-stu-id="03f72-130">CIM\_TapeDrive</span></span>](reset-method-in-class-cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="03f72-131">**CIM \_ disable-tapedrive**</span><span class="sxs-lookup"><span data-stu-id="03f72-131">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> </dl>

 

 




