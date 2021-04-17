---
description: 存取儲存在 COM + 目錄中的資料。
ms.assetid: d77123f6-9821-4c80-860c-5f1feaca7987
title: 'COMAdminCatalog 類別 (ComAdmin) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalog
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: fa6e71d13f5a3d157bd3ce1035d0616dc1e5a519
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468393"
---
# <a name="comadmincatalog-class"></a><span data-ttu-id="09d49-103">COMAdminCatalog 類別</span><span class="sxs-lookup"><span data-stu-id="09d49-103">COMAdminCatalog class</span></span>

<span data-ttu-id="09d49-104">存取儲存在 COM + 目錄中的資料。</span><span class="sxs-lookup"><span data-stu-id="09d49-104">Accesses the data that is stored in the COM+ catalog.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="09d49-105">執行時機</span><span class="sxs-lookup"><span data-stu-id="09d49-105">When to implement</span></span>

<span data-ttu-id="09d49-106">這個類別是由 COM + 所執行。</span><span class="sxs-lookup"><span data-stu-id="09d49-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="09d49-107">需求</span><span class="sxs-lookup"><span data-stu-id="09d49-107">Requirement</span></span> | <span data-ttu-id="09d49-108">值</span><span class="sxs-lookup"><span data-stu-id="09d49-108">Value</span></span> |
|------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09d49-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="09d49-109">CLSID</span></span>      | <span data-ttu-id="09d49-110">CLSID \_ COMAdminCatalog</span><span class="sxs-lookup"><span data-stu-id="09d49-110">CLSID\_COMAdminCatalog</span></span>                                                                                            |
| <span data-ttu-id="09d49-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="09d49-111">ProgID</span></span>     | <span data-ttu-id="09d49-112">L "COMAdmin. COMAdminCatalog"</span><span class="sxs-lookup"><span data-stu-id="09d49-112">L"COMAdmin.COMAdminCatalog"</span></span>                                                                                       |
| <span data-ttu-id="09d49-113">介面</span><span class="sxs-lookup"><span data-stu-id="09d49-113">Interfaces</span></span> | [<span data-ttu-id="09d49-114">**ICOMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="09d49-114">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)<br/> [<span data-ttu-id="09d49-115">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="09d49-115">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)<br/> |



 

## <a name="when-to-use"></a><span data-ttu-id="09d49-116">使用時機</span><span class="sxs-lookup"><span data-stu-id="09d49-116">When to use</span></span>

<span data-ttu-id="09d49-117">您可以使用從 **COMAdminCatalog** 類別建立的物件，開始以程式設計方式存取儲存在 com + 目錄中的 com + 設定資料。</span><span class="sxs-lookup"><span data-stu-id="09d49-117">You use objects created from the **COMAdminCatalog** class to begin programmatic access to COM+ configuration data stored in the COM+ catalog.</span></span> <span data-ttu-id="09d49-118">這項資訊的基礎是元件服務管理工具的主控台樹中的資料夾和專案。</span><span class="sxs-lookup"><span data-stu-id="09d49-118">This information underlies the folders and items in the console tree of the Component Services administration tool.</span></span> <span data-ttu-id="09d49-119">**COMAdminCatalog** 類別可讓您存取目錄中的集合、安裝 com + 應用程式和元件、啟動和停止服務，以及連接至遠端伺服器並加以管理。</span><span class="sxs-lookup"><span data-stu-id="09d49-119">The **COMAdminCatalog** class enables you to access collections in the catalog, install COM+ applications and components, start and stop services, and connect to and administer remote servers.</span></span>

