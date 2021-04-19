---
description: 確認參考的實體元素是否可包含或插入實體封裝中。
ms.assetid: 406aaa75-b48c-4377-adb5-e900676b6e36
ms.tgt_platform: multiple
title: CIM_PhysicalPackage 類別的 IsCompatible 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalPackage.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1957b8d0c1929ff6f7b4ef8c69fa55ea4ccc83b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973573"
---
# <a name="iscompatible-method-of-the-cim_physicalpackage-class"></a><span data-ttu-id="6420c-103">CIM PhysicalPackage 類別的 IsCompatible 方法 \_</span><span class="sxs-lookup"><span data-stu-id="6420c-103">IsCompatible method of the CIM\_PhysicalPackage class</span></span>

<span data-ttu-id="6420c-104">**IsCompatible** 方法會驗證參考的實體元素是否可包含或插入實體封裝中。</span><span class="sxs-lookup"><span data-stu-id="6420c-104">The **IsCompatible** method verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="6420c-105">在子類別中，可以使用方法上的 **ValueMap** 辨識符號來指定可能的傳回碼集。</span><span class="sxs-lookup"><span data-stu-id="6420c-105">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="6420c-106">您也可以在子類別中，以 **值** 陣列限定詞的形式指定要轉譯之 **ValueMap** 內容的字串。</span><span class="sxs-lookup"><span data-stu-id="6420c-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6420c-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="6420c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6420c-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="6420c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6420c-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="6420c-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6420c-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="6420c-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6420c-111">語法</span><span class="sxs-lookup"><span data-stu-id="6420c-111">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="6420c-112">參數</span><span class="sxs-lookup"><span data-stu-id="6420c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6420c-113">*ElementToCheck* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6420c-113">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6420c-114">**IsCompatible** 方法執行所在實體元素的參考。</span><span class="sxs-lookup"><span data-stu-id="6420c-114">Reference to the physical element that the **IsCompatible** method runs against.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6420c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="6420c-115">Return value</span></span>

<span data-ttu-id="6420c-116">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="6420c-116">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="6420c-117">備註</span><span class="sxs-lookup"><span data-stu-id="6420c-117">Remarks</span></span>

<span data-ttu-id="6420c-118">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="6420c-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="6420c-119">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="6420c-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="6420c-120">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="6420c-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6420c-121">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="6420c-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6420c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="6420c-122">Requirements</span></span>



| <span data-ttu-id="6420c-123">需求</span><span class="sxs-lookup"><span data-stu-id="6420c-123">Requirement</span></span> | <span data-ttu-id="6420c-124">值</span><span class="sxs-lookup"><span data-stu-id="6420c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6420c-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6420c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6420c-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6420c-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6420c-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6420c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6420c-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6420c-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6420c-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="6420c-129">Namespace</span></span><br/>                | <span data-ttu-id="6420c-130">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6420c-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6420c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6420c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6420c-132"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="6420c-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6420c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6420c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6420c-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6420c-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6420c-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6420c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6420c-136">**CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="6420c-136">**CIM\_PhysicalPackage**</span></span>](iscompatible-method-in-class-cim-physicalpackage.md)
</dt> <dt>

[<span data-ttu-id="6420c-137">**CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="6420c-137">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 

