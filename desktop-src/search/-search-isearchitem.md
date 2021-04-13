---
description: 提供方法來定義使用者介面 (UI) 和索引子所建立之搜尋命名空間物件之間的互動。
ms.assetid: e48c9e5b-9b15-4bc1-91ef-81ba7a05bfbd
title: ISearchItem 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem
api_type:
- COM
api_location: ''
ms.openlocfilehash: c6c0fd5b534c13f8fae2e6759645ac812fc3986c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386126"
---
# <a name="isearchitem-interface"></a><span data-ttu-id="c0a6c-103">ISearchItem 介面</span><span class="sxs-lookup"><span data-stu-id="c0a6c-103">ISearchItem interface</span></span>

<span data-ttu-id="c0a6c-104">提供方法來定義使用者介面 (UI) 和索引子所建立之搜尋命名空間物件之間的互動。</span><span class="sxs-lookup"><span data-stu-id="c0a6c-104">Provides methods that define interaction between a user interface (UI) and the Search namespace objects created by the indexer.</span></span>

## <a name="members"></a><span data-ttu-id="c0a6c-105">成員</span><span class="sxs-lookup"><span data-stu-id="c0a6c-105">Members</span></span>

<span data-ttu-id="c0a6c-106">**ISearchItem** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="c0a6c-106">The **ISearchItem** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c0a6c-107">**ISearchItem** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c0a6c-107">**ISearchItem** also has these types of members:</span></span>

-   [<span data-ttu-id="c0a6c-108">方法</span><span class="sxs-lookup"><span data-stu-id="c0a6c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c0a6c-109">方法</span><span class="sxs-lookup"><span data-stu-id="c0a6c-109">Methods</span></span>

<span data-ttu-id="c0a6c-110">**ISearchItem** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c0a6c-110">The **ISearchItem** interface has these methods.</span></span>



| <span data-ttu-id="c0a6c-111">方法</span><span class="sxs-lookup"><span data-stu-id="c0a6c-111">Method</span></span>                                                         | <span data-ttu-id="c0a6c-112">描述</span><span class="sxs-lookup"><span data-stu-id="c0a6c-112">Description</span></span>                                                                                                                               |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0a6c-113">**GetParentFolder**</span><span class="sxs-lookup"><span data-stu-id="c0a6c-113">**GetParentFolder**</span></span>](-search-isearchitem-getparentfolder.md) | <span data-ttu-id="c0a6c-114">如果 URL 代表實際的 Shell 資料來源 (也稱為 Shell 命名空間延伸) ，則取得 **ISearchItem** 物件。</span><span class="sxs-lookup"><span data-stu-id="c0a6c-114">Gets the **ISearchItem** object if the URL represents an actual Shell data source (also known as a Shell namespace extension).</span></span><br/> |
| <span data-ttu-id="c0a6c-115">[**GetUIObjectOf**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c0a6c-115">[**GetUIObjectOf**](/previous-versions/windows/desktop/legacy/dd756721(v=vs.85))</span></span>     | <span data-ttu-id="c0a6c-116">取得 **ISearchItem** 的使用者介面 (UI) 物件。</span><span class="sxs-lookup"><span data-stu-id="c0a6c-116">Gets the user interface (UI) object of **ISearchItem**.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="c0a6c-117">備註</span><span class="sxs-lookup"><span data-stu-id="c0a6c-117">Remarks</span></span>

<span data-ttu-id="c0a6c-118">只有在 Windows XP 和 Windows Server 2003 上才支援 [**ISearchItem：： GetParentFolder**](-search-isearchitem-getparentfolder.md) ，且不應再使用。</span><span class="sxs-lookup"><span data-stu-id="c0a6c-118">The [**ISearchItem::GetParentFolder**](-search-isearchitem-getparentfolder.md) is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="c0a6c-119">若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 **ISearchItem** 介面和下列 Api： [**IItemPreviewerExt**](-search-iitempreviewerext.md)、 [**IItemPropertyBag**](iitempropertybag.md)和 [**ISearchProtocolUI**](-search-isearchprotocolui.md) 介面、 [**LINKINFO**](-search-linkinfo.md) 結構和 [**LINKTYPE**](-search-linktype.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="c0a6c-119">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **ISearchItem** interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md), and [**ISearchProtocolUI**](-search-isearchprotocolui.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0a6c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0a6c-120">Requirements</span></span>



| <span data-ttu-id="c0a6c-121">需求</span><span class="sxs-lookup"><span data-stu-id="c0a6c-121">Requirement</span></span> | <span data-ttu-id="c0a6c-122">值</span><span class="sxs-lookup"><span data-stu-id="c0a6c-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c0a6c-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0a6c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c0a6c-124">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0a6c-124">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c0a6c-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0a6c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c0a6c-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0a6c-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c0a6c-127">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="c0a6c-127">Redistributable</span></span><br/>          | <span data-ttu-id="c0a6c-128">Windows 桌面搜尋 (WDS) 3。0</span><span class="sxs-lookup"><span data-stu-id="c0a6c-128">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
