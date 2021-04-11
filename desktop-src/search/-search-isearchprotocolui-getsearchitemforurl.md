---
description: 取得指定之資料的搜尋專案。 針對收集程式所處理的每個 URL，會呼叫這個方法一次，並抓取 ISearchItem 物件的指標。
ms.assetid: 35893bc9-8327-44f9-a9fc-7855c5c063e3
title: ISearchProtocolUI：： GetSearchItemForUrl 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI.GetSearchItemForUrl
api_type:
- COM
api_location: ''
ms.openlocfilehash: f8a9bbe3459109946b7a4789d9b9f0fb7473ff05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689876"
---
# <a name="isearchprotocoluigetsearchitemforurl-method"></a><span data-ttu-id="79103-104">ISearchProtocolUI：： GetSearchItemForUrl 方法</span><span class="sxs-lookup"><span data-stu-id="79103-104">ISearchProtocolUI::GetSearchItemForUrl method</span></span>

<span data-ttu-id="79103-105">取得指定之資料的搜尋專案。</span><span class="sxs-lookup"><span data-stu-id="79103-105">Gets the search item for the data specified.</span></span> <span data-ttu-id="79103-106">針對收集程式所處理的每個 URL，會呼叫這個方法一次，並抓取 [**ISearchItem**](-search-isearchitem.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="79103-106">This method is called once for every URL processed by the gatherer, and retrieves a pointer to the [**ISearchItem**](-search-isearchitem.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="79103-107">語法</span><span class="sxs-lookup"><span data-stu-id="79103-107">Syntax</span></span>


```C++
HRESULT GetSearchItemForUrl(
  [in]          LPCOLESTR        pcwszURL,
  [in]          IItemPropertyBag *pPropertyBag,
  [out, retval] ISearchItem      **ppSearchItem
);
```



## <a name="parameters"></a><span data-ttu-id="79103-108">參數</span><span class="sxs-lookup"><span data-stu-id="79103-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79103-109">*pcwszURL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="79103-109">*pcwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79103-110">類型： **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="79103-110">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="79103-111">Null 資料終止的 Unicode 字串指標，其中包含要存取之 URL 的搜尋專案。</span><span class="sxs-lookup"><span data-stu-id="79103-111">Pointer to a null data terminated Unicode string containing the search item for the URL being accessed.</span></span>

</dd> <dt>

<span data-ttu-id="79103-112">*pPropertyBag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="79103-112">*pPropertyBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79103-113">類型： \**IItemPropertyBag \** _</span><span class="sxs-lookup"><span data-stu-id="79103-113">Type: \**IItemPropertyBag\** _</span></span>

<span data-ttu-id="79103-114">[_ *IItemPropertyBag* \*](iitempropertybag.md)物件的指標，其中包含搜尋專案的相關資訊，包括專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="79103-114">Pointer to an [_ *IItemPropertyBag*\*](iitempropertybag.md) object that contains information about the search item, including the properties of the item.</span></span>

</dd> <dt>

<span data-ttu-id="79103-115">*ppSearchItem* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="79103-115">*ppSearchItem* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="79103-116">類型： **[ **ISearchItem**](-search-isearchitem.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="79103-116">Type: **[**ISearchItem**](-search-isearchitem.md)\*\***</span></span>

<span data-ttu-id="79103-117">接收這個方法所建立之 [**ISearchItem**](-search-isearchitem.md) 物件的指標位址。</span><span class="sxs-lookup"><span data-stu-id="79103-117">Receives the address of a pointer to the [**ISearchItem**](-search-isearchitem.md) object created by this method.</span></span> <span data-ttu-id="79103-118">此物件包含搜尋專案的相關資訊，例如專案的檔案名。</span><span class="sxs-lookup"><span data-stu-id="79103-118">This object contains information about the search item, such as the item's file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79103-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="79103-119">Return value</span></span>

<span data-ttu-id="79103-120">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="79103-120">Type: **HRESULT**</span></span>

<span data-ttu-id="79103-121">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="79103-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="79103-122">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="79103-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="79103-123">備註</span><span class="sxs-lookup"><span data-stu-id="79103-123">Remarks</span></span>

<span data-ttu-id="79103-124">只有在 Windows XP 和 Windows Server 2003 上才支援 **ISearchProtocolUI：： GetSearchItemForUrl** 方法，且不應再使用。</span><span class="sxs-lookup"><span data-stu-id="79103-124">The **ISearchProtocolUI::GetSearchItemForUrl** method is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="79103-125">若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 [**ISearchProtocolUI**](-search-isearchprotocolui.md) 介面和下列 Api： [**IItemPreviewerExt**](-search-iitempreviewerext.md)、 [**IItemPropertyBag**](iitempropertybag.md) 和 [**ISearchItem**](-search-isearchitem.md) 介面、 [**LINKINFO**](-search-linkinfo.md) 結構和 [**LINKTYPE**](-search-linktype.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="79103-125">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**ISearchProtocolUI**](-search-isearchprotocolui.md) interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="79103-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="79103-126">Requirements</span></span>



| <span data-ttu-id="79103-127">需求</span><span class="sxs-lookup"><span data-stu-id="79103-127">Requirement</span></span> | <span data-ttu-id="79103-128">值</span><span class="sxs-lookup"><span data-stu-id="79103-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="79103-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="79103-129">Minimum supported client</span></span><br/> | <span data-ttu-id="79103-130">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79103-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="79103-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="79103-131">Minimum supported server</span></span><br/> | <span data-ttu-id="79103-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79103-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="79103-133">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="79103-133">Redistributable</span></span><br/>          | <span data-ttu-id="79103-134">Windows 桌面搜尋 (WDS) 3。0</span><span class="sxs-lookup"><span data-stu-id="79103-134">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="79103-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79103-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79103-136">**ISearchProtocolUI**</span><span class="sxs-lookup"><span data-stu-id="79103-136">**ISearchProtocolUI**</span></span>](-search-isearchprotocolui.md)
</dt> </dl>

 

 




