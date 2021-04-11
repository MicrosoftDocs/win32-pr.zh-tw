---
description: 導致一或多個屬性儲存在屬性包中。 只有在 Windows XP 和 Windows Server 2003 上才支援 IItemPropertyBag 介面，且不應再使用。
ms.assetid: 35491fbc-fb1c-4bad-86e8-9f19856ed7cb
title: IItemPropertyBag：： Write 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7df66487bba0c2bbef40cf3642754dff56f65835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112392"
---
# <a name="iitempropertybagwrite-method"></a><span data-ttu-id="f0d63-104">IItemPropertyBag：： Write 方法</span><span class="sxs-lookup"><span data-stu-id="f0d63-104">IItemPropertyBag::Write method</span></span>

<span data-ttu-id="f0d63-105">導致一或多個屬性儲存在屬性包中。</span><span class="sxs-lookup"><span data-stu-id="f0d63-105">Causes one or more properties to be saved into the property bag.</span></span> <span data-ttu-id="f0d63-106">只有在 Windows XP 和 Windows Server 2003 上才支援 [**IItemPropertyBag**](iitempropertybag.md) 介面，且不應再使用。</span><span class="sxs-lookup"><span data-stu-id="f0d63-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0d63-107">語法</span><span class="sxs-lookup"><span data-stu-id="f0d63-107">Syntax</span></span>


```C++
HRESULT Write(
  [in] ULONG    cProperties,
  [in] ITEMPROP *pPropBag,
  [in] VARIANT  *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="f0d63-108">參數</span><span class="sxs-lookup"><span data-stu-id="f0d63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0d63-109">*cProperties* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0d63-109">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0d63-110">要儲存的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="f0d63-110">The number of properties to save.</span></span> <span data-ttu-id="f0d63-111">這個引數會指定 *pPropBag* 和 *pvarValue* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="f0d63-111">This argument specifies the number of elements in the arrays at *pPropBag* and *pvarValue*.</span></span>

</dd> <dt>

<span data-ttu-id="f0d63-112">*pPropBag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0d63-112">*pPropBag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0d63-113">[**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop)結構陣列的指標，指定要儲存的屬性。</span><span class="sxs-lookup"><span data-stu-id="f0d63-113">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that specifies the properties to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="f0d63-114">*pvarValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f0d63-114">*pvarValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0d63-115">VARIANT 的指標，該 **變數** 的類型取決於它所包含之屬性資訊的資料類型。</span><span class="sxs-lookup"><span data-stu-id="f0d63-115">Pointer to a **VARIANT** whose type depends on the data type of the property information that it contains.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0d63-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="f0d63-116">Return value</span></span>

<span data-ttu-id="f0d63-117">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="f0d63-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="f0d63-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f0d63-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0d63-119">備註</span><span class="sxs-lookup"><span data-stu-id="f0d63-119">Remarks</span></span>

<span data-ttu-id="f0d63-120">只有在 Windows XP 和 Windows Server 2003 上才支援 [**IItemPropertyBag**](iitempropertybag.md) 介面，且不應再使用。</span><span class="sxs-lookup"><span data-stu-id="f0d63-120">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="f0d63-121">若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 [**IItemPropertyBag**](iitempropertybag.md) 介面和下列 Api： [**ISearchProtocolUI**](-search-isearchprotocolui.md)、 [**IItemPreviewerExt**](-search-iitempreviewerext.md) 和 [**ISearchItem**](-search-isearchitem.md) 介面、 [**LINKINFO**](-search-linkinfo.md) 和 [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) 結構，以及 [**LINKTYPE**](-search-linktype.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="f0d63-121">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0d63-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0d63-122">Requirements</span></span>



| <span data-ttu-id="f0d63-123">需求</span><span class="sxs-lookup"><span data-stu-id="f0d63-123">Requirement</span></span> | <span data-ttu-id="f0d63-124">值</span><span class="sxs-lookup"><span data-stu-id="f0d63-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f0d63-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0d63-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f0d63-126">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0d63-126">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f0d63-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0d63-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f0d63-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0d63-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f0d63-129">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="f0d63-129">Redistributable</span></span><br/>          | <span data-ttu-id="f0d63-130">Windows 桌面搜尋 (WDS) 3。0</span><span class="sxs-lookup"><span data-stu-id="f0d63-130">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="f0d63-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0d63-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0d63-132">**IItemPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="f0d63-132">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 




