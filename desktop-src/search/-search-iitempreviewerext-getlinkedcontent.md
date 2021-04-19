---
description: 允許延伸至屬性的豐富內容。
ms.assetid: d1b09ea0-7263-4b7c-8c59-25251bb6b285
title: IItemPreviewerExt：： GetLinkedContent 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetLinkedContent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7d450bbda2ac7c24b49d1ca5032fd1c59754652e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972821"
---
# <a name="iitempreviewerextgetlinkedcontent-method"></a><span data-ttu-id="1840f-103">IItemPreviewerExt：： GetLinkedContent 方法</span><span class="sxs-lookup"><span data-stu-id="1840f-103">IItemPreviewerExt::GetLinkedContent method</span></span>

<span data-ttu-id="1840f-104">允許延伸至屬性的豐富內容。</span><span class="sxs-lookup"><span data-stu-id="1840f-104">Permits the extension to rich content for a property.</span></span>

## <a name="syntax"></a><span data-ttu-id="1840f-105">語法</span><span class="sxs-lookup"><span data-stu-id="1840f-105">Syntax</span></span>


```C++
HRESULT GetLinkedContent(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="1840f-106">參數</span><span class="sxs-lookup"><span data-stu-id="1840f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1840f-107">*dwCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1840f-107">*dwContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1840f-108">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1840f-108">Type: **DWORD**</span></span>

<span data-ttu-id="1840f-109">作業的內容識別碼。</span><span class="sxs-lookup"><span data-stu-id="1840f-109">The context identifier for the operation.</span></span> <span data-ttu-id="1840f-110">覆寫 *dwCoNtext* 預設值，將內容識別碼設定為您選擇的值。</span><span class="sxs-lookup"><span data-stu-id="1840f-110">Override the *dwContext* default to set the context identifier to a value of your choosing.</span></span>

</dd> <dt>

<span data-ttu-id="1840f-111">*pwszProp* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1840f-111">*pwszProp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1840f-112">類型： **LPCOLESTR**</span><span class="sxs-lookup"><span data-stu-id="1840f-112">Type: **LPCOLESTR**</span></span>

<span data-ttu-id="1840f-113">作為 Unicode 字串之連結內容的屬性指標。</span><span class="sxs-lookup"><span data-stu-id="1840f-113">A pointer to the property of the linked content as a Unicode string.</span></span>

</dd> <dt>

<span data-ttu-id="1840f-114">*pInfo* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="1840f-114">*pInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1840f-115">類型： \**[**LINKINFO**](-search-linkinfo.md) \** _</span><span class="sxs-lookup"><span data-stu-id="1840f-115">Type: \**[**LINKINFO**](-search-linkinfo.md)\** _</span></span>

<span data-ttu-id="1840f-116">接收 [_ *LINKINFO* \*](-search-linkinfo.md)結構的指標，此結構的方法會傳回交易的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1840f-116">Receives a pointer to the [_ *LINKINFO*\*](-search-linkinfo.md) structure in which the method returns information about the transaction.</span></span> <span data-ttu-id="1840f-117">*pInfo* 不得為 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="1840f-117">*pInfo* must not be a **NULL** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1840f-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="1840f-118">Return value</span></span>

<span data-ttu-id="1840f-119">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1840f-119">Type: **HRESULT**</span></span>

<span data-ttu-id="1840f-120">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="1840f-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1840f-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1840f-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1840f-122">備註</span><span class="sxs-lookup"><span data-stu-id="1840f-122">Remarks</span></span>

<span data-ttu-id="1840f-123">只有在 Windows XP 和 Windows Server 2003 上才支援 [**IItemPreviewerExt**](-search-iitempreviewerext.md) 介面，且不應再使用。</span><span class="sxs-lookup"><span data-stu-id="1840f-123">The [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="1840f-124">若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 [**IItemPreviewerExt**](-search-iitempreviewerext.md) 介面和下列 Api： [**ISearchProtocolUI**](-search-isearchprotocolui.md)、 [**IItemPropertyBag**](iitempropertybag.md) 和 [**ISearchItem**](-search-isearchitem.md) 介面、 [**LINKINFO**](-search-linkinfo.md) 結構和 [**LINKTYPE**](-search-linktype.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="1840f-124">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface, and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="1840f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="1840f-125">Requirements</span></span>



| <span data-ttu-id="1840f-126">需求</span><span class="sxs-lookup"><span data-stu-id="1840f-126">Requirement</span></span> | <span data-ttu-id="1840f-127">值</span><span class="sxs-lookup"><span data-stu-id="1840f-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1840f-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1840f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1840f-129">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1840f-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1840f-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1840f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1840f-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1840f-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1840f-132">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="1840f-132">Redistributable</span></span><br/>          | <span data-ttu-id="1840f-133">Windows 桌面搜尋 (WDS) 3。0</span><span class="sxs-lookup"><span data-stu-id="1840f-133">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="1840f-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1840f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1840f-135">**IItemPreviewerExt**</span><span class="sxs-lookup"><span data-stu-id="1840f-135">**IItemPreviewerExt**</span></span>](-search-iitempreviewerext.md)
</dt> </dl>

 

 




