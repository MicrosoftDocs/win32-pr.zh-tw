---
description: Shutdown 方法會要求關閉作業系統。
ms.assetid: f2a2a98b-2f4f-4aa1-9f54-515660273c8d
ms.tgt_platform: multiple
title: CIM_OperatingSystem 類別的 Shutdown 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78a11f325b8682b0024ff281a48989b837d3073a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847050"
---
# <a name="shutdown-method-of-the-cim_operatingsystem-class"></a><span data-ttu-id="2c06a-103">CIM 作業系統類別的 Shutdown 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2c06a-103">Shutdown method of the CIM\_OperatingSystem class</span></span>

<span data-ttu-id="2c06a-104">**Shutdown** 方法會要求關閉作業系統。</span><span class="sxs-lookup"><span data-stu-id="2c06a-104">The **Shutdown** method requests a shutdown of the operating system.</span></span> <span data-ttu-id="2c06a-105">作業系統的執行或子類別可以建立 **關機** 和 [**重新開機**](reboot-method-in-class-cim-operatingsystem.md) 方法之間的相依性。</span><span class="sxs-lookup"><span data-stu-id="2c06a-105">The implementation or subclass of the operating system can establish dependencies between the **Shutdown** and [**Reboot**](reboot-method-in-class-cim-operatingsystem.md) methods.</span></span> <span data-ttu-id="2c06a-106">例如，您可以提供更複雜的功能，例如已排程的關機和重新開機。</span><span class="sxs-lookup"><span data-stu-id="2c06a-106">For example, more sophisticated capabilities can be provided, such as a scheduled shutdown and reboot.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c06a-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="2c06a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2c06a-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="2c06a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2c06a-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="2c06a-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2c06a-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="2c06a-110">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2c06a-111">語法</span><span class="sxs-lookup"><span data-stu-id="2c06a-111">Syntax</span></span>


```mof
uint32 Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="2c06a-112">參數</span><span class="sxs-lookup"><span data-stu-id="2c06a-112">Parameters</span></span>

<span data-ttu-id="2c06a-113">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2c06a-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2c06a-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c06a-114">Return value</span></span>

<span data-ttu-id="2c06a-115">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="2c06a-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c06a-116">備註</span><span class="sxs-lookup"><span data-stu-id="2c06a-116">Remarks</span></span>

<span data-ttu-id="2c06a-117">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="2c06a-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="2c06a-118">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="2c06a-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="2c06a-119">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="2c06a-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2c06a-120">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="2c06a-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c06a-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c06a-121">Requirements</span></span>



| <span data-ttu-id="2c06a-122">需求</span><span class="sxs-lookup"><span data-stu-id="2c06a-122">Requirement</span></span> | <span data-ttu-id="2c06a-123">值</span><span class="sxs-lookup"><span data-stu-id="2c06a-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c06a-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c06a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2c06a-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c06a-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2c06a-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c06a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2c06a-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c06a-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2c06a-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="2c06a-128">Namespace</span></span><br/>                | <span data-ttu-id="2c06a-129">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2c06a-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2c06a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="2c06a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c06a-131"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c06a-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c06a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2c06a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c06a-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c06a-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c06a-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c06a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c06a-135">CIM \_ 作業系統</span><span class="sxs-lookup"><span data-stu-id="2c06a-135">CIM\_OperatingSystem</span></span>](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="2c06a-136">**CIM \_ 作業系統**</span><span class="sxs-lookup"><span data-stu-id="2c06a-136">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> </dl>

 

