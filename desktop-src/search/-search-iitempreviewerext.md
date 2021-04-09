---
description: 提供提供瀏覽器設定的方法。 只有在 Windows XP 和 Windows Server 2003 上才支援 IItemPreviewerExt 介面，且不應再使用。
ms.assetid: d7d6cbb0-18bf-4e68-b7b4-307cadbced5c
title: IItemPreviewerExt 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt
api_type:
- COM
api_location: ''
ms.openlocfilehash: 820ddfdf73d36a7cba968a721872b1e9fb33a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943278"
---
# <a name="iitempreviewerext-interface"></a><span data-ttu-id="a90d6-104">IItemPreviewerExt 介面</span><span class="sxs-lookup"><span data-stu-id="a90d6-104">IItemPreviewerExt interface</span></span>

<span data-ttu-id="a90d6-105">提供提供瀏覽器設定的方法。</span><span class="sxs-lookup"><span data-stu-id="a90d6-105">Provides methods for supplying browser settings.</span></span> <span data-ttu-id="a90d6-106">只有在 Windows XP 和 Windows Server 2003 上才支援 **IItemPreviewerExt** 介面，且不應再使用。</span><span class="sxs-lookup"><span data-stu-id="a90d6-106">The **IItemPreviewerExt** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="a90d6-107">成員</span><span class="sxs-lookup"><span data-stu-id="a90d6-107">Members</span></span>

<span data-ttu-id="a90d6-108">**IItemPreviewerExt** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="a90d6-108">The **IItemPreviewerExt** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a90d6-109">**IItemPreviewerExt** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a90d6-109">**IItemPreviewerExt** also has these types of members:</span></span>

-   [<span data-ttu-id="a90d6-110">方法</span><span class="sxs-lookup"><span data-stu-id="a90d6-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a90d6-111">方法</span><span class="sxs-lookup"><span data-stu-id="a90d6-111">Methods</span></span>

<span data-ttu-id="a90d6-112">**IItemPreviewerExt** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a90d6-112">The **IItemPreviewerExt** interface has these methods.</span></span>



| <span data-ttu-id="a90d6-113">方法</span><span class="sxs-lookup"><span data-stu-id="a90d6-113">Method</span></span>                                                                               | <span data-ttu-id="a90d6-114">描述</span><span class="sxs-lookup"><span data-stu-id="a90d6-114">Description</span></span>                                                                                  |
|:-------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a90d6-115">**GetLinkedContent**</span><span class="sxs-lookup"><span data-stu-id="a90d6-115">**GetLinkedContent**</span></span>](-search-iitempreviewerext-getlinkedcontent.md)               | <span data-ttu-id="a90d6-116">允許延伸至屬性的豐富內容。</span><span class="sxs-lookup"><span data-stu-id="a90d6-116">Permits the extension to rich content for a property.</span></span> <br/>                            |
| [<span data-ttu-id="a90d6-117">**GetRelatedPart**</span><span class="sxs-lookup"><span data-stu-id="a90d6-117">**GetRelatedPart**</span></span>](-search-iitempreviewerext-getrelatedpart.md)                   | <span data-ttu-id="a90d6-118">取得要內嵌至輸出 MHTML 資料流程的相關主體部分。</span><span class="sxs-lookup"><span data-stu-id="a90d6-118">Gets a related body part for embedding into the output MHTML stream.</span></span><br/>              |
| [<span data-ttu-id="a90d6-119">**ProcessTransformCommand**</span><span class="sxs-lookup"><span data-stu-id="a90d6-119">**ProcessTransformCommand**</span></span>](-search-iitempreviewerext-processtransformcommand.md) | <span data-ttu-id="a90d6-120">允許處理在預覽範本中遇到的轉換命令。</span><span class="sxs-lookup"><span data-stu-id="a90d6-120">Permits processing of a transformation command encountered in a preview template.</span></span><br/> |
| [<span data-ttu-id="a90d6-121">**SuggestBrowserPolicy**</span><span class="sxs-lookup"><span data-stu-id="a90d6-121">**SuggestBrowserPolicy**</span></span>](-search-iitempreviewerext-suggestbrowserpolicy.md)       | <span data-ttu-id="a90d6-122">建議要套用至瀏覽器的安全性原則。</span><span class="sxs-lookup"><span data-stu-id="a90d6-122">Suggests the security policy to be applied to the browser.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="a90d6-123">備註</span><span class="sxs-lookup"><span data-stu-id="a90d6-123">Remarks</span></span>

<span data-ttu-id="a90d6-124">只有在 Windows XP 和 Windows Server 2003 上才支援 **IItemPreviewerExt** 介面，且不應再使用。</span><span class="sxs-lookup"><span data-stu-id="a90d6-124">The **IItemPreviewerExt** interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="a90d6-125">若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 **IItemPreviewerExt** 介面和下列 Api： [**ISearchProtocolUI**](-search-isearchprotocolui.md)、 [**IItemPropertyBag**](iitempropertybag.md) 和 [**ISearchItem**](-search-isearchitem.md) 介面、 [**LINKINFO**](-search-linkinfo.md) 結構和 [**LINKTYPE**](-search-linktype.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="a90d6-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **IItemPreviewerExt** interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="a90d6-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="a90d6-126">Requirements</span></span>



| <span data-ttu-id="a90d6-127">需求</span><span class="sxs-lookup"><span data-stu-id="a90d6-127">Requirement</span></span> | <span data-ttu-id="a90d6-128">值</span><span class="sxs-lookup"><span data-stu-id="a90d6-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a90d6-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a90d6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a90d6-130">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a90d6-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a90d6-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a90d6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a90d6-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a90d6-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a90d6-133">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="a90d6-133">Redistributable</span></span><br/>          | <span data-ttu-id="a90d6-134">Windows 桌面搜尋 (WDS) 3。0</span><span class="sxs-lookup"><span data-stu-id="a90d6-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 
