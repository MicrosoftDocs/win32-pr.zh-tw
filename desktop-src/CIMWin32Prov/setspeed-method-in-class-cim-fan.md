---
description: SetSpeed 方法會要求風扇速度設定為在方法的輸入參數中指定的值。
ms.assetid: 7dd1cd57-66c5-4b50-9a73-31caf0b824e6
ms.tgt_platform: multiple
title: CIM_Fan 類別的 SetSpeed 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Fan.SetSpeed
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 16d90dbef3a9318ad144303e5720cea0abbde03e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847596"
---
# <a name="setspeed-method-of-the-cim_fan-class"></a><span data-ttu-id="da531-103">CIM 風扇類別的 SetSpeed 方法 \_</span><span class="sxs-lookup"><span data-stu-id="da531-103">SetSpeed method of the CIM\_Fan class</span></span>

<span data-ttu-id="da531-104">**SetSpeed** 方法會要求風扇速度設定為在方法的輸入參數中指定的值。</span><span class="sxs-lookup"><span data-stu-id="da531-104">The **SetSpeed** method requests that the fan speed be set to the value specified in the method's input parameter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da531-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="da531-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="da531-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="da531-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="da531-107">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="da531-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="da531-108">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="da531-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="da531-109">語法</span><span class="sxs-lookup"><span data-stu-id="da531-109">Syntax</span></span>


```mof
uint32 SetSpeed(
  [in] uint64 DesiredSpeed
);
```



## <a name="parameters"></a><span data-ttu-id="da531-110">參數</span><span class="sxs-lookup"><span data-stu-id="da531-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da531-111">*DesiredSpeed* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da531-111">*DesiredSpeed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da531-112">要求的風扇速度，以每分鐘的旋轉。</span><span class="sxs-lookup"><span data-stu-id="da531-112">Requested fan speed, in revolutions per minute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da531-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="da531-113">Return value</span></span>

<span data-ttu-id="da531-114">在成功時傳回 0 (零) 的值; 如果不支援要求，則傳回 1 (一個) ，以及指定錯誤的任何其他數位。</span><span class="sxs-lookup"><span data-stu-id="da531-114">Returns a value of 0 (zero) on success, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="da531-115">備註</span><span class="sxs-lookup"><span data-stu-id="da531-115">Remarks</span></span>

<span data-ttu-id="da531-116">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="da531-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="da531-117">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="da531-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="da531-118">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="da531-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="da531-119">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="da531-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="da531-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="da531-120">Requirements</span></span>



| <span data-ttu-id="da531-121">需求</span><span class="sxs-lookup"><span data-stu-id="da531-121">Requirement</span></span> | <span data-ttu-id="da531-122">值</span><span class="sxs-lookup"><span data-stu-id="da531-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da531-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da531-123">Minimum supported client</span></span><br/> | <span data-ttu-id="da531-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da531-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da531-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da531-125">Minimum supported server</span></span><br/> | <span data-ttu-id="da531-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da531-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da531-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="da531-127">Namespace</span></span><br/>                | <span data-ttu-id="da531-128">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="da531-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="da531-129">MOF</span><span class="sxs-lookup"><span data-stu-id="da531-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da531-130"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="da531-130"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="da531-131">DLL</span><span class="sxs-lookup"><span data-stu-id="da531-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da531-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da531-132"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da531-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da531-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da531-134">CIM \_ 風扇</span><span class="sxs-lookup"><span data-stu-id="da531-134">CIM\_Fan</span></span>](setspeed-method-in-class-cim-fan.md)
</dt> <dt>

[<span data-ttu-id="da531-135">**CIM \_ 風扇**</span><span class="sxs-lookup"><span data-stu-id="da531-135">**CIM\_Fan**</span></span>](cim-fan.md)
</dt> </dl>

 

