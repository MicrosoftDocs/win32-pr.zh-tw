---
description: 建立並存取共用屬性群組中的共用屬性。
ms.assetid: 20fd32f0-b2b2-4bed-8c59-1d1fdc8a399e
title: 'SharedPropertyGroup 類別 (ComSvcs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedPropertyGroup
api_type:
- COM
ms.openlocfilehash: a3fff14043d67b96db99334c7bec1afee2577f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688763"
---
# <a name="sharedpropertygroup-class"></a><span data-ttu-id="921da-103">SharedPropertyGroup 類別</span><span class="sxs-lookup"><span data-stu-id="921da-103">SharedPropertyGroup class</span></span>

<span data-ttu-id="921da-104">建立並存取共用屬性群組中的共用屬性。</span><span class="sxs-lookup"><span data-stu-id="921da-104">Creates and accesses the shared properties in a shared property group.</span></span>

<span data-ttu-id="921da-105">如需有關在 COM + 中使用共用屬性管理員的詳細資訊，請參閱 [Com + 共用屬性管理員](com--shared-property-manager.md)。</span><span class="sxs-lookup"><span data-stu-id="921da-105">For more information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="921da-106">執行時機</span><span class="sxs-lookup"><span data-stu-id="921da-106">When to implement</span></span>

<span data-ttu-id="921da-107">這個類別是由 COM + 所執行。</span><span class="sxs-lookup"><span data-stu-id="921da-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="921da-108">需求</span><span class="sxs-lookup"><span data-stu-id="921da-108">Requirement</span></span> | <span data-ttu-id="921da-109">值</span><span class="sxs-lookup"><span data-stu-id="921da-109">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="921da-110">介面</span><span class="sxs-lookup"><span data-stu-id="921da-110">Interfaces</span></span> | [<span data-ttu-id="921da-111">**ISharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="921da-111">**ISharedPropertyGroup**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) |



 

## <a name="when-to-use"></a><span data-ttu-id="921da-112">使用時機</span><span class="sxs-lookup"><span data-stu-id="921da-112">When to use</span></span>

<span data-ttu-id="921da-113">您可以使用這個類別來存取 [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)的方法。</span><span class="sxs-lookup"><span data-stu-id="921da-113">Use this class to access the methods of [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span></span>

## <a name="remarks"></a><span data-ttu-id="921da-114">備註</span><span class="sxs-lookup"><span data-stu-id="921da-114">Remarks</span></span>

<span data-ttu-id="921da-115">您可以使用 [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager)的 [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup)方法來建立 **SharedPropertyGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="921da-115">You can create a **SharedPropertyGroup** object using the [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) method of [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager).</span></span>

<span data-ttu-id="921da-116">若要從 Microsoft Visual Basic 使用這個類別，請新增 COM + 服務類型程式庫的參考。</span><span class="sxs-lookup"><span data-stu-id="921da-116">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="921da-117">SharedPropertyGroup 物件是藉由呼叫 [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md)物件的 [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup)方法來建立。</span><span class="sxs-lookup"><span data-stu-id="921da-117">A SharedPropertyGroup object is created by calling the [**CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) method of the [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="921da-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="921da-118">Requirements</span></span>



| <span data-ttu-id="921da-119">需求</span><span class="sxs-lookup"><span data-stu-id="921da-119">Requirement</span></span> | <span data-ttu-id="921da-120">值</span><span class="sxs-lookup"><span data-stu-id="921da-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="921da-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="921da-121">Minimum supported client</span></span><br/> | <span data-ttu-id="921da-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="921da-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="921da-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="921da-123">Minimum supported server</span></span><br/> | <span data-ttu-id="921da-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="921da-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="921da-125">標頭</span><span class="sxs-lookup"><span data-stu-id="921da-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="921da-126"><dt>ComSvcs。h</dt></span><span class="sxs-lookup"><span data-stu-id="921da-126"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="921da-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="921da-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="921da-128">**ISharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="921da-128">**ISharedPropertyGroup**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)
</dt> <dt>

[<span data-ttu-id="921da-129">**SharedProperty**</span><span class="sxs-lookup"><span data-stu-id="921da-129">**SharedProperty**</span></span>](sharedproperty.md)
</dt> <dt>

[<span data-ttu-id="921da-130">**SharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="921da-130">**SharedPropertyGroupManager**</span></span>](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