<span data-ttu-id="09d49-120">元件服務管理工具中的資料夾對應至目錄中的集合，您可以使用從 [**COMAdminCatalogCollection**](comadmincatalogcollection.md) 類別建立的物件來表示。</span><span class="sxs-lookup"><span data-stu-id="09d49-120">Folders in the Component Services administration tool correspond to collections in the catalog, which you can represent by using objects created from the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class.</span></span> <span data-ttu-id="09d49-121">資料夾中的專案會對應至集合中的專案，您可以使用從 [**COMAdminCatalogObject**](comadmincatalogobject.md) 類別建立的物件來表示。</span><span class="sxs-lookup"><span data-stu-id="09d49-121">Items in the folders correspond to items in the collections, which you can represent by using objects created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="09d49-122">並非所有透過 [**COMAdminCatalogCollection**](comadmincatalogcollection.md) 和 [**COMAdminCatalogObject**](comadmincatalogobject.md) 公開的集合和專案都可在「元件服務」系統管理工具中使用。</span><span class="sxs-lookup"><span data-stu-id="09d49-122">Not all of the collections and items exposed through [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and [**COMAdminCatalogObject**](comadmincatalogobject.md) are available in the Component Services administration tool.</span></span>

<span data-ttu-id="09d49-123">如需特定集合及其屬性的相關資訊，請參閱 [Com + 系統管理集合](com--administration-collections.md)。</span><span class="sxs-lookup"><span data-stu-id="09d49-123">For information regarding specific collections and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="09d49-124">如需以程式設計方式管理 COM + 的簡介，請參閱 [自動化 COM + 管理](automating-com--administration.md)。</span><span class="sxs-lookup"><span data-stu-id="09d49-124">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="09d49-125">備註</span><span class="sxs-lookup"><span data-stu-id="09d49-125">Remarks</span></span>

<span data-ttu-id="09d49-126">若要建立這個物件，請呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)。</span><span class="sxs-lookup"><span data-stu-id="09d49-126">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="09d49-127">若要從 Microsoft Visual Basic 使用這個類別，請將參考新增至 COM + 系統管理員類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="09d49-127">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="09d49-128">您可以使用 "COMAdmin. COMAdminCatalog" 將 COMAdminCatalog 物件宣告為類別名稱。</span><span class="sxs-lookup"><span data-stu-id="09d49-128">A COMAdminCatalog object can be declared using "COMAdmin.COMAdminCatalog" as the class name.</span></span>

<span data-ttu-id="09d49-129">在以 Windows XP 發行的 COM + 1.5 中， **COMAdminCatalog** 類別會執行 [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) 介面。</span><span class="sxs-lookup"><span data-stu-id="09d49-129">In COM+ 1.5, released with Windows XP, the **COMAdminCatalog** class implements the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface.</span></span> <span data-ttu-id="09d49-130">不過，在以 Windows 2000 發行的 COM + 1.0 中， **COMAdminCatalog** 類別只會執行 [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) 介面。</span><span class="sxs-lookup"><span data-stu-id="09d49-130">However, in COM+ 1.0, released with Windows 2000, the **COMAdminCatalog** class implements only the [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="09d49-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="09d49-131">Requirements</span></span>



| <span data-ttu-id="09d49-132">需求</span><span class="sxs-lookup"><span data-stu-id="09d49-132">Requirement</span></span> | <span data-ttu-id="09d49-133">值</span><span class="sxs-lookup"><span data-stu-id="09d49-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09d49-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09d49-134">Minimum supported client</span></span><br/> | <span data-ttu-id="09d49-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09d49-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="09d49-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09d49-136">Minimum supported server</span></span><br/> | <span data-ttu-id="09d49-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09d49-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="09d49-138">標頭</span><span class="sxs-lookup"><span data-stu-id="09d49-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="09d49-139"><dt>ComAdmin。h</dt></span><span class="sxs-lookup"><span data-stu-id="09d49-139"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="09d49-140">Idl</span><span class="sxs-lookup"><span data-stu-id="09d49-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="09d49-141"><dt>ComAdmin .Idl</dt></span><span class="sxs-lookup"><span data-stu-id="09d49-141"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09d49-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09d49-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09d49-143">**COMAdminCatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="09d49-143">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
</dt> <dt>

[<span data-ttu-id="09d49-144">**COMAdminCatalogObject**</span><span class="sxs-lookup"><span data-stu-id="09d49-144">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
</dt> <dt>

[<span data-ttu-id="09d49-145">**ICOMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="09d49-145">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
</dt> <dt>

[<span data-ttu-id="09d49-146">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="09d49-146">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
</dt> </dl>

 

