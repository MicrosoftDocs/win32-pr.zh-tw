---
description: 將 managed 物件系結至應用程式域，也就是應用程式執行所在的隔離環境。
ms.assetid: 9357ea5d-6f86-4747-a923-16575ff13122
title: 'AppDomainHelper 類別 (ComSvcs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AppDomainHelper
api_type:
- COM
ms.openlocfilehash: 6b4fbedbca631ec49dc2e416d939abdeb239e5b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510522"
---
# <a name="appdomainhelper-class"></a><span data-ttu-id="2a15e-103">AppDomainHelper 類別</span><span class="sxs-lookup"><span data-stu-id="2a15e-103">AppDomainHelper class</span></span>

<span data-ttu-id="2a15e-104">將 managed 物件系結至應用程式域，也就是應用程式執行所在的隔離環境。</span><span class="sxs-lookup"><span data-stu-id="2a15e-104">Binds a managed object to an application domain, which is an isolated environment where applications execute.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="2a15e-105">執行時機</span><span class="sxs-lookup"><span data-stu-id="2a15e-105">When to implement</span></span>

<span data-ttu-id="2a15e-106">這個類別是由 COM + 所執行。</span><span class="sxs-lookup"><span data-stu-id="2a15e-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="2a15e-107">需求</span><span class="sxs-lookup"><span data-stu-id="2a15e-107">Requirement</span></span> | <span data-ttu-id="2a15e-108">值</span><span class="sxs-lookup"><span data-stu-id="2a15e-108">Value</span></span> |
|------------|-------------------------------------------------------|
| <span data-ttu-id="2a15e-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="2a15e-109">CLSID</span></span>      | <span data-ttu-id="2a15e-110">GUID \_ AppDomainHelper</span><span class="sxs-lookup"><span data-stu-id="2a15e-110">GUID\_AppDomainHelper</span></span>                                 |
| <span data-ttu-id="2a15e-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="2a15e-111">ProgID</span></span>     | <span data-ttu-id="2a15e-112">L "System.enterpriseservices. AppDomainHelper"</span><span class="sxs-lookup"><span data-stu-id="2a15e-112">L"System.EnterpriseServices.Internal.AppDomainHelper"</span></span> |
| <span data-ttu-id="2a15e-113">介面</span><span class="sxs-lookup"><span data-stu-id="2a15e-113">Interfaces</span></span> | [<span data-ttu-id="2a15e-114">**IAppDomainHelper**</span><span class="sxs-lookup"><span data-stu-id="2a15e-114">**IAppDomainHelper**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)          |



 

## <a name="when-to-use"></a><span data-ttu-id="2a15e-115">使用時機</span><span class="sxs-lookup"><span data-stu-id="2a15e-115">When to use</span></span>

<span data-ttu-id="2a15e-116">您可以使用這個類別來存取 [**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)的方法。</span><span class="sxs-lookup"><span data-stu-id="2a15e-116">Use this class to access the methods of [**IAppDomainHelper**](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper).</span></span>

## <a name="remarks"></a><span data-ttu-id="2a15e-117">備註</span><span class="sxs-lookup"><span data-stu-id="2a15e-117">Remarks</span></span>

<span data-ttu-id="2a15e-118">若要建立這個物件，請呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)。</span><span class="sxs-lookup"><span data-stu-id="2a15e-118">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="2a15e-119">若要從 Microsoft Visual Basic 使用這個類別，請新增 COM + 服務類型程式庫的參考。</span><span class="sxs-lookup"><span data-stu-id="2a15e-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="2a15e-120">您可以使用 "COMSVCSLib. AppDomainHelper" 將 AppDomainHelper 物件宣告為類別名稱。</span><span class="sxs-lookup"><span data-stu-id="2a15e-120">An AppDomainHelper object can be declared using "COMSVCSLib.AppDomainHelper" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a15e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a15e-121">Requirements</span></span>



| <span data-ttu-id="2a15e-122">需求</span><span class="sxs-lookup"><span data-stu-id="2a15e-122">Requirement</span></span> | <span data-ttu-id="2a15e-123">值</span><span class="sxs-lookup"><span data-stu-id="2a15e-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2a15e-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2a15e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2a15e-125">僅限 Windows XP （含 SP1） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a15e-125">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2a15e-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2a15e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2a15e-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a15e-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2a15e-128">標頭</span><span class="sxs-lookup"><span data-stu-id="2a15e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a15e-129"><dt>ComSvcs。h</dt></span><span class="sxs-lookup"><span data-stu-id="2a15e-129"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a15e-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a15e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a15e-131">**IAppDomainHelper**</span><span class="sxs-lookup"><span data-stu-id="2a15e-131">**IAppDomainHelper**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iappdomainhelper)
</dt> </dl>

 

