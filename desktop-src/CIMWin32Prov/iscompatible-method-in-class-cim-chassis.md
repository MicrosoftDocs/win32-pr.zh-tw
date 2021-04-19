---
description: 確認參考的實體底座是否可包含或插入實體套件中。
ms.assetid: 9a1aa1b7-2b95-4887-9d14-e416ff69f9df
ms.tgt_platform: multiple
title: CIM_Chassis 類別的 IsCompatible 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chassis.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8796582b153a7283429715569eeed91e4dd38fc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971126"
---
# <a name="iscompatible-method-of-the-cim_chassis-class"></a><span data-ttu-id="a34af-103">CIM 底座類別的 IsCompatible 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a34af-103">IsCompatible method of the CIM\_Chassis class</span></span>

<span data-ttu-id="a34af-104">**IsCompatible** 方法會驗證參考的實體底座是否可包含或插入實體套件中。</span><span class="sxs-lookup"><span data-stu-id="a34af-104">The **IsCompatible** method verifies whether the referenced physical chassis can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="a34af-105">在子類別中，可以使用方法上的 [**ValueMap**](/windows/desktop/WmiSdk/standard-qualifiers) 辨識符號來指定可能的傳回碼集。</span><span class="sxs-lookup"><span data-stu-id="a34af-105">In a subclass, the set of possible return codes can be specified by using a [**ValueMap**](/windows/desktop/WmiSdk/standard-qualifiers) qualifier on the method.</span></span> <span data-ttu-id="a34af-106">您也可以在子類別中，以 **值** 陣列限定詞的形式指定要轉譯之 **ValueMap** 內容的字串。</span><span class="sxs-lookup"><span data-stu-id="a34af-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="a34af-107">這個方法繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="a34af-107">This method is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a34af-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="a34af-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a34af-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="a34af-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a34af-110">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="a34af-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a34af-111">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="a34af-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a34af-112">語法</span><span class="sxs-lookup"><span data-stu-id="a34af-112">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="a34af-113">參數</span><span class="sxs-lookup"><span data-stu-id="a34af-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a34af-114">*ElementToCheck* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a34af-114">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a34af-115">要檢查相容性之實體元素的參考。</span><span class="sxs-lookup"><span data-stu-id="a34af-115">Reference to the physical element for which to check compatibility.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a34af-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="a34af-116">Return value</span></span>

<span data-ttu-id="a34af-117">在成功時傳回 0 (零) 的值; 如果不支援要求，則傳回 1 (一個) ，以及指定錯誤的任何其他數位。</span><span class="sxs-lookup"><span data-stu-id="a34af-117">Returns a value of 0 (zero) on success, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a34af-118">備註</span><span class="sxs-lookup"><span data-stu-id="a34af-118">Remarks</span></span>

<span data-ttu-id="a34af-119">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="a34af-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a34af-120">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="a34af-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a34af-121">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="a34af-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a34af-122">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a34af-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a34af-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a34af-123">Requirements</span></span>



| <span data-ttu-id="a34af-124">需求</span><span class="sxs-lookup"><span data-stu-id="a34af-124">Requirement</span></span> | <span data-ttu-id="a34af-125">值</span><span class="sxs-lookup"><span data-stu-id="a34af-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a34af-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a34af-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a34af-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a34af-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a34af-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a34af-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a34af-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a34af-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a34af-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="a34af-130">Namespace</span></span><br/>                | <span data-ttu-id="a34af-131">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a34af-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a34af-132">MOF</span><span class="sxs-lookup"><span data-stu-id="a34af-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a34af-133"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a34af-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a34af-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a34af-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a34af-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a34af-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a34af-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a34af-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a34af-137">**CIM \_ 底座**</span><span class="sxs-lookup"><span data-stu-id="a34af-137">**CIM\_Chassis**</span></span>](iscompatible-method-in-class-cim-chassis.md)
</dt> <dt>

[<span data-ttu-id="a34af-138">**CIM \_ 底座**</span><span class="sxs-lookup"><span data-stu-id="a34af-138">**CIM\_Chassis**</span></span>](cim-chassis.md)
</dt> </dl>

 

