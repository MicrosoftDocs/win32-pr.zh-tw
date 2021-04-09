---
description: CIM VersionCompatibilityCheck 類別的 Invoke 方法會 \_ 評估特定檢查。
ms.assetid: d1ccc248-340e-4277-9696-063e1e2bf915
ms.tgt_platform: multiple
title: CIM_VersionCompatibilityCheck 類別的 Invoke 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VersionCompatibilityCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bccbb6072ae84a238b60247daf6b81cfaa74e608
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847196"
---
# <a name="invoke-method-of-the-cim_versioncompatibilitycheck-class"></a><span data-ttu-id="a74bf-103">CIM VersionCompatibilityCheck 類別的 Invoke 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a74bf-103">Invoke method of the CIM\_VersionCompatibilityCheck class</span></span>

<span data-ttu-id="a74bf-104">[**CIM \_ VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md)類別的 **Invoke** 方法會評估特定檢查。</span><span class="sxs-lookup"><span data-stu-id="a74bf-104">The **Invoke** method of the [**CIM\_VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) class evaluates a particular check.</span></span> <span data-ttu-id="a74bf-105">方法會在 CIM 內容中評估特定檢查的詳細資料，由非抽象 [**cim \_ 檢查**](cim-check.md) 子類別描述。</span><span class="sxs-lookup"><span data-stu-id="a74bf-105">The details of how the method evaluates a particular check in a CIM context are described by the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span> <span data-ttu-id="a74bf-106">此方法繼承自 **CIM \_ 檢查**。</span><span class="sxs-lookup"><span data-stu-id="a74bf-106">This method is inherited from **CIM\_Check**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a74bf-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="a74bf-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a74bf-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="a74bf-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a74bf-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="a74bf-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a74bf-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="a74bf-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a74bf-111">語法</span><span class="sxs-lookup"><span data-stu-id="a74bf-111">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="a74bf-112">參數</span><span class="sxs-lookup"><span data-stu-id="a74bf-112">Parameters</span></span>

<span data-ttu-id="a74bf-113">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a74bf-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a74bf-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a74bf-114">Return value</span></span>

<span data-ttu-id="a74bf-115">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="a74bf-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a74bf-116">備註</span><span class="sxs-lookup"><span data-stu-id="a74bf-116">Remarks</span></span>

<span data-ttu-id="a74bf-117">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="a74bf-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a74bf-118">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="a74bf-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a74bf-119">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="a74bf-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a74bf-120">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a74bf-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a74bf-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a74bf-121">Requirements</span></span>



| <span data-ttu-id="a74bf-122">需求</span><span class="sxs-lookup"><span data-stu-id="a74bf-122">Requirement</span></span> | <span data-ttu-id="a74bf-123">值</span><span class="sxs-lookup"><span data-stu-id="a74bf-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a74bf-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a74bf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a74bf-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a74bf-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a74bf-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a74bf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a74bf-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a74bf-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a74bf-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="a74bf-128">Namespace</span></span><br/>                | <span data-ttu-id="a74bf-129">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a74bf-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a74bf-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a74bf-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a74bf-131"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a74bf-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a74bf-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a74bf-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a74bf-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a74bf-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a74bf-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a74bf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a74bf-135">CIM \_ VersionCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="a74bf-135">CIM\_VersionCompatibilityCheck</span></span>](invoke-method-in-class-cim-versioncompatibilitycheck.md)
</dt> <dt>

[<span data-ttu-id="a74bf-136">**CIM \_ VersionCompatibilityCheck**</span><span class="sxs-lookup"><span data-stu-id="a74bf-136">**CIM\_VersionCompatibilityCheck**</span></span>](cim-versioncompatibilitycheck.md)
</dt> </dl>

 

