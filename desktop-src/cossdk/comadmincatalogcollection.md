---
description: 代表 COM + 目錄中的任何集合。 您可以使用它來列舉、新增、移除和取出集合中的專案，以及存取相關集合。
ms.assetid: 2530e44f-c428-4baa-88e1-8d01eaf234cc
title: 'COMAdminCatalogCollection 類別 (ComAdmin) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogCollection
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 985a6b947708542ec3ce1dc6ecc835c94259b315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689008"
---
# <a name="comadmincatalogcollection-class"></a><span data-ttu-id="174fe-104">COMAdminCatalogCollection 類別</span><span class="sxs-lookup"><span data-stu-id="174fe-104">COMAdminCatalogCollection class</span></span>

<span data-ttu-id="174fe-105">代表 COM + 目錄中的任何集合。</span><span class="sxs-lookup"><span data-stu-id="174fe-105">Represents any collection in the COM+ catalog.</span></span> <span data-ttu-id="174fe-106">您可以使用它來列舉、新增、移除和取出集合中的專案，以及存取相關集合。</span><span class="sxs-lookup"><span data-stu-id="174fe-106">Use it to enumerate, add, remove, and retrieve items in a collection and to access related collections.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="174fe-107">執行時機</span><span class="sxs-lookup"><span data-stu-id="174fe-107">When to implement</span></span>

<span data-ttu-id="174fe-108">這個類別是由 COM + 所執行。</span><span class="sxs-lookup"><span data-stu-id="174fe-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="174fe-109">需求</span><span class="sxs-lookup"><span data-stu-id="174fe-109">Requirement</span></span> | <span data-ttu-id="174fe-110">值</span><span class="sxs-lookup"><span data-stu-id="174fe-110">Value</span></span> |
|------------|--------------------------------------------------|
| <span data-ttu-id="174fe-111">介面</span><span class="sxs-lookup"><span data-stu-id="174fe-111">Interfaces</span></span> | [<span data-ttu-id="174fe-112">**ICatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="174fe-112">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) |



 

## <a name="when-to-use"></a><span data-ttu-id="174fe-113">使用時機</span><span class="sxs-lookup"><span data-stu-id="174fe-113">When to use</span></span>

<span data-ttu-id="174fe-114">當您想要以程式設計方式操作 COM + 目錄中的集合時，請使用從 **COMAdminCatalogCollection** 類別建立的物件。</span><span class="sxs-lookup"><span data-stu-id="174fe-114">Use objects created from the **COMAdminCatalogCollection** class when you want to programmatically manipulate a collection in the COM+ catalog.</span></span> <span data-ttu-id="174fe-115">這些集合會對應到 [元件服務] 系統管理工具中的資料夾。</span><span class="sxs-lookup"><span data-stu-id="174fe-115">These collections correspond to folders in the Component Services administration tool.</span></span> <span data-ttu-id="174fe-116">資料夾內的專案會對應至集合中的專案，您可以使用從 [**COMAdminCatalogObject**](comadmincatalogobject.md) 類別建立的物件來表示。</span><span class="sxs-lookup"><span data-stu-id="174fe-116">Items inside the folders correspond to items in collections, which you can represent by using objects created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="174fe-117">如需有關目錄及其屬性之集合的詳細資訊，請參閱 [Com + 系統管理集合](com--administration-collections.md)。</span><span class="sxs-lookup"><span data-stu-id="174fe-117">For information regarding the collections on the catalog and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="174fe-118">如需以程式設計方式管理 COM + 的簡介，請參閱 [自動化 COM + 管理](automating-com--administration.md)。</span><span class="sxs-lookup"><span data-stu-id="174fe-118">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="174fe-119">備註</span><span class="sxs-lookup"><span data-stu-id="174fe-119">Remarks</span></span>

<span data-ttu-id="174fe-120">您無法直接建立 **COMAdminCatalogCollection** 物件。</span><span class="sxs-lookup"><span data-stu-id="174fe-120">You cannot directly create a **COMAdminCatalogCollection** object.</span></span> <span data-ttu-id="174fe-121">若要使用這個物件的方法，您必須建立 [**COMAdminCatalog**](comadmincatalog.md) 物件、取得 [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)的參考，然後使用 [**ICOMAdminCatalog：： >getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) 取得代表最上層集合的 [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) 介面參考。</span><span class="sxs-lookup"><span data-stu-id="174fe-121">To use the methods this object, you must create a [**COMAdminCatalog**](comadmincatalog.md) object, obtain a reference to [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), and then use [**ICOMAdminCatalog::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) to get a reference to an [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface that represents a top-level collection.</span></span> <span data-ttu-id="174fe-122">這會顯示在下列範例中，其中 "TopCollection" 必須取代為其中一個最上層 COM + 系統管理集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="174fe-122">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections.</span></span>


```C++
    HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
      (void**)&pCatalog); 
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pCatalog->GetCollection(L"TopCollection", 
      (IDispatch**)&pTopColl);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
```



<span data-ttu-id="174fe-123">若要從 Microsoft Visual Basic 使用這個類別，請將參考新增至 COM + 系統管理員類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="174fe-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="174fe-124">您可以藉由呼叫 [**COMAdminCatalog**](comadmincatalog.md)物件上的 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection)來建立 COMAdminCatalogCollection 物件。</span><span class="sxs-lookup"><span data-stu-id="174fe-124">A COMAdminCatalogCollection object can be created by calling [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) on a [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="174fe-125">這會顯示在下列範例中，其中 "TopCollection" 必須取代為其中一個最上層 COM + 系統管理集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="174fe-125">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections.</span></span>


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")

```



## <a name="requirements"></a><span data-ttu-id="174fe-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="174fe-126">Requirements</span></span>



| <span data-ttu-id="174fe-127">需求</span><span class="sxs-lookup"><span data-stu-id="174fe-127">Requirement</span></span> | <span data-ttu-id="174fe-128">值</span><span class="sxs-lookup"><span data-stu-id="174fe-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="174fe-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="174fe-129">Minimum supported client</span></span><br/> | <span data-ttu-id="174fe-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="174fe-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="174fe-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="174fe-131">Minimum supported server</span></span><br/> | <span data-ttu-id="174fe-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="174fe-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="174fe-133">標頭</span><span class="sxs-lookup"><span data-stu-id="174fe-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="174fe-134"><dt>ComAdmin。h</dt></span><span class="sxs-lookup"><span data-stu-id="174fe-134"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="174fe-135">Idl</span><span class="sxs-lookup"><span data-stu-id="174fe-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="174fe-136"><dt>ComAdmin .Idl</dt></span><span class="sxs-lookup"><span data-stu-id="174fe-136"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="174fe-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="174fe-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="174fe-138">**COMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="174fe-138">**COMAdminCatalog**</span></span>](comadmincatalog.md)
</dt> <dt>

[<span data-ttu-id="174fe-139">**COMAdminCatalogObject**</span><span class="sxs-lookup"><span data-stu-id="174fe-139">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
</dt> <dt>

[<span data-ttu-id="174fe-140">**ICatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="174fe-140">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
</dt> </dl>

 

 




