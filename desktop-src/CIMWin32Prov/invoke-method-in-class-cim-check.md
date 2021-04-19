---
description: CIM 檢查類別的 Invoke 方法會 \_ 評估特定檢查。
ms.assetid: cf1adeb2-f8a2-4f84-978f-e801bce104ac
ms.tgt_platform: multiple
title: CIM_Check 類別的 Invoke 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Check.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7774fcd1b3ef451fffb34ce9ad10d404e8ea95b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972766"
---
# <a name="invoke-method-of-the-cim_check-class"></a><span data-ttu-id="f722d-103">CIM 檢查類別的 Invoke 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f722d-103">Invoke method of the CIM\_Check class</span></span>

<span data-ttu-id="f722d-104">[**CIM \_ 檢查**](cim-check.md)類別的 **Invoke** 方法會評估特定檢查。</span><span class="sxs-lookup"><span data-stu-id="f722d-104">The **Invoke** method of the [**CIM\_Check**](cim-check.md) class evaluates a particular check.</span></span>

<span data-ttu-id="f722d-105">如需方法如何評估 CIM 內容中特定檢查的詳細資訊，請參閱非抽象 [**cim \_ 檢查**](cim-check.md) 子類別。</span><span class="sxs-lookup"><span data-stu-id="f722d-105">For more information about how the method evaluates a particular check in a CIM context, see the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f722d-106">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="f722d-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f722d-107">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="f722d-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f722d-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="f722d-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f722d-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="f722d-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f722d-110">語法</span><span class="sxs-lookup"><span data-stu-id="f722d-110">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="f722d-111">參數</span><span class="sxs-lookup"><span data-stu-id="f722d-111">Parameters</span></span>

<span data-ttu-id="f722d-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f722d-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f722d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f722d-113">Return value</span></span>

<span data-ttu-id="f722d-114">在成功時傳回 0 (零) 的值，如果不支援此方法，則傳回 1 (一個) ，以及指定錯誤的任何其他數位。</span><span class="sxs-lookup"><span data-stu-id="f722d-114">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f722d-115">備註</span><span class="sxs-lookup"><span data-stu-id="f722d-115">Remarks</span></span>

<span data-ttu-id="f722d-116">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="f722d-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f722d-117">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="f722d-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="f722d-118">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="f722d-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f722d-119">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f722d-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f722d-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="f722d-120">Requirements</span></span>



| <span data-ttu-id="f722d-121">需求</span><span class="sxs-lookup"><span data-stu-id="f722d-121">Requirement</span></span> | <span data-ttu-id="f722d-122">值</span><span class="sxs-lookup"><span data-stu-id="f722d-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f722d-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f722d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f722d-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f722d-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f722d-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f722d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f722d-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f722d-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f722d-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="f722d-127">Namespace</span></span><br/>                | <span data-ttu-id="f722d-128">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f722d-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f722d-129">MOF</span><span class="sxs-lookup"><span data-stu-id="f722d-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f722d-130"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f722d-130"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f722d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f722d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f722d-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f722d-132"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f722d-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f722d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f722d-134">**CIM \_ 檢查**</span><span class="sxs-lookup"><span data-stu-id="f722d-134">**CIM\_Check**</span></span>](invoke-method-in-class-cim-check.md)
</dt> <dt>

[<span data-ttu-id="f722d-135">**CIM \_ 檢查**</span><span class="sxs-lookup"><span data-stu-id="f722d-135">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

