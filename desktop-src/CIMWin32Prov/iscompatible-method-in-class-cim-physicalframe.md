---
description: 確認參考的實體框架是否可包含或插入實體封裝中。
ms.assetid: 8102569d-a956-445a-ae42-23eb206ba224
ms.tgt_platform: multiple
title: CIM_PhysicalFrame 類別的 IsCompatible 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalFrame.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 121405e66a9361e832f6accb24ca6e303bb8e280
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936210"
---
# <a name="iscompatible-method-of-the-cim_physicalframe-class"></a><span data-ttu-id="88ea9-103">CIM PhysicalFrame 類別的 IsCompatible 方法 \_</span><span class="sxs-lookup"><span data-stu-id="88ea9-103">IsCompatible method of the CIM\_PhysicalFrame class</span></span>

<span data-ttu-id="88ea9-104">**IsCompatible** 方法會驗證參考的實體框架是否可包含或插入實體封裝中。</span><span class="sxs-lookup"><span data-stu-id="88ea9-104">The **IsCompatible** method verifies whether the referenced physical frame can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="88ea9-105">在子類別中，可以使用方法上的 **ValueMap** 辨識符號來指定可能的傳回碼集。</span><span class="sxs-lookup"><span data-stu-id="88ea9-105">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="88ea9-106">您也可以在子類別中，以 **值** 陣列限定詞的形式指定要轉譯之 **ValueMap** 內容的字串。</span><span class="sxs-lookup"><span data-stu-id="88ea9-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="88ea9-107">這個方法繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。</span><span class="sxs-lookup"><span data-stu-id="88ea9-107">This method is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="88ea9-108">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="88ea9-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="88ea9-109">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="88ea9-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="88ea9-110">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="88ea9-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="88ea9-111">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="88ea9-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="88ea9-112">語法</span><span class="sxs-lookup"><span data-stu-id="88ea9-112">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="88ea9-113">參數</span><span class="sxs-lookup"><span data-stu-id="88ea9-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88ea9-114">*ElementToCheck* \[在\]</span><span class="sxs-lookup"><span data-stu-id="88ea9-114">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88ea9-115">**IsCompatible** 方法執行所在實體元素的參考。</span><span class="sxs-lookup"><span data-stu-id="88ea9-115">Reference to the physical element that the **IsCompatible** method runs against.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88ea9-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="88ea9-116">Return value</span></span>

<span data-ttu-id="88ea9-117">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="88ea9-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="88ea9-118">備註</span><span class="sxs-lookup"><span data-stu-id="88ea9-118">Remarks</span></span>

<span data-ttu-id="88ea9-119">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="88ea9-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="88ea9-120">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="88ea9-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="88ea9-121">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="88ea9-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="88ea9-122">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="88ea9-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="88ea9-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="88ea9-123">Requirements</span></span>



| <span data-ttu-id="88ea9-124">需求</span><span class="sxs-lookup"><span data-stu-id="88ea9-124">Requirement</span></span> | <span data-ttu-id="88ea9-125">值</span><span class="sxs-lookup"><span data-stu-id="88ea9-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88ea9-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="88ea9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="88ea9-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88ea9-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="88ea9-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="88ea9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="88ea9-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88ea9-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="88ea9-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="88ea9-130">Namespace</span></span><br/>                | <span data-ttu-id="88ea9-131">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="88ea9-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="88ea9-132">MOF</span><span class="sxs-lookup"><span data-stu-id="88ea9-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88ea9-133"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="88ea9-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="88ea9-134">DLL</span><span class="sxs-lookup"><span data-stu-id="88ea9-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88ea9-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88ea9-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88ea9-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88ea9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88ea9-137">**CIM \_ PhysicalFrame**</span><span class="sxs-lookup"><span data-stu-id="88ea9-137">**CIM\_PhysicalFrame**</span></span>](iscompatible-method-in-class-cim-physicalframe.md)
</dt> <dt>

[<span data-ttu-id="88ea9-138">**CIM \_ PhysicalFrame**</span><span class="sxs-lookup"><span data-stu-id="88ea9-138">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> </dl>

 

