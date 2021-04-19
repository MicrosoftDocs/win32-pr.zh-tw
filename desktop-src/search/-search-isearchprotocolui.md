---
description: 提供叫用 ISearchItem 物件的方法。
ms.assetid: b52fd64b-b03a-4d02-a64f-201f6b7d5045
title: ISearchProtocolUI 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3923ddaff014d393690be31c0e0ca2be94a3cb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967095"
---
# <a name="isearchprotocolui-interface"></a><span data-ttu-id="24b62-103">ISearchProtocolUI 介面</span><span class="sxs-lookup"><span data-stu-id="24b62-103">ISearchProtocolUI interface</span></span>

<span data-ttu-id="24b62-104">提供叫用 [**ISearchItem**](-search-isearchitem.md) 物件的方法。</span><span class="sxs-lookup"><span data-stu-id="24b62-104">Provides a method for invoking [**ISearchItem**](-search-isearchitem.md) objects.</span></span> <span data-ttu-id="24b62-105">當處理來自收集程式的 Url 時，通訊協定主機會呼叫此介面中的方法。</span><span class="sxs-lookup"><span data-stu-id="24b62-105">Methods in this interface are called by the protocol host when processing URLs from the gatherer.</span></span> <span data-ttu-id="24b62-106">通訊協定處理常式會執行以原生格式存取內容來源的通訊協定，而此介面會執行自訂的通訊協定處理常式，以展開可編制索引的資料來源。</span><span class="sxs-lookup"><span data-stu-id="24b62-106">The protocol handler implements the protocol for accessing a content source in its native format, and this interface implements a custom protocol handler to expand the data sources that can be indexed.</span></span>

## <a name="members"></a><span data-ttu-id="24b62-107">成員</span><span class="sxs-lookup"><span data-stu-id="24b62-107">Members</span></span>

<span data-ttu-id="24b62-108">**ISearchProtocolUI** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="24b62-108">The **ISearchProtocolUI** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="24b62-109">**ISearchProtocolUI** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="24b62-109">**ISearchProtocolUI** also has these types of members:</span></span>

-   [<span data-ttu-id="24b62-110">方法</span><span class="sxs-lookup"><span data-stu-id="24b62-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="24b62-111">方法</span><span class="sxs-lookup"><span data-stu-id="24b62-111">Methods</span></span>

<span data-ttu-id="24b62-112">**ISearchProtocolUI** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="24b62-112">The **ISearchProtocolUI** interface has these methods.</span></span>



| <span data-ttu-id="24b62-113">方法</span><span class="sxs-lookup"><span data-stu-id="24b62-113">Method</span></span>                                                                       | <span data-ttu-id="24b62-114">描述</span><span class="sxs-lookup"><span data-stu-id="24b62-114">Description</span></span>                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24b62-115">**GetSearchItemForUrl**</span><span class="sxs-lookup"><span data-stu-id="24b62-115">**GetSearchItemForUrl**</span></span>](-search-isearchprotocolui-getsearchitemforurl.md) | <span data-ttu-id="24b62-116">取得指定之資料的搜尋專案。</span><span class="sxs-lookup"><span data-stu-id="24b62-116">Gets the search item for the data specified.</span></span> <span data-ttu-id="24b62-117">針對收集程式所處理的每個 URL，會呼叫這個方法一次，並抓取 [**ISearchItem**](-search-isearchitem.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="24b62-117">This method is called once for every URL processed by the gatherer, and retrieves a pointer to the [**ISearchItem**](-search-isearchitem.md) object.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="24b62-118">備註</span><span class="sxs-lookup"><span data-stu-id="24b62-118">Remarks</span></span>

<span data-ttu-id="24b62-119">只有在 Windows XP 和 Windows Server 2003 上才支援 **ISearchProtocolUI** 介面，且不應再使用。</span><span class="sxs-lookup"><span data-stu-id="24b62-119">The **ISearchProtocolUI** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="24b62-120">若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 **ISearchProtocolUI** 介面和下列 Api： [**IItemPreviewerExt**](-search-iitempreviewerext.md)、 [**IItemPropertyBag**](iitempropertybag.md) 和 [**ISearchItem**](-search-isearchitem.md) 介面、 [**LINKINFO**](-search-linkinfo.md) 結構和 [**LINKTYPE**](-search-linktype.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="24b62-120">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **ISearchProtocolUI** interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="24b62-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="24b62-121">Requirements</span></span>



| <span data-ttu-id="24b62-122">需求</span><span class="sxs-lookup"><span data-stu-id="24b62-122">Requirement</span></span> | <span data-ttu-id="24b62-123">值</span><span class="sxs-lookup"><span data-stu-id="24b62-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="24b62-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="24b62-124">Minimum supported client</span></span><br/> | <span data-ttu-id="24b62-125">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24b62-125">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="24b62-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="24b62-126">Minimum supported server</span></span><br/> | <span data-ttu-id="24b62-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="24b62-127">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="24b62-128">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="24b62-128">Redistributable</span></span><br/>          | <span data-ttu-id="24b62-129">Windows 桌面搜尋 (WDS) 3。0</span><span class="sxs-lookup"><span data-stu-id="24b62-129">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
