---
description: 使用 .NET Framework common language runtime 中的 managed 程式碼時，捕獲元件的相關資訊。
ms.assetid: 45dcdc6a-74df-4763-ba8b-82f604db78d4
title: 'ClrAssemblyLocator 類別 (ComSvcs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ClrAssemblyLocator
api_type:
- COM
ms.openlocfilehash: ff5c1d21525a950208c1b919d4dee0e2122d2e50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847171"
---
# <a name="clrassemblylocator-class"></a><span data-ttu-id="68ee9-103">ClrAssemblyLocator 類別</span><span class="sxs-lookup"><span data-stu-id="68ee9-103">ClrAssemblyLocator class</span></span>

<span data-ttu-id="68ee9-104">使用 .NET Framework common language runtime 中的 managed 程式碼時，捕獲元件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="68ee9-104">Retrieves information about an assembly when using managed code in the .NET Framework common language runtime.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="68ee9-105">執行時機</span><span class="sxs-lookup"><span data-stu-id="68ee9-105">When to implement</span></span>

<span data-ttu-id="68ee9-106">這個類別是由 COM + 所執行。</span><span class="sxs-lookup"><span data-stu-id="68ee9-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="68ee9-107">需求</span><span class="sxs-lookup"><span data-stu-id="68ee9-107">Requirement</span></span> | <span data-ttu-id="68ee9-108">值</span><span class="sxs-lookup"><span data-stu-id="68ee9-108">Value</span></span> |
|------------|-------------------------------------------------------|
| <span data-ttu-id="68ee9-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="68ee9-109">CLSID</span></span>      | <span data-ttu-id="68ee9-110">GUID \_ AssemblyLocator</span><span class="sxs-lookup"><span data-stu-id="68ee9-110">GUID\_AssemblyLocator</span></span>                                 |
| <span data-ttu-id="68ee9-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="68ee9-111">ProgID</span></span>     | <span data-ttu-id="68ee9-112">L "System.enterpriseservices. AssemblyLocator"</span><span class="sxs-lookup"><span data-stu-id="68ee9-112">L"System.EnterpriseServices.Internal.AssemblyLocator"</span></span> |
| <span data-ttu-id="68ee9-113">介面</span><span class="sxs-lookup"><span data-stu-id="68ee9-113">Interfaces</span></span> | [<span data-ttu-id="68ee9-114">**IAssemblyLocator**</span><span class="sxs-lookup"><span data-stu-id="68ee9-114">**IAssemblyLocator**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator)          |



 

## <a name="when-to-use"></a><span data-ttu-id="68ee9-115">使用時機</span><span class="sxs-lookup"><span data-stu-id="68ee9-115">When to use</span></span>

<span data-ttu-id="68ee9-116">您可以使用這個類別來存取 [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator)的方法。</span><span class="sxs-lookup"><span data-stu-id="68ee9-116">Use this class to access the methods of [**IAssemblyLocator**](/windows/desktop/api/ComSvcs/nn-comsvcs-iassemblylocator).</span></span>

## <a name="remarks"></a><span data-ttu-id="68ee9-117">備註</span><span class="sxs-lookup"><span data-stu-id="68ee9-117">Remarks</span></span>

<span data-ttu-id="68ee9-118">若要建立這個物件，請呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)。</span><span class="sxs-lookup"><span data-stu-id="68ee9-118">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="68ee9-119">若要從 Microsoft Visual Basic 使用這個類別，請新增 COM + 服務類型程式庫的參考。</span><span class="sxs-lookup"><span data-stu-id="68ee9-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="68ee9-120">您可以使用 "COMSVCSLib. ClrAssemblyLocator" 將 ClrAssemblyLocator 物件宣告為類別名稱。</span><span class="sxs-lookup"><span data-stu-id="68ee9-120">A ClrAssemblyLocator object can be declared using "COMSVCSLib.ClrAssemblyLocator" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="68ee9-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="68ee9-121">Requirements</span></span>



| <span data-ttu-id="68ee9-122">需求</span><span class="sxs-lookup"><span data-stu-id="68ee9-122">Requirement</span></span> | <span data-ttu-id="68ee9-123">值</span><span class="sxs-lookup"><span data-stu-id="68ee9-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="68ee9-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68ee9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="68ee9-125">僅限 Windows XP （含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68ee9-125">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="68ee9-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68ee9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="68ee9-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68ee9-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="68ee9-128">標頭</span><span class="sxs-lookup"><span data-stu-id="68ee9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="68ee9-129"><dt>ComSvcs。h</dt></span><span class="sxs-lookup"><span data-stu-id="68ee9-129"><dt>ComSvcs.h</dt></span></span> </dl> |



 

