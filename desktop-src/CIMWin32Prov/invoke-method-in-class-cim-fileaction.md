---
description: CIM FileAction 類別的 Invoke 方法 \_ 會採取特定的動作。 方法如何執行此動作的詳細資料是特定的執行方式。 此方法繼承自 CIM \_ 動作。
ms.assetid: f7514d67-4141-4d1a-bdfd-83aa062291aa
ms.tgt_platform: multiple
title: CIM_FileAction 類別的 Invoke 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b1d0a877936a27a681a20e5ffd73da9dda77dcf4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187680"
---
# <a name="invoke-method-of-the-cim_fileaction-class"></a><span data-ttu-id="66890-105">CIM FileAction 類別的 Invoke 方法 \_</span><span class="sxs-lookup"><span data-stu-id="66890-105">Invoke method of the CIM\_FileAction class</span></span>

<span data-ttu-id="66890-106">[**CIM \_ FileAction**](cim-fileaction.md)類別的 **Invoke** 方法會採取特定的動作。</span><span class="sxs-lookup"><span data-stu-id="66890-106">The **Invoke** method of the [**CIM\_FileAction**](cim-fileaction.md) class takes a particular action.</span></span> <span data-ttu-id="66890-107">方法如何執行此動作的詳細資料是特定的執行方式。</span><span class="sxs-lookup"><span data-stu-id="66890-107">Details of how the method performs the action are implementation specific.</span></span> <span data-ttu-id="66890-108">此方法繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="66890-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66890-109">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="66890-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="66890-110">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="66890-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="66890-111">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="66890-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="66890-112">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="66890-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="66890-113">語法</span><span class="sxs-lookup"><span data-stu-id="66890-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="66890-114">參數</span><span class="sxs-lookup"><span data-stu-id="66890-114">Parameters</span></span>

<span data-ttu-id="66890-115">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="66890-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="66890-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="66890-116">Return value</span></span>

<span data-ttu-id="66890-117">在成功時傳回 0 (零) 的值，如果不支援此方法，則傳回 1 (一個) ，以及指定錯誤的任何其他數位。</span><span class="sxs-lookup"><span data-stu-id="66890-117">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="66890-118">備註</span><span class="sxs-lookup"><span data-stu-id="66890-118">Remarks</span></span>

<span data-ttu-id="66890-119">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="66890-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="66890-120">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="66890-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="66890-121">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="66890-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="66890-122">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="66890-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="66890-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="66890-123">Requirements</span></span>



| <span data-ttu-id="66890-124">需求</span><span class="sxs-lookup"><span data-stu-id="66890-124">Requirement</span></span> | <span data-ttu-id="66890-125">值</span><span class="sxs-lookup"><span data-stu-id="66890-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66890-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66890-126">Minimum supported client</span></span><br/> | <span data-ttu-id="66890-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66890-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="66890-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66890-128">Minimum supported server</span></span><br/> | <span data-ttu-id="66890-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66890-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="66890-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="66890-130">Namespace</span></span><br/>                | <span data-ttu-id="66890-131">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="66890-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="66890-132">MOF</span><span class="sxs-lookup"><span data-stu-id="66890-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66890-133"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="66890-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="66890-134">DLL</span><span class="sxs-lookup"><span data-stu-id="66890-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66890-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66890-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66890-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66890-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66890-137">CIM \_ FileAction</span><span class="sxs-lookup"><span data-stu-id="66890-137">CIM\_FileAction</span></span>](invoke-method-in-class-cim-fileaction.md)
</dt> <dt>

[<span data-ttu-id="66890-138">**CIM \_ FileAction**</span><span class="sxs-lookup"><span data-stu-id="66890-138">**CIM\_FileAction**</span></span>](cim-fileaction.md)
</dt> </dl>

 

