---
description: CIM DirectorySpecification 類別的 Invoke 方法會 \_ 評估特定檢查。
ms.assetid: 63289f94-f134-4159-898c-404cdd8f2a5c
ms.tgt_platform: multiple
title: CIM_DirectorySpecification 類別的 Invoke 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecification.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 48e5cb315f7dba6be187280ee6a16d7c4711752f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970317"
---
# <a name="invoke-method-of-the-cim_directoryspecification-class"></a><span data-ttu-id="250f8-103">CIM DirectorySpecification 類別的 Invoke 方法 \_</span><span class="sxs-lookup"><span data-stu-id="250f8-103">Invoke method of the CIM\_DirectorySpecification class</span></span>

<span data-ttu-id="250f8-104">[**CIM \_ DirectorySpecification**](cim-directoryspecification.md)類別的 **Invoke** 方法會評估特定檢查。</span><span class="sxs-lookup"><span data-stu-id="250f8-104">The **Invoke** method of the [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class evaluates a particular check.</span></span> <span data-ttu-id="250f8-105">有關方法如何評估 CIM 內容中特定檢查的詳細資料，請參閱非抽象 [**cim \_ 檢查**](cim-check.md) 子類別。</span><span class="sxs-lookup"><span data-stu-id="250f8-105">Details about how the method evaluates a particular check in a CIM context are described by the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span> <span data-ttu-id="250f8-106">此方法繼承自 **CIM \_ 檢查**。</span><span class="sxs-lookup"><span data-stu-id="250f8-106">This method is inherited from **CIM\_Check**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="250f8-107">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="250f8-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="250f8-108">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="250f8-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="250f8-109">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="250f8-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="250f8-110">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="250f8-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="250f8-111">語法</span><span class="sxs-lookup"><span data-stu-id="250f8-111">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="250f8-112">參數</span><span class="sxs-lookup"><span data-stu-id="250f8-112">Parameters</span></span>

<span data-ttu-id="250f8-113">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="250f8-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="250f8-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="250f8-114">Return value</span></span>

<span data-ttu-id="250f8-115">如果成功，則傳回0，如果不支援方法，則傳回1，而任何其他值則表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="250f8-115">Returns a 0 if successful, a 1 if the method is not supported, and any other value indicates an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="250f8-116">備註</span><span class="sxs-lookup"><span data-stu-id="250f8-116">Remarks</span></span>

<span data-ttu-id="250f8-117">這個方法目前不是由 WMI 所執行。</span><span class="sxs-lookup"><span data-stu-id="250f8-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="250f8-118">若要使用這個方法，您必須在自己的提供者中加以執行。</span><span class="sxs-lookup"><span data-stu-id="250f8-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="250f8-119">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="250f8-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="250f8-120">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="250f8-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="250f8-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="250f8-121">Requirements</span></span>



| <span data-ttu-id="250f8-122">需求</span><span class="sxs-lookup"><span data-stu-id="250f8-122">Requirement</span></span> | <span data-ttu-id="250f8-123">值</span><span class="sxs-lookup"><span data-stu-id="250f8-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="250f8-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="250f8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="250f8-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="250f8-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="250f8-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="250f8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="250f8-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="250f8-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="250f8-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="250f8-128">Namespace</span></span><br/>                | <span data-ttu-id="250f8-129">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="250f8-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="250f8-130">MOF</span><span class="sxs-lookup"><span data-stu-id="250f8-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="250f8-131"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="250f8-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="250f8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="250f8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="250f8-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="250f8-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="250f8-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="250f8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="250f8-135">CIM \_ DirectorySpecification</span><span class="sxs-lookup"><span data-stu-id="250f8-135">CIM\_DirectorySpecification</span></span>](invoke-method-in-class-cim-directoryspecification.md)
</dt> <dt>

[<span data-ttu-id="250f8-136">**CIM \_ DirectorySpecification**</span><span class="sxs-lookup"><span data-stu-id="250f8-136">**CIM\_DirectorySpecification**</span></span>](cim-directoryspecification.md)
</dt> </dl>

 

