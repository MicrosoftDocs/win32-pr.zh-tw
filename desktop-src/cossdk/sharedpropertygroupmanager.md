---
description: 建立共用屬性群組，並取得現有共用屬性群組的存取權。
ms.assetid: 4ba05806-afda-4926-8ca4-abbf15ed8278
title: 'SharedPropertyGroupManager 類別 (ComSvcs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroupManager
api_type:
- COM
ms.openlocfilehash: 680c5caef996d329e18192193f30841f61f02f27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847220"
---
# <a name="sharedpropertygroupmanager-class"></a><span data-ttu-id="6446a-103">SharedPropertyGroupManager 類別</span><span class="sxs-lookup"><span data-stu-id="6446a-103">SharedPropertyGroupManager class</span></span>

<span data-ttu-id="6446a-104">建立共用屬性群組，並取得現有共用屬性群組的存取權。</span><span class="sxs-lookup"><span data-stu-id="6446a-104">Creates shared property groups and to obtain access to existing shared property groups.</span></span>

<span data-ttu-id="6446a-105">如需有關在 COM + 中使用共用屬性管理員的詳細資訊，請參閱 [Com + 共用屬性管理員](com--shared-property-manager.md)。</span><span class="sxs-lookup"><span data-stu-id="6446a-105">For more information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="6446a-106">執行時機</span><span class="sxs-lookup"><span data-stu-id="6446a-106">When to implement</span></span>

<span data-ttu-id="6446a-107">這個類別是由 COM + 所執行。</span><span class="sxs-lookup"><span data-stu-id="6446a-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="6446a-108">需求</span><span class="sxs-lookup"><span data-stu-id="6446a-108">Requirement</span></span> | <span data-ttu-id="6446a-109">值</span><span class="sxs-lookup"><span data-stu-id="6446a-109">Value</span></span> |
|------------|--------------------------------------------------------------------|
| <span data-ttu-id="6446a-110">CLSID</span><span class="sxs-lookup"><span data-stu-id="6446a-110">CLSID</span></span>      | <span data-ttu-id="6446a-111">CLSID \_ SharedPropertyGroupManager</span><span class="sxs-lookup"><span data-stu-id="6446a-111">CLSID\_SharedPropertyGroupManager</span></span>                                  |
| <span data-ttu-id="6446a-112">ProgID</span><span class="sxs-lookup"><span data-stu-id="6446a-112">ProgID</span></span>     | <span data-ttu-id="6446a-113">L "MTxSpm. SharedPropertyGroupManager"</span><span class="sxs-lookup"><span data-stu-id="6446a-113">L"MTxSpm.SharedPropertyGroupManager"</span></span>                               |
| <span data-ttu-id="6446a-114">介面</span><span class="sxs-lookup"><span data-stu-id="6446a-114">Interfaces</span></span> | [<span data-ttu-id="6446a-115">**ISharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="6446a-115">**ISharedPropertyGroupManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) |



 

## <a name="when-to-use"></a><span data-ttu-id="6446a-116">使用時機</span><span class="sxs-lookup"><span data-stu-id="6446a-116">When to use</span></span>

<span data-ttu-id="6446a-117">您可以使用這個類別來存取 [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)的方法。</span><span class="sxs-lookup"><span data-stu-id="6446a-117">Use this class to access the methods of [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span></span>

## <a name="remarks"></a><span data-ttu-id="6446a-118">備註</span><span class="sxs-lookup"><span data-stu-id="6446a-118">Remarks</span></span>

<span data-ttu-id="6446a-119">若要建立這個物件，請呼叫 [**IObjectCoNtext：： CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance)。</span><span class="sxs-lookup"><span data-stu-id="6446a-119">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="6446a-120">若要從 Microsoft Visual Basic 使用這個類別，請新增 COM + 服務類型程式庫的參考。</span><span class="sxs-lookup"><span data-stu-id="6446a-120">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="6446a-121">您可以使用 "COMSVCSLib. SharedPropertyGroupManager" 將 SharedPropertyGroupManager 物件宣告為類別名稱。</span><span class="sxs-lookup"><span data-stu-id="6446a-121">A SharedPropertyGroupManager object can be declared using "COMSVCSLib.SharedPropertyGroupManager" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="6446a-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="6446a-122">Requirements</span></span>



| <span data-ttu-id="6446a-123">需求</span><span class="sxs-lookup"><span data-stu-id="6446a-123">Requirement</span></span> | <span data-ttu-id="6446a-124">值</span><span class="sxs-lookup"><span data-stu-id="6446a-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6446a-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6446a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6446a-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6446a-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6446a-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6446a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6446a-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6446a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6446a-129">標頭</span><span class="sxs-lookup"><span data-stu-id="6446a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6446a-130"><dt>ComSvcs。h</dt></span><span class="sxs-lookup"><span data-stu-id="6446a-130"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6446a-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6446a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6446a-132">**ISharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="6446a-132">**ISharedPropertyGroupManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)
</dt> <dt>

[<span data-ttu-id="6446a-133">**SharedProperty**</span><span class="sxs-lookup"><span data-stu-id="6446a-133">**SharedProperty**</span></span>](sharedproperty.md)
</dt> <dt>

[<span data-ttu-id="6446a-134">**SharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="6446a-134">**SharedPropertyGroup**</span></span>](sharedpropertygroup.md)
</dt> </dl>

 

 




