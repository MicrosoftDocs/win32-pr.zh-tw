---
description: StartService 方法會將服務置於啟動狀態。
ms.assetid: 0f2880ed-1643-4211-8684-12493711b1f8
ms.tgt_platform: multiple
title: " (CIMWin32 WMI 提供者的 CIM_Service 類別的 StartService 方法) "
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1592552595c06ec7111041cbb1c1b1d2628f8b6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688887"
---
# <a name="startservice-method-of-the-cim_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="c9bc6-103"> (CIMWin32 WMI 提供者的 CIM_Service 類別的 StartService 方法) </span><span class="sxs-lookup"><span data-stu-id="c9bc6-103">StartService method of the CIM_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="c9bc6-104">**StartService** 方法會將服務置於啟動狀態。</span><span class="sxs-lookup"><span data-stu-id="c9bc6-104">The **StartService** method puts the service in a started state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c9bc6-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="c9bc6-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c9bc6-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="c9bc6-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c9bc6-107">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="c9bc6-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c9bc6-108">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="c9bc6-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c9bc6-109">語法</span><span class="sxs-lookup"><span data-stu-id="c9bc6-109">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="c9bc6-110">參數</span><span class="sxs-lookup"><span data-stu-id="c9bc6-110">Parameters</span></span>

<span data-ttu-id="c9bc6-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c9bc6-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9bc6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9bc6-112">Return value</span></span>

<span data-ttu-id="c9bc6-113">在成功時傳回 0 (零) 的值，並傳回任何其他數位以表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="c9bc6-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="c9bc6-114">在子類別中，可以使用方法上的 **ValueMap** 辨識符號來指定可能的傳回碼集。</span><span class="sxs-lookup"><span data-stu-id="c9bc6-114">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="c9bc6-115">您也可以在子類別中，以 **值** 陣列限定詞的形式指定要轉譯之 **ValueMap** 內容的字串。</span><span class="sxs-lookup"><span data-stu-id="c9bc6-115">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9bc6-116">備註</span><span class="sxs-lookup"><span data-stu-id="c9bc6-116">Remarks</span></span>

<span data-ttu-id="c9bc6-117">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="c9bc6-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c9bc6-118">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="c9bc6-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c9bc6-119">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="c9bc6-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c9bc6-120">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="c9bc6-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9bc6-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9bc6-121">Requirements</span></span>



| <span data-ttu-id="c9bc6-122">需求</span><span class="sxs-lookup"><span data-stu-id="c9bc6-122">Requirement</span></span> | <span data-ttu-id="c9bc6-123">值</span><span class="sxs-lookup"><span data-stu-id="c9bc6-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9bc6-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9bc6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c9bc6-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9bc6-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c9bc6-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9bc6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c9bc6-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9bc6-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c9bc6-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="c9bc6-128">Namespace</span></span><br/>                | <span data-ttu-id="c9bc6-129">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c9bc6-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c9bc6-130">MOF</span><span class="sxs-lookup"><span data-stu-id="c9bc6-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9bc6-131"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9bc6-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9bc6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c9bc6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9bc6-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9bc6-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9bc6-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9bc6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9bc6-135">CIM \_ 服務</span><span class="sxs-lookup"><span data-stu-id="c9bc6-135">CIM\_Service</span></span>](startservice-method-in-class-cim-service.md)
</dt> <dt>

[<span data-ttu-id="c9bc6-136">**CIM \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="c9bc6-136">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

