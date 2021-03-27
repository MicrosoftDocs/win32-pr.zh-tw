---
description: 從 Idlist.txt 內的 IPropertyStore 傳回屬性。
ms.assetid: D0BE2A9A-5832-4C0E-BFB6-96EB467C3D9D
title: CItemIDFactory::GetPropertyFromIDList 方法 (Shidfact.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 22aaec6d0616337a887f2876b51aaa744b205ba7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689816"
---
# <a name="citemidfactorygetpropertyfromidlist-methods"></a><span data-ttu-id="4cf41-103">CItemIDFactory：： GetPropertyFromIDList 方法</span><span class="sxs-lookup"><span data-stu-id="4cf41-103">CItemIDFactory::GetPropertyFromIDList methods</span></span>

<span data-ttu-id="4cf41-104">從 Idlist.txt 內的 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 傳回屬性。</span><span class="sxs-lookup"><span data-stu-id="4cf41-104">Returns a property from the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) within the IDList.</span></span>

### <a name="overload-list"></a><span data-ttu-id="4cf41-105">多載清單</span><span class="sxs-lookup"><span data-stu-id="4cf41-105">Overload list</span></span>



| <span data-ttu-id="4cf41-106">方法</span><span class="sxs-lookup"><span data-stu-id="4cf41-106">Method</span></span>                                                                        | <span data-ttu-id="4cf41-107">描述</span><span class="sxs-lookup"><span data-stu-id="4cf41-107">Description</span></span>                                                                                                                                   |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cf41-108">[**GetPropertyFromIDList**](/windows/win32/api/shidfact/nf-shidfact-citemidfactory-getpropertyfromidlist(pcuidlist_relative_pcwstr_propvariant))</span><span class="sxs-lookup"><span data-stu-id="4cf41-108">[**GetPropertyFromIDList**](/windows/win32/api/shidfact/nf-shidfact-citemidfactory-getpropertyfromidlist(pcuidlist_relative_pcwstr_propvariant))</span></span>     | <span data-ttu-id="4cf41-109">使用索引鍵，從 Idlist.txt 內的 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 取得屬性，做為變數。</span><span class="sxs-lookup"><span data-stu-id="4cf41-109">Gets a property from the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) within the IDList as a variant, using the key.</span></span><br/>            |
| <span data-ttu-id="4cf41-110">[**GetPropertyFromIDList**](/windows/win32/api/shidfact/nf-shidfact-citemidfactory-getpropertyfromidlist(pcuidlist_relative_pcwstr_propvariant))</span><span class="sxs-lookup"><span data-stu-id="4cf41-110">[**GetPropertyFromIDList**](/windows/win32/api/shidfact/nf-shidfact-citemidfactory-getpropertyfromidlist(pcuidlist_relative_pcwstr_propvariant))</span></span>    | <span data-ttu-id="4cf41-111">使用已命名的屬性，從 Idlist.txt 內的 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 取得以變異數為變數的屬性。</span><span class="sxs-lookup"><span data-stu-id="4cf41-111">Gets a property from the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) within the IDList as a variant, using the named property.</span></span><br/> |
| <span data-ttu-id="4cf41-112">[**GetPropertyFromIDList**]/windows/win32/api/shidfact/nf-shidfact-citemidfactory-getpropertyfromidlist (pcuidlist_relative_pcwstr_propvariant) ) </span><span class="sxs-lookup"><span data-stu-id="4cf41-112">[**GetPropertyFromIDList**]/windows/win32/api/shidfact/nf-shidfact-citemidfactory-getpropertyfromidlist(pcuidlist_relative_pcwstr_propvariant))</span></span>  | <span data-ttu-id="4cf41-113">使用索引鍵，從 Idlist.txt 內的 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 中取得屬性。</span><span class="sxs-lookup"><span data-stu-id="4cf41-113">Gets a property from the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) within the IDList, using the key.</span></span><br/>                         |
| <span data-ttu-id="4cf41-114">[**GetPropertyFromIDList**](/windows/win32/api/shidfact/nf-shidfact-citemidfactory-getpropertyfromidlist(pcuidlist_relative_pcwstr_propvariant))</span><span class="sxs-lookup"><span data-stu-id="4cf41-114">[**GetPropertyFromIDList**](/windows/win32/api/shidfact/nf-shidfact-citemidfactory-getpropertyfromidlist(pcuidlist_relative_pcwstr_propvariant))</span></span> | <span data-ttu-id="4cf41-115">使用命名屬性，從 Idlist.txt 內的 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 取得屬性。</span><span class="sxs-lookup"><span data-stu-id="4cf41-115">Gets a property from the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) within the IDList, using the named property.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="4cf41-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="4cf41-116">Requirements</span></span>



| <span data-ttu-id="4cf41-117">需求</span><span class="sxs-lookup"><span data-stu-id="4cf41-117">Requirement</span></span> | <span data-ttu-id="4cf41-118">值</span><span class="sxs-lookup"><span data-stu-id="4cf41-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4cf41-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4cf41-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4cf41-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4cf41-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4cf41-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4cf41-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4cf41-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4cf41-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4cf41-123">標頭</span><span class="sxs-lookup"><span data-stu-id="4cf41-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cf41-124"><dt>Shidfact。h</dt></span><span class="sxs-lookup"><span data-stu-id="4cf41-124"><dt>Shidfact.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cf41-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4cf41-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cf41-126">**CItemIDFactory**</span><span class="sxs-lookup"><span data-stu-id="4cf41-126">**CItemIDFactory**</span></span>](/windows/win32/api/shidfact/nl-shidfact-citemidfactory)
</dt> </dl>

 

 
