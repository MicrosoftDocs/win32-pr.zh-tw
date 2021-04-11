---
description: ResetCounter 方法會重設錯誤和警告計數器。
ms.assetid: 5bc6c939-cd97-40ca-a16c-5227e7f27c76
ms.tgt_platform: multiple
title: CIM_DeviceErrorCounts 類別的 ResetCounter 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts.ResetCounter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 386547362f5a7aa52bddfbf9df3af01949aecbdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847085"
---
# <a name="resetcounter-method-of-the-cim_deviceerrorcounts-class"></a><span data-ttu-id="2b054-103">CIM DeviceErrorCounts 類別的 ResetCounter 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2b054-103">ResetCounter method of the CIM\_DeviceErrorCounts class</span></span>

<span data-ttu-id="2b054-104">**ResetCounter** 方法會重設錯誤和警告計數器。</span><span class="sxs-lookup"><span data-stu-id="2b054-104">The **ResetCounter** method resets the error and warning counters.</span></span> <span data-ttu-id="2b054-105">使用方法，如此一來，邏輯裝置的檢測（表格列出錯誤和警告）也可以重設其內部處理和計數器。</span><span class="sxs-lookup"><span data-stu-id="2b054-105">A method is used so that the logical device's instrumentation, which tabulates the errors and warnings, can also reset its internal processing and counters.</span></span> <span data-ttu-id="2b054-106">在子類別中，可以使用方法上的 **ValueMap** 辨識符號來指定可能的傳回碼組。</span><span class="sxs-lookup"><span data-stu-id="2b054-106">In a subclass, the set of possible return codes can be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="2b054-107">您也可以在子類別中，以 **值** 陣列限定詞的形式指定要轉譯之 **ValueMap** 內容的字串。</span><span class="sxs-lookup"><span data-stu-id="2b054-107">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2b054-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="2b054-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2b054-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="2b054-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2b054-110">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="2b054-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2b054-111">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="2b054-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2b054-112">語法</span><span class="sxs-lookup"><span data-stu-id="2b054-112">Syntax</span></span>


```mof
uint32 ResetCounter(
  [in] uint16 SelectedCounter
);
```



## <a name="parameters"></a><span data-ttu-id="2b054-113">參數</span><span class="sxs-lookup"><span data-stu-id="2b054-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b054-114">*SelectedCounter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b054-114">*SelectedCounter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b054-115">要重設的錯誤計數器。</span><span class="sxs-lookup"><span data-stu-id="2b054-115">Error counter to reset.</span></span>

<dt>

<span id="All"></span><span id="all"></span><span id="ALL"></span>

<span data-ttu-id="2b054-116">**所有** (0) </span><span class="sxs-lookup"><span data-stu-id="2b054-116">**All** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Indeterminate_Error_Counter"></span><span id="indeterminate_error_counter"></span><span id="INDETERMINATE_ERROR_COUNTER"></span>

<span data-ttu-id="2b054-117">**不定錯誤計數器** (1) </span><span class="sxs-lookup"><span data-stu-id="2b054-117">**Indeterminate Error Counter** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical_Error_Counter"></span><span id="critical_error_counter"></span><span id="CRITICAL_ERROR_COUNTER"></span>

<span data-ttu-id="2b054-118">**重大錯誤計數器** (2) </span><span class="sxs-lookup"><span data-stu-id="2b054-118">**Critical Error Counter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Major_Error_Counter"></span><span id="major_error_counter"></span><span id="MAJOR_ERROR_COUNTER"></span>

<span data-ttu-id="2b054-119">**主要錯誤計數器** (3) </span><span class="sxs-lookup"><span data-stu-id="2b054-119">**Major Error Counter** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Minor_Error_Counter"></span><span id="minor_error_counter"></span><span id="MINOR_ERROR_COUNTER"></span>

<span data-ttu-id="2b054-120">**次要錯誤計數器** (4) </span><span class="sxs-lookup"><span data-stu-id="2b054-120">**Minor Error Counter** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning_Counter"></span><span id="warning_counter"></span><span id="WARNING_COUNTER"></span>

<span data-ttu-id="2b054-121">**警告計數器** (5) </span><span class="sxs-lookup"><span data-stu-id="2b054-121">**Warning Counter** (5)</span></span>


<span data-ttu-id="2b054-122"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2b054-122"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="2b054-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b054-123">Return value</span></span>

<span data-ttu-id="2b054-124">如果成功，則傳回 0 (零) 如果不支援則為 1 (一個) ，如果發生錯誤，則傳回任何其他值。</span><span class="sxs-lookup"><span data-stu-id="2b054-124">Returns 0 (zero) if successful, 1 (one) if not supported, and any other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b054-125">備註</span><span class="sxs-lookup"><span data-stu-id="2b054-125">Remarks</span></span>

<span data-ttu-id="2b054-126">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="2b054-126">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="2b054-127">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="2b054-127">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="2b054-128">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="2b054-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2b054-129">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="2b054-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b054-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b054-130">Requirements</span></span>



| <span data-ttu-id="2b054-131">需求</span><span class="sxs-lookup"><span data-stu-id="2b054-131">Requirement</span></span> | <span data-ttu-id="2b054-132">值</span><span class="sxs-lookup"><span data-stu-id="2b054-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b054-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b054-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2b054-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b054-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2b054-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b054-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2b054-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b054-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2b054-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="2b054-137">Namespace</span></span><br/>                | <span data-ttu-id="2b054-138">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2b054-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2b054-139">MOF</span><span class="sxs-lookup"><span data-stu-id="2b054-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b054-140"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b054-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b054-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2b054-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b054-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b054-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b054-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b054-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b054-144">CIM \_ DeviceErrorCounts</span><span class="sxs-lookup"><span data-stu-id="2b054-144">CIM\_DeviceErrorCounts</span></span>](resetcounter-method-in-class-cim-deviceerrorcounts.md)
</dt> <dt>

[<span data-ttu-id="2b054-145">**CIM \_ DeviceErrorCounts**</span><span class="sxs-lookup"><span data-stu-id="2b054-145">**CIM\_DeviceErrorCounts**</span></span>](cim-deviceerrorcounts.md)
</dt> </dl>

 

