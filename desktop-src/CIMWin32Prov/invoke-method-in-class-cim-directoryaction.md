---
description: CIM DirectoryAction 類別的 Invoke 方法 \_ 會採取特定的動作。 方法如何執行此動作的詳細資料是執行特定的。 此方法繼承自 CIM \_ 動作。
ms.assetid: e919dfdb-a52d-4bcb-abff-e1273c406226
ms.tgt_platform: multiple
title: CIM_DirectoryAction 類別的 Invoke 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f30184fe46cd8e8b9a595545ccba9a7d738af18e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847199"
---
# <a name="invoke-method-of-the-cim_directoryaction-class"></a><span data-ttu-id="5ca65-105">CIM DirectoryAction 類別的 Invoke 方法 \_</span><span class="sxs-lookup"><span data-stu-id="5ca65-105">Invoke method of the CIM\_DirectoryAction class</span></span>

<span data-ttu-id="5ca65-106">[**CIM \_ DirectoryAction**](cim-directoryaction.md)類別的 **Invoke** 方法會採取特定的動作。</span><span class="sxs-lookup"><span data-stu-id="5ca65-106">The **Invoke** method of the [**CIM\_DirectoryAction**](cim-directoryaction.md) class takes a particular action.</span></span> <span data-ttu-id="5ca65-107">方法如何執行此動作的詳細資料是執行特定的。</span><span class="sxs-lookup"><span data-stu-id="5ca65-107">Details of how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="5ca65-108">此方法繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="5ca65-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5ca65-109">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="5ca65-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5ca65-110">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="5ca65-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5ca65-111">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="5ca65-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5ca65-112">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="5ca65-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5ca65-113">語法</span><span class="sxs-lookup"><span data-stu-id="5ca65-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="5ca65-114">參數</span><span class="sxs-lookup"><span data-stu-id="5ca65-114">Parameters</span></span>

<span data-ttu-id="5ca65-115">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5ca65-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5ca65-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5ca65-116">Return value</span></span>

<span data-ttu-id="5ca65-117">在成功時傳回 0 (零) 的值，如果不支援此方法，則傳回 1 (一個) ，以及指定錯誤的任何其他數位。</span><span class="sxs-lookup"><span data-stu-id="5ca65-117">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ca65-118">備註</span><span class="sxs-lookup"><span data-stu-id="5ca65-118">Remarks</span></span>

<span data-ttu-id="5ca65-119">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="5ca65-119">WMI does not implement this class.</span></span>

<span data-ttu-id="5ca65-120">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="5ca65-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5ca65-121">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5ca65-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ca65-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ca65-122">Requirements</span></span>



| <span data-ttu-id="5ca65-123">需求</span><span class="sxs-lookup"><span data-stu-id="5ca65-123">Requirement</span></span> | <span data-ttu-id="5ca65-124">值</span><span class="sxs-lookup"><span data-stu-id="5ca65-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca65-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ca65-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5ca65-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ca65-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5ca65-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ca65-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5ca65-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ca65-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5ca65-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="5ca65-129">Namespace</span></span><br/>                | <span data-ttu-id="5ca65-130">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5ca65-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5ca65-131">MOF</span><span class="sxs-lookup"><span data-stu-id="5ca65-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ca65-132"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ca65-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ca65-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5ca65-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ca65-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ca65-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ca65-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ca65-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ca65-136">CIM \_ DirectoryAction</span><span class="sxs-lookup"><span data-stu-id="5ca65-136">CIM\_DirectoryAction</span></span>](invoke-method-in-class-cim-directoryaction.md)
</dt> <dt>

[<span data-ttu-id="5ca65-137">**CIM \_ DirectoryAction**</span><span class="sxs-lookup"><span data-stu-id="5ca65-137">**CIM\_DirectoryAction**</span></span>](cim-directoryaction.md)
</dt> </dl>

 

