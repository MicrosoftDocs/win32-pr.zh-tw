---
description: CIM RebootAction 類別的 Invoke 方法 \_ 會採取特定的動作。 方法執行動作的詳細資料是特定的實作為。 此方法繼承自 CIM \_ 動作。
ms.assetid: 27b6571e-94fe-423e-89ab-5ba2bc632882
ms.tgt_platform: multiple
title: CIM_RebootAction 類別的 Invoke 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RebootAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e68849a486cc6a5b61dc55cf86e259e2f58435e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985388"
---
# <a name="invoke-method-of-the-cim_rebootaction-class"></a><span data-ttu-id="0af7a-105">CIM RebootAction 類別的 Invoke 方法 \_</span><span class="sxs-lookup"><span data-stu-id="0af7a-105">Invoke method of the CIM\_RebootAction class</span></span>

<span data-ttu-id="0af7a-106">[**CIM \_ RebootAction**](cim-rebootaction.md)類別的 **Invoke** 方法會採取特定的動作。</span><span class="sxs-lookup"><span data-stu-id="0af7a-106">The **Invoke** method of the [**CIM\_RebootAction**](cim-rebootaction.md) class takes a particular action.</span></span> <span data-ttu-id="0af7a-107">方法執行動作的詳細資料是特定的實作為。</span><span class="sxs-lookup"><span data-stu-id="0af7a-107">The details of how the method performs the action are implementation specific.</span></span> <span data-ttu-id="0af7a-108">此方法繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="0af7a-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0af7a-109">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="0af7a-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0af7a-110">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="0af7a-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0af7a-111">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="0af7a-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0af7a-112">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="0af7a-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0af7a-113">語法</span><span class="sxs-lookup"><span data-stu-id="0af7a-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="0af7a-114">參數</span><span class="sxs-lookup"><span data-stu-id="0af7a-114">Parameters</span></span>

<span data-ttu-id="0af7a-115">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0af7a-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0af7a-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="0af7a-116">Return value</span></span>

<span data-ttu-id="0af7a-117">在成功時傳回 0 (零) 的整數值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="0af7a-117">Returns an integer value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="0af7a-118">備註</span><span class="sxs-lookup"><span data-stu-id="0af7a-118">Remarks</span></span>

<span data-ttu-id="0af7a-119">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="0af7a-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0af7a-120">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="0af7a-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="0af7a-121">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="0af7a-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0af7a-122">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="0af7a-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0af7a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="0af7a-123">Requirements</span></span>



| <span data-ttu-id="0af7a-124">需求</span><span class="sxs-lookup"><span data-stu-id="0af7a-124">Requirement</span></span> | <span data-ttu-id="0af7a-125">值</span><span class="sxs-lookup"><span data-stu-id="0af7a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0af7a-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0af7a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0af7a-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0af7a-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0af7a-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0af7a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0af7a-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0af7a-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0af7a-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="0af7a-130">Namespace</span></span><br/>                | <span data-ttu-id="0af7a-131">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0af7a-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0af7a-132">MOF</span><span class="sxs-lookup"><span data-stu-id="0af7a-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0af7a-133"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0af7a-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0af7a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0af7a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0af7a-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0af7a-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0af7a-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0af7a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0af7a-137">CIM \_ RebootAction</span><span class="sxs-lookup"><span data-stu-id="0af7a-137">CIM\_RebootAction</span></span>](invoke-method-in-class-cim-rebootaction.md)
</dt> <dt>

[<span data-ttu-id="0af7a-138">**CIM \_ RebootAction**</span><span class="sxs-lookup"><span data-stu-id="0af7a-138">**CIM\_RebootAction**</span></span>](cim-rebootaction.md)
</dt> </dl>

 

