---
description: CIM OSVersionCheck 類別的 Invoke 方法會 \_ 評估特定檢查。 方法會在 CIM 內容中評估特定檢查的詳細資料，由非抽象 CIM \_ 檢查子類別描述。 此方法繼承自 CIM \_ 檢查。
ms.assetid: ff06772c-e40c-49c8-b334-5ee480926245
ms.tgt_platform: multiple
title: CIM_OSVersionCheck 類別的 Invoke 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OSVersionCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 49d6944c4a28c956356fef430e47bc8636082930
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110477"
---
# <a name="invoke-method-of-the-cim_osversioncheck-class"></a><span data-ttu-id="75e3a-105">CIM OSVersionCheck 類別的 Invoke 方法 \_</span><span class="sxs-lookup"><span data-stu-id="75e3a-105">Invoke method of the CIM\_OSVersionCheck class</span></span>

<span data-ttu-id="75e3a-106">[**CIM \_ OSVersionCheck**](cim-osversioncheck.md)類別的 **Invoke** 方法會評估特定檢查。</span><span class="sxs-lookup"><span data-stu-id="75e3a-106">The **Invoke** method of the [**CIM\_OSVersionCheck**](cim-osversioncheck.md) class evaluates a particular check.</span></span> <span data-ttu-id="75e3a-107">方法會在 CIM 內容中評估特定檢查的詳細資料，由非抽象 [**cim \_ 檢查**](cim-check.md) 子類別描述。</span><span class="sxs-lookup"><span data-stu-id="75e3a-107">The details of how the method evaluates a particular check in a CIM context is described by the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span> <span data-ttu-id="75e3a-108">此方法繼承自 **CIM \_ 檢查**。</span><span class="sxs-lookup"><span data-stu-id="75e3a-108">This method is inherited from **CIM\_Check**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="75e3a-109">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="75e3a-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="75e3a-110">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="75e3a-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="75e3a-111">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="75e3a-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="75e3a-112">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="75e3a-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="75e3a-113">語法</span><span class="sxs-lookup"><span data-stu-id="75e3a-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="75e3a-114">參數</span><span class="sxs-lookup"><span data-stu-id="75e3a-114">Parameters</span></span>

<span data-ttu-id="75e3a-115">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="75e3a-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="75e3a-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="75e3a-116">Return value</span></span>

<span data-ttu-id="75e3a-117">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="75e3a-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="75e3a-118">備註</span><span class="sxs-lookup"><span data-stu-id="75e3a-118">Remarks</span></span>

<span data-ttu-id="75e3a-119">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="75e3a-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="75e3a-120">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="75e3a-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="75e3a-121">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="75e3a-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="75e3a-122">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="75e3a-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="75e3a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="75e3a-123">Requirements</span></span>



| <span data-ttu-id="75e3a-124">需求</span><span class="sxs-lookup"><span data-stu-id="75e3a-124">Requirement</span></span> | <span data-ttu-id="75e3a-125">值</span><span class="sxs-lookup"><span data-stu-id="75e3a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75e3a-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75e3a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="75e3a-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75e3a-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="75e3a-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75e3a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="75e3a-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75e3a-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="75e3a-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="75e3a-130">Namespace</span></span><br/>                | <span data-ttu-id="75e3a-131">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="75e3a-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="75e3a-132">MOF</span><span class="sxs-lookup"><span data-stu-id="75e3a-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75e3a-133"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="75e3a-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="75e3a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="75e3a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75e3a-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75e3a-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75e3a-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75e3a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75e3a-137">CIM \_ OSVersionCheck</span><span class="sxs-lookup"><span data-stu-id="75e3a-137">CIM\_OSVersionCheck</span></span>](invoke-method-in-class-cim-osversioncheck.md)
</dt> <dt>

[<span data-ttu-id="75e3a-138">**CIM \_ OSVersionCheck**</span><span class="sxs-lookup"><span data-stu-id="75e3a-138">**CIM\_OSVersionCheck**</span></span>](cim-osversioncheck.md)
</dt> </dl>

 

