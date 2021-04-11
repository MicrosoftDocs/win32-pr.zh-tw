---
description: CIM 動作類別的 Invoke 方法 \_ 會採取特定動作。 方法如何執行此動作的詳細資料是執行特定的。
ms.assetid: 4f0be560-bd78-4c7f-b6e3-ca86837a84f9
ms.tgt_platform: multiple
title: CIM_Action 類別的 Invoke 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Action.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e02e414fb05e0dd4ea97c3e3a4d87659fed4c963
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847202"
---
# <a name="invoke-method-of-the-cim_action-class"></a><span data-ttu-id="f7a79-104">CIM 動作類別的 Invoke 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f7a79-104">Invoke method of the CIM\_Action class</span></span>

<span data-ttu-id="f7a79-105">[**CIM \_ 動作**](cim-action.md)類別的 **Invoke** 方法會採取特定動作。</span><span class="sxs-lookup"><span data-stu-id="f7a79-105">The **Invoke** method of the [**CIM\_Action**](cim-action.md) class takes a particular action.</span></span> <span data-ttu-id="f7a79-106">方法如何執行此動作的詳細資料是執行特定的。</span><span class="sxs-lookup"><span data-stu-id="f7a79-106">The details of how the method performs the action is implementation-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f7a79-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="f7a79-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f7a79-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="f7a79-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f7a79-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="f7a79-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f7a79-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="f7a79-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f7a79-111">語法</span><span class="sxs-lookup"><span data-stu-id="f7a79-111">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="f7a79-112">參數</span><span class="sxs-lookup"><span data-stu-id="f7a79-112">Parameters</span></span>

<span data-ttu-id="f7a79-113">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f7a79-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f7a79-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f7a79-114">Return value</span></span>

<span data-ttu-id="f7a79-115">在成功時傳回 0 (零) 的值，如果不支援此方法，則傳回 1 (一個) ，以及指定錯誤的任何其他數位。</span><span class="sxs-lookup"><span data-stu-id="f7a79-115">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7a79-116">備註</span><span class="sxs-lookup"><span data-stu-id="f7a79-116">Remarks</span></span>

<span data-ttu-id="f7a79-117">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="f7a79-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f7a79-118">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="f7a79-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="f7a79-119">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="f7a79-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f7a79-120">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f7a79-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7a79-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7a79-121">Requirements</span></span>



| <span data-ttu-id="f7a79-122">需求</span><span class="sxs-lookup"><span data-stu-id="f7a79-122">Requirement</span></span> | <span data-ttu-id="f7a79-123">值</span><span class="sxs-lookup"><span data-stu-id="f7a79-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7a79-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7a79-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f7a79-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7a79-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f7a79-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7a79-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f7a79-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7a79-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f7a79-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="f7a79-128">Namespace</span></span><br/>                | <span data-ttu-id="f7a79-129">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f7a79-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f7a79-130">MOF</span><span class="sxs-lookup"><span data-stu-id="f7a79-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7a79-131"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7a79-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7a79-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f7a79-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7a79-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7a79-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7a79-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7a79-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7a79-135">CIM \_ 動作</span><span class="sxs-lookup"><span data-stu-id="f7a79-135">CIM\_Action</span></span>](invoke-method-in-class-cim-action.md)
</dt> <dt>

[<span data-ttu-id="f7a79-136">**CIM \_ 動作**</span><span class="sxs-lookup"><span data-stu-id="f7a79-136">**CIM\_Action**</span></span>](cim-action.md)
</dt> <dt>

[<span data-ttu-id="f7a79-137">CIM 類別</span><span class="sxs-lookup"><span data-stu-id="f7a79-137">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

