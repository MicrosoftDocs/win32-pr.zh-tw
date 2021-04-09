---
description: 定義方法，以取得搜尋專案屬性的相關資訊。 只有在 Windows XP 和 Windows Server 2003 上才支援這個介面，且不應再使用。
ms.assetid: 0fef34c5-f20f-475a-9223-5cb73079c842
title: IItemPropertyBag 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4da3db21947de6d35ef5e848499efc7f22633f7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112388"
---
# <a name="iitempropertybag-interface"></a><span data-ttu-id="b9dda-104">IItemPropertyBag 介面</span><span class="sxs-lookup"><span data-stu-id="b9dda-104">IItemPropertyBag interface</span></span>

<span data-ttu-id="b9dda-105">定義方法，以取得搜尋專案屬性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b9dda-105">Defines methods to obtain information about the properties of a search item.</span></span> <span data-ttu-id="b9dda-106">只有在 Windows XP 和 Windows Server 2003 上才支援這個介面，且不應再使用。</span><span class="sxs-lookup"><span data-stu-id="b9dda-106">This interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="b9dda-107">成員</span><span class="sxs-lookup"><span data-stu-id="b9dda-107">Members</span></span>

<span data-ttu-id="b9dda-108">**IItemPropertyBag** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="b9dda-108">The **IItemPropertyBag** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b9dda-109">**IItemPropertyBag** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b9dda-109">**IItemPropertyBag** also has these types of members:</span></span>

-   [<span data-ttu-id="b9dda-110">方法</span><span class="sxs-lookup"><span data-stu-id="b9dda-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b9dda-111">方法</span><span class="sxs-lookup"><span data-stu-id="b9dda-111">Methods</span></span>

<span data-ttu-id="b9dda-112">**IItemPropertyBag** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b9dda-112">The **IItemPropertyBag** interface has these methods.</span></span>



| <span data-ttu-id="b9dda-113">方法</span><span class="sxs-lookup"><span data-stu-id="b9dda-113">Method</span></span>                                                      | <span data-ttu-id="b9dda-114">描述</span><span class="sxs-lookup"><span data-stu-id="b9dda-114">Description</span></span>                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9dda-115">[**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b9dda-115">[**CountProperties**](/previous-versions/windows/desktop/legacy/ff684387(v=vs.85))</span></span> | <span data-ttu-id="b9dda-116">取得屬性包中屬性數目的計數。</span><span class="sxs-lookup"><span data-stu-id="b9dda-116">Gets a count of the number of properties in the property bag.</span></span><br/>                     |
| [<span data-ttu-id="b9dda-117">**GetPropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="b9dda-117">**GetPropertyInfo**</span></span>](iitempropertybag-getpropertyinfo.md) | <span data-ttu-id="b9dda-118">取得讀取或儲存屬性包中的屬性所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="b9dda-118">Gets the information required to read or save the properties in the property bag.</span></span><br/> |
| [<span data-ttu-id="b9dda-119">**讀**</span><span class="sxs-lookup"><span data-stu-id="b9dda-119">**Read**</span></span>](iitempropertybag-read.md)                       | <span data-ttu-id="b9dda-120">使一或多個屬性從屬性包中讀取。</span><span class="sxs-lookup"><span data-stu-id="b9dda-120">Causes one or more properties to be read from the property bag.</span></span><br/>                   |
| [<span data-ttu-id="b9dda-121">**寫**</span><span class="sxs-lookup"><span data-stu-id="b9dda-121">**Write**</span></span>](iitempropertybag-write.md)                     | <span data-ttu-id="b9dda-122">導致一或多個屬性儲存在屬性包中。</span><span class="sxs-lookup"><span data-stu-id="b9dda-122">Causes one or more properties to be saved into the property bag.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="b9dda-123">備註</span><span class="sxs-lookup"><span data-stu-id="b9dda-123">Remarks</span></span>

<span data-ttu-id="b9dda-124">只有在 Windows XP 和 Windows Server 2003 上才支援 **IItemPropertyBag** 介面，且不應再使用。</span><span class="sxs-lookup"><span data-stu-id="b9dda-124">The **IItemPropertyBag** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="b9dda-125">若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 **IItemPropertyBag** 介面和下列 Api： [**ISearchProtocolUI**](-search-isearchprotocolui.md)、 [**IItemPreviewerExt**](-search-iitempreviewerext.md) 和 [**ISearchItem**](-search-isearchitem.md) 介面、 [**LINKINFO**](-search-linkinfo.md) 和 [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) 結構，以及 [**LINKTYPE**](-search-linktype.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="b9dda-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **IItemPropertyBag** interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9dda-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9dda-126">Requirements</span></span>



| <span data-ttu-id="b9dda-127">需求</span><span class="sxs-lookup"><span data-stu-id="b9dda-127">Requirement</span></span> | <span data-ttu-id="b9dda-128">值</span><span class="sxs-lookup"><span data-stu-id="b9dda-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b9dda-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b9dda-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b9dda-130">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9dda-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b9dda-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b9dda-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b9dda-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9dda-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b9dda-133">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="b9dda-133">Redistributable</span></span><br/>          | <span data-ttu-id="b9dda-134">Windows 桌面搜尋 (WDS) 3。0</span><span class="sxs-lookup"><span data-stu-id="b9dda-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
