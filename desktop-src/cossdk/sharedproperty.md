---
description: 設定或抓取共用屬性的值。
ms.assetid: 19ed8d50-3ac1-408e-9f25-09f284d025f1
title: 'SharedProperty 類別 (ComSvcs) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SharedProperty
api_type:
- COM
ms.openlocfilehash: a7a7857ad280ad722601bdced6c25d04b03dc0b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110553"
---
# <a name="sharedproperty-class"></a><span data-ttu-id="3a2d1-103">SharedProperty 類別</span><span class="sxs-lookup"><span data-stu-id="3a2d1-103">SharedProperty class</span></span>

<span data-ttu-id="3a2d1-104">設定或抓取共用屬性的值。</span><span class="sxs-lookup"><span data-stu-id="3a2d1-104">Sets or retrieves the value of a shared property.</span></span>

<span data-ttu-id="3a2d1-105">如需有關在 COM + 中使用共用屬性管理員的一般資訊，請參閱 [Com + 共用屬性管理員](com--shared-property-manager.md)。</span><span class="sxs-lookup"><span data-stu-id="3a2d1-105">For general information about using the Shared Property Manager in COM+, see [COM+ Shared Property Manager](com--shared-property-manager.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="3a2d1-106">執行時機</span><span class="sxs-lookup"><span data-stu-id="3a2d1-106">When to implement</span></span>

<span data-ttu-id="3a2d1-107">這個類別是由 COM + 所執行。</span><span class="sxs-lookup"><span data-stu-id="3a2d1-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="3a2d1-108">需求</span><span class="sxs-lookup"><span data-stu-id="3a2d1-108">Requirement</span></span> | <span data-ttu-id="3a2d1-109">值</span><span class="sxs-lookup"><span data-stu-id="3a2d1-109">Value</span></span> |
|------------|--------------------------------------------|
| <span data-ttu-id="3a2d1-110">介面</span><span class="sxs-lookup"><span data-stu-id="3a2d1-110">Interfaces</span></span> | [<span data-ttu-id="3a2d1-111">**ISharedProperty**</span><span class="sxs-lookup"><span data-stu-id="3a2d1-111">**ISharedProperty**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) |



 

## <a name="when-to-use"></a><span data-ttu-id="3a2d1-112">使用時機</span><span class="sxs-lookup"><span data-stu-id="3a2d1-112">When to use</span></span>

<span data-ttu-id="3a2d1-113">您可以使用這個類別來存取 [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty)的方法。</span><span class="sxs-lookup"><span data-stu-id="3a2d1-113">Use this class to access the methods of [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty).</span></span>

## <a name="remarks"></a><span data-ttu-id="3a2d1-114">備註</span><span class="sxs-lookup"><span data-stu-id="3a2d1-114">Remarks</span></span>

<span data-ttu-id="3a2d1-115">您可以使用 [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup)的 [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty)或 [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition)方法來建立 **SharedProperty** 物件。</span><span class="sxs-lookup"><span data-stu-id="3a2d1-115">You can create a **SharedProperty** object by using the [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) or [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) methods of [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup).</span></span>

<span data-ttu-id="3a2d1-116">若要從 Microsoft Visual Basic 使用這個類別，請新增 COM + 服務類型程式庫的參考。</span><span class="sxs-lookup"><span data-stu-id="3a2d1-116">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="3a2d1-117">SharedProperty 物件是藉由呼叫 [**SharedPropertyGroup**](sharedpropertygroup.md)物件的 [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty)或 [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition)方法來建立。</span><span class="sxs-lookup"><span data-stu-id="3a2d1-117">A SharedProperty object is created by calling the [**CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) or [**CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) methods of the [**SharedPropertyGroup**](sharedpropertygroup.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a2d1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a2d1-118">Requirements</span></span>



| <span data-ttu-id="3a2d1-119">需求</span><span class="sxs-lookup"><span data-stu-id="3a2d1-119">Requirement</span></span> | <span data-ttu-id="3a2d1-120">值</span><span class="sxs-lookup"><span data-stu-id="3a2d1-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3a2d1-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a2d1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3a2d1-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a2d1-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3a2d1-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a2d1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3a2d1-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a2d1-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3a2d1-125">標頭</span><span class="sxs-lookup"><span data-stu-id="3a2d1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a2d1-126"><dt>ComSvcs。h</dt></span><span class="sxs-lookup"><span data-stu-id="3a2d1-126"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a2d1-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a2d1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a2d1-128">**ISharedProperty**</span><span class="sxs-lookup"><span data-stu-id="3a2d1-128">**ISharedProperty**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty)
</dt> <dt>

[<span data-ttu-id="3a2d1-129">**SharedPropertyGroup**</span><span class="sxs-lookup"><span data-stu-id="3a2d1-129">**SharedPropertyGroup**</span></span>](sharedpropertygroup.md)
</dt> <dt>

[<span data-ttu-id="3a2d1-130">**SharedPropertyGroupManager**</span><span class="sxs-lookup"><span data-stu-id="3a2d1-130">**SharedPropertyGroupManager**</span></span>](sharedpropertygroupmanager.md)
</dt> </dl>

 

 




