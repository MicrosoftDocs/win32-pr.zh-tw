---
description: CIM ExecuteProgram 類別的 Invoke 方法 \_ 會採取特定的動作。 方法執行動作的詳細資料是特定的實作為。 此方法繼承自 CIM \_ 動作。
ms.assetid: 14a12fae-14a6-412a-a778-8dd34a5843d1
ms.tgt_platform: multiple
title: CIM_ExecuteProgram 類別的 Invoke 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ExecuteProgram.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bdf9a4edb78bb47c0354991d161339099e4dc49f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385912"
---
# <a name="invoke-method-of-the-cim_executeprogram-class"></a><span data-ttu-id="f33df-105">CIM ExecuteProgram 類別的 Invoke 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f33df-105">Invoke method of the CIM\_ExecuteProgram class</span></span>

<span data-ttu-id="f33df-106">[**CIM \_ ExecuteProgram**](cim-executeprogram.md)類別的 **Invoke** 方法會採取特定的動作。</span><span class="sxs-lookup"><span data-stu-id="f33df-106">The **Invoke** method of the [**CIM\_ExecuteProgram**](cim-executeprogram.md) class takes a particular action.</span></span> <span data-ttu-id="f33df-107">方法執行動作的詳細資料是特定的實作為。</span><span class="sxs-lookup"><span data-stu-id="f33df-107">The details of how the method performs the action are implementation specific.</span></span> <span data-ttu-id="f33df-108">此方法繼承自 [**CIM \_ 動作**](cim-action.md)。</span><span class="sxs-lookup"><span data-stu-id="f33df-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f33df-109">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="f33df-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f33df-110">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="f33df-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f33df-111">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="f33df-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f33df-112">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="f33df-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f33df-113">語法</span><span class="sxs-lookup"><span data-stu-id="f33df-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="f33df-114">參數</span><span class="sxs-lookup"><span data-stu-id="f33df-114">Parameters</span></span>

<span data-ttu-id="f33df-115">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f33df-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f33df-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="f33df-116">Return value</span></span>

<span data-ttu-id="f33df-117">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="f33df-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f33df-118">備註</span><span class="sxs-lookup"><span data-stu-id="f33df-118">Remarks</span></span>

<span data-ttu-id="f33df-119">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="f33df-119">WMI does not implement this class.</span></span>

<span data-ttu-id="f33df-120">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="f33df-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f33df-121">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f33df-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f33df-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="f33df-122">Requirements</span></span>



| <span data-ttu-id="f33df-123">需求</span><span class="sxs-lookup"><span data-stu-id="f33df-123">Requirement</span></span> | <span data-ttu-id="f33df-124">值</span><span class="sxs-lookup"><span data-stu-id="f33df-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f33df-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f33df-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f33df-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f33df-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f33df-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f33df-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f33df-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f33df-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f33df-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="f33df-129">Namespace</span></span><br/>                | <span data-ttu-id="f33df-130">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f33df-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f33df-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f33df-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f33df-132"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f33df-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f33df-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f33df-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f33df-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f33df-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f33df-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f33df-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f33df-136">CIM \_ ExecuteProgram</span><span class="sxs-lookup"><span data-stu-id="f33df-136">CIM\_ExecuteProgram</span></span>](invoke-method-in-class-cim-executeprogram.md)
</dt> <dt>

[<span data-ttu-id="f33df-137">**CIM \_ ExecuteProgram**</span><span class="sxs-lookup"><span data-stu-id="f33df-137">**CIM\_ExecuteProgram**</span></span>](cim-executeprogram.md)
</dt> </dl>

 

