---
description: 使一或多個屬性從屬性包中讀取。 只有在 Windows XP 和 Windows Server 2003 上才支援 IItemPropertyBag 介面，且不應再使用。
ms.assetid: 78a63ef0-1b79-4b07-9121-a6fbd1116c4b
title: IItemPropertyBag：： Read 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: ef7af13dc42239a2823d7e7ca9b8def4748519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318152"
---
# <a name="iitempropertybagread-method"></a><span data-ttu-id="93006-104">IItemPropertyBag：： Read 方法</span><span class="sxs-lookup"><span data-stu-id="93006-104">IItemPropertyBag::Read method</span></span>

<span data-ttu-id="93006-105">使一或多個屬性從屬性包中讀取。</span><span class="sxs-lookup"><span data-stu-id="93006-105">Causes one or more properties to be read from the property bag.</span></span> <span data-ttu-id="93006-106">只有在 Windows XP 和 Windows Server 2003 上才支援 [**IItemPropertyBag**](iitempropertybag.md) 介面，且不應再使用。</span><span class="sxs-lookup"><span data-stu-id="93006-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="93006-107">語法</span><span class="sxs-lookup"><span data-stu-id="93006-107">Syntax</span></span>


```C++
HRESULT Read(
  [in]  ULONG    cProperties,
  [in]  ITEMPROP *pPropBag,
  [out] VARIANT  *pvarValue,
  [out] HRESULT  *phrError
);
```



## <a name="parameters"></a><span data-ttu-id="93006-108">參數</span><span class="sxs-lookup"><span data-stu-id="93006-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93006-109">*cProperties* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93006-109">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93006-110">要讀取的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="93006-110">The number of properties to read.</span></span> <span data-ttu-id="93006-111">這個引數會指定陣列中 *pPropBag*、 *pvarValue* 和 *phrError* 的元素數目。</span><span class="sxs-lookup"><span data-stu-id="93006-111">This argument specifies the number of elements in the arrays at *pPropBag*, *pvarValue*, and *phrError*.</span></span>

</dd> <dt>

<span data-ttu-id="93006-112">*pPropBag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="93006-112">*pPropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93006-113">[**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop)結構陣列的指標，指定所要求的屬性。</span><span class="sxs-lookup"><span data-stu-id="93006-113">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that specifies the properties that are requested.</span></span>

</dd> <dt>

<span data-ttu-id="93006-114">*pvarValue* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="93006-114">*pvarValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93006-115">接收傳回 **VARIANT** 結構陣列的指標，此陣列會接收屬性值。</span><span class="sxs-lookup"><span data-stu-id="93006-115">Receives a pointer that returns an array of **VARIANT** structures that receives the property values.</span></span>

</dd> <dt>

<span data-ttu-id="93006-116">*phrError* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="93006-116">*phrError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93006-117">**HRESULT** 值陣列的指標，這些值會接收每個讀取之屬性的結果。</span><span class="sxs-lookup"><span data-stu-id="93006-117">Pointer to an array of **HRESULT** values that receives the result of each property read.</span></span> <span data-ttu-id="93006-118">此陣列中至少必須有 *cProperties* 元素。</span><span class="sxs-lookup"><span data-stu-id="93006-118">There must be at least *cProperties* elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93006-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="93006-119">Return value</span></span>

<span data-ttu-id="93006-120">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="93006-120">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="93006-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="93006-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="93006-122">備註</span><span class="sxs-lookup"><span data-stu-id="93006-122">Remarks</span></span>

<span data-ttu-id="93006-123">只有在 Windows XP 和 Windows Server 2003 上才支援 [**IItemPropertyBag**](iitempropertybag.md) 介面，且不應再使用。</span><span class="sxs-lookup"><span data-stu-id="93006-123">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="93006-124">若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 [**IItemPropertyBag**](iitempropertybag.md) 介面和下列 Api： [**ISearchProtocolUI**](-search-isearchprotocolui.md)、 [**IItemPreviewerExt**](-search-iitempreviewerext.md) 和 [**ISearchItem**](-search-isearchitem.md) 介面、 [**LINKINFO**](-search-linkinfo.md) 和 [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) 結構，以及 [**LINKTYPE**](-search-linktype.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="93006-124">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="93006-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="93006-125">Requirements</span></span>



| <span data-ttu-id="93006-126">需求</span><span class="sxs-lookup"><span data-stu-id="93006-126">Requirement</span></span> | <span data-ttu-id="93006-127">值</span><span class="sxs-lookup"><span data-stu-id="93006-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="93006-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93006-128">Minimum supported client</span></span><br/> | <span data-ttu-id="93006-129">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93006-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="93006-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93006-130">Minimum supported server</span></span><br/> | <span data-ttu-id="93006-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93006-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="93006-132">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="93006-132">Redistributable</span></span><br/>          | <span data-ttu-id="93006-133">Windows 桌面搜尋 (WDS) 3。0</span><span class="sxs-lookup"><span data-stu-id="93006-133">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="93006-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93006-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93006-135">**IItemPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="93006-135">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 




