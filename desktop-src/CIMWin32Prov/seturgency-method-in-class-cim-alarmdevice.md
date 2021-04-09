---
description: SetUrgency 方法會設定警示所需的緊急程度等級。
ms.assetid: ac2e7fda-1317-440a-adbd-1ef0844d124c
ms.tgt_platform: multiple
title: CIM_AlarmDevice 類別的 SetUrgency 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice.SetUrgency
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35918677e210ac2fe7ac4798a04db9dc628f5fa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936292"
---
# <a name="seturgency-method-of-the-cim_alarmdevice-class"></a><span data-ttu-id="9d201-103">CIM AlarmDevice 類別的 SetUrgency 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9d201-103">SetUrgency method of the CIM\_AlarmDevice class</span></span>

<span data-ttu-id="9d201-104">**SetUrgency** 方法會設定警示所需的緊急程度等級。</span><span class="sxs-lookup"><span data-stu-id="9d201-104">The **SetUrgency** method sets the desired urgency level for an alarm.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9d201-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="9d201-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9d201-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="9d201-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9d201-107">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="9d201-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9d201-108">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="9d201-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9d201-109">語法</span><span class="sxs-lookup"><span data-stu-id="9d201-109">Syntax</span></span>


```mof
uint32 SetUrgency(
  [in] uint16 RequestedUrgency
);
```



## <a name="parameters"></a><span data-ttu-id="9d201-110">參數</span><span class="sxs-lookup"><span data-stu-id="9d201-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d201-111">*RequestedUrgency* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9d201-111">*RequestedUrgency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d201-112">警示閃爍、震動或發出聲音聲的相對頻率。</span><span class="sxs-lookup"><span data-stu-id="9d201-112">Relative frequency at which the alarm flashes, vibrates, or emits audible tones.</span></span> <span data-ttu-id="9d201-113">下列值來自 [**CIM \_ AlarmDevice**](cim-alarmdevice.md)中的 **緊迫** 屬性。</span><span class="sxs-lookup"><span data-stu-id="9d201-113">The following values are from the **Urgency** property in [**CIM\_AlarmDevice**](cim-alarmdevice.md).</span></span>

<dt>

<span data-ttu-id="9d201-114">0</span><span class="sxs-lookup"><span data-stu-id="9d201-114">0</span></span>
</dt> <dd>

<span data-ttu-id="9d201-115">不明。</span><span class="sxs-lookup"><span data-stu-id="9d201-115">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="9d201-116">1</span><span class="sxs-lookup"><span data-stu-id="9d201-116">1</span></span>
</dt> <dd>

<span data-ttu-id="9d201-117">其他。</span><span class="sxs-lookup"><span data-stu-id="9d201-117">Other.</span></span>

</dd> <dt>

<span data-ttu-id="9d201-118">2</span><span class="sxs-lookup"><span data-stu-id="9d201-118">2</span></span>
</dt> <dd>

<span data-ttu-id="9d201-119">不支援。</span><span class="sxs-lookup"><span data-stu-id="9d201-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9d201-120">3</span><span class="sxs-lookup"><span data-stu-id="9d201-120">3</span></span>
</dt> <dd>

<span data-ttu-id="9d201-121">資訊。</span><span class="sxs-lookup"><span data-stu-id="9d201-121">Informational.</span></span>

</dd> <dt>

<span data-ttu-id="9d201-122">4</span><span class="sxs-lookup"><span data-stu-id="9d201-122">4</span></span>
</dt> <dd>

<span data-ttu-id="9d201-123">非關鍵性。</span><span class="sxs-lookup"><span data-stu-id="9d201-123">Non-critical.</span></span>

</dd> <dt>

<span data-ttu-id="9d201-124">5</span><span class="sxs-lookup"><span data-stu-id="9d201-124">5</span></span>
</dt> <dd>

<span data-ttu-id="9d201-125">嚴重。</span><span class="sxs-lookup"><span data-stu-id="9d201-125">Critical.</span></span>

</dd> <dt>

<span data-ttu-id="9d201-126">6</span><span class="sxs-lookup"><span data-stu-id="9d201-126">6</span></span>
</dt> <dd>

<span data-ttu-id="9d201-127">無法.</span><span class="sxs-lookup"><span data-stu-id="9d201-127">Unrecoverable.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d201-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="9d201-128">Return value</span></span>

<span data-ttu-id="9d201-129">在成功時傳回 0 (零) 的值，如果不支援要求的緊急等級，則傳回 1 (一個) ，以及指定錯誤的任何其他數位。</span><span class="sxs-lookup"><span data-stu-id="9d201-129">Returns a value of 0 (zero) on success, 1 (one) if the requested urgency level is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d201-130">備註</span><span class="sxs-lookup"><span data-stu-id="9d201-130">Remarks</span></span>

<span data-ttu-id="9d201-131">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="9d201-131">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="9d201-132">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="9d201-132">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="9d201-133">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="9d201-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9d201-134">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9d201-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d201-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d201-135">Requirements</span></span>



| <span data-ttu-id="9d201-136">需求</span><span class="sxs-lookup"><span data-stu-id="9d201-136">Requirement</span></span> | <span data-ttu-id="9d201-137">值</span><span class="sxs-lookup"><span data-stu-id="9d201-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d201-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d201-138">Minimum supported client</span></span><br/> | <span data-ttu-id="9d201-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d201-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9d201-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d201-140">Minimum supported server</span></span><br/> | <span data-ttu-id="9d201-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d201-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9d201-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="9d201-142">Namespace</span></span><br/>                | <span data-ttu-id="9d201-143">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9d201-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9d201-144">MOF</span><span class="sxs-lookup"><span data-stu-id="9d201-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d201-145"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d201-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d201-146">DLL</span><span class="sxs-lookup"><span data-stu-id="9d201-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d201-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d201-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d201-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d201-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d201-149">CIM \_ AlarmDevice</span><span class="sxs-lookup"><span data-stu-id="9d201-149">CIM\_AlarmDevice</span></span>](seturgency-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[<span data-ttu-id="9d201-150">**CIM \_ AlarmDevice**</span><span class="sxs-lookup"><span data-stu-id="9d201-150">**CIM\_AlarmDevice**</span></span>](cim-alarmdevice.md)
</dt> </dl>

 

