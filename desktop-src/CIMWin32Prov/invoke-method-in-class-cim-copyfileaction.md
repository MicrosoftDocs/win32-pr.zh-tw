---
description: CIM CopyFileAction 類別的 Invoke 方法 \_ 會採取特定的動作。 如何執行此動作的詳細資料是執行特定的。 此方法繼承自 CIM \_ 動作。
ms.assetid: b948e9ed-332d-4ac5-be7f-88b7f46f5f1d
ms.tgt_platform: multiple
title: CIM_CopyFileAction 類別的 Invoke 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CopyFileAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b88ddafd0420a40af8b815aab26849572cb7c019
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847201"
---
# <a name="invoke-method-of-the-cim_copyfileaction-class"></a><span data-ttu-id="733fd-105">CIM CopyFileAction 類別的 Invoke 方法 \_</span><span class="sxs-lookup"><span data-stu-id="733fd-105">Invoke method of the CIM\_CopyFileAction class</span></span>

<span data-ttu-id="733fd-106">[**CIM \_ CopyFileAction**](cim-copyfileaction.md)類別的 **Invoke** 方法會採取特定的動作。</span><span class="sxs-lookup"><span data-stu-id="733fd-106">The **Invoke** method of the [**CIM\_CopyFileAction**](cim-copyfileaction.md) class takes a particular action.</span></span> <span data-ttu-id="733fd-107">如何執行此動作的詳細資料是執行特定的。</span><span class="sxs-lookup"><span data-stu-id="733fd-107">Details about how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="733fd-108">此方法繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="733fd-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="733fd-109">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="733fd-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="733fd-110">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="733fd-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="733fd-111">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="733fd-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="733fd-112">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="733fd-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="733fd-113">語法</span><span class="sxs-lookup"><span data-stu-id="733fd-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="733fd-114">參數</span><span class="sxs-lookup"><span data-stu-id="733fd-114">Parameters</span></span>

<span data-ttu-id="733fd-115">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="733fd-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="733fd-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="733fd-116">Return value</span></span>

<span data-ttu-id="733fd-117">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="733fd-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="733fd-118">備註</span><span class="sxs-lookup"><span data-stu-id="733fd-118">Remarks</span></span>

<span data-ttu-id="733fd-119">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="733fd-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="733fd-120">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="733fd-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="733fd-121">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="733fd-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="733fd-122">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="733fd-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="733fd-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="733fd-123">Requirements</span></span>



| <span data-ttu-id="733fd-124">需求</span><span class="sxs-lookup"><span data-stu-id="733fd-124">Requirement</span></span> | <span data-ttu-id="733fd-125">值</span><span class="sxs-lookup"><span data-stu-id="733fd-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="733fd-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="733fd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="733fd-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="733fd-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="733fd-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="733fd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="733fd-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="733fd-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="733fd-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="733fd-130">Namespace</span></span><br/>                | <span data-ttu-id="733fd-131">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="733fd-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="733fd-132">MOF</span><span class="sxs-lookup"><span data-stu-id="733fd-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="733fd-133"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="733fd-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="733fd-134">DLL</span><span class="sxs-lookup"><span data-stu-id="733fd-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="733fd-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="733fd-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="733fd-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="733fd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="733fd-137">**CIM \_ CopyFileAction**</span><span class="sxs-lookup"><span data-stu-id="733fd-137">**CIM\_CopyFileAction**</span></span>](invoke-method-in-class-cim-copyfileaction.md)
</dt> <dt>

[<span data-ttu-id="733fd-138">**CIM \_ CopyFileAction**</span><span class="sxs-lookup"><span data-stu-id="733fd-138">**CIM\_CopyFileAction**</span></span>](cim-copyfileaction.md)
</dt> </dl>

 

