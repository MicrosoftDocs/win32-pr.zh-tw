---
description: 重新開機方法會要求作業系統重新開機。
ms.assetid: 2ce766dd-51a4-4ffb-a45a-40399f1110f6
ms.tgt_platform: multiple
title: CIM_OperatingSystem 類別的重新開機方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e498dd16372503b23aa56471224faf4d5d0ff012
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997063"
---
# <a name="reboot-method-of-the-cim_operatingsystem-class"></a><span data-ttu-id="9ede1-103">CIM 作業系統類別的重新開機方法 \_</span><span class="sxs-lookup"><span data-stu-id="9ede1-103">Reboot method of the CIM\_OperatingSystem class</span></span>

<span data-ttu-id="9ede1-104">**重新開機** 方法會要求作業系統重新開機。</span><span class="sxs-lookup"><span data-stu-id="9ede1-104">The **Reboot** method requests a reboot of the operating system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9ede1-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="9ede1-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9ede1-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="9ede1-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9ede1-107">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="9ede1-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9ede1-108">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="9ede1-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9ede1-109">語法</span><span class="sxs-lookup"><span data-stu-id="9ede1-109">Syntax</span></span>


```mof
uint32 Reboot();
```



## <a name="parameters"></a><span data-ttu-id="9ede1-110">參數</span><span class="sxs-lookup"><span data-stu-id="9ede1-110">Parameters</span></span>

<span data-ttu-id="9ede1-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9ede1-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9ede1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9ede1-112">Return value</span></span>

<span data-ttu-id="9ede1-113">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="9ede1-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ede1-114">備註</span><span class="sxs-lookup"><span data-stu-id="9ede1-114">Remarks</span></span>

<span data-ttu-id="9ede1-115">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="9ede1-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="9ede1-116">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="9ede1-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="9ede1-117">針對衍生自 [**CIM \_ 作業系統**](cim-operatingsystem.md)的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="9ede1-117">For WMI classes that are derived from [**CIM\_OperatingSystem**](cim-operatingsystem.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9ede1-118">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="9ede1-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9ede1-119">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9ede1-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="9ede1-120">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="9ede1-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9ede1-121">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9ede1-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ede1-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="9ede1-122">Requirements</span></span>



| <span data-ttu-id="9ede1-123">需求</span><span class="sxs-lookup"><span data-stu-id="9ede1-123">Requirement</span></span> | <span data-ttu-id="9ede1-124">值</span><span class="sxs-lookup"><span data-stu-id="9ede1-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ede1-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9ede1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9ede1-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ede1-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9ede1-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9ede1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9ede1-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ede1-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9ede1-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="9ede1-129">Namespace</span></span><br/>                | <span data-ttu-id="9ede1-130">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9ede1-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9ede1-131">MOF</span><span class="sxs-lookup"><span data-stu-id="9ede1-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ede1-132"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ede1-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ede1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9ede1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ede1-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ede1-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ede1-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9ede1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ede1-136">CIM \_ 作業系統</span><span class="sxs-lookup"><span data-stu-id="9ede1-136">CIM\_OperatingSystem</span></span>](reboot-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="9ede1-137">**CIM \_ 作業系統**</span><span class="sxs-lookup"><span data-stu-id="9ede1-137">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> </dl>

 

