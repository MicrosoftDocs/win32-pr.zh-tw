---
description: 取得讀取或儲存屬性包中的屬性所需的資訊。 只有在 Windows XP 和 Windows Server 2003 上才支援 IItemPropertyBag 介面，且不應再使用。
ms.assetid: 1667b67d-9dd2-48a6-81dd-c8b06834cef0
title: IItemPropertyBag：： GetPropertyInfo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.GetPropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: a64b064c6c6d3708edc353db136fcad599d14adb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991810"
---
# <a name="iitempropertybaggetpropertyinfo-method"></a><span data-ttu-id="846ce-104">IItemPropertyBag：： GetPropertyInfo 方法</span><span class="sxs-lookup"><span data-stu-id="846ce-104">IItemPropertyBag::GetPropertyInfo method</span></span>

<span data-ttu-id="846ce-105">取得讀取或儲存屬性包中的屬性所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="846ce-105">Gets the information required to read or save the properties in the property bag.</span></span> <span data-ttu-id="846ce-106">只有在 Windows XP 和 Windows Server 2003 上才支援 [**IItemPropertyBag**](iitempropertybag.md) 介面，且不應再使用。</span><span class="sxs-lookup"><span data-stu-id="846ce-106">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="846ce-107">語法</span><span class="sxs-lookup"><span data-stu-id="846ce-107">Syntax</span></span>


```C++
HRESULT GetPropertyInfo(
  [in]  ULONG    iProperty,
  [in]  ULONG    cProperties,
  [out] ITEMPROP *pPropBag,
  [out] ULONG    *pcProperties
);
```



## <a name="parameters"></a><span data-ttu-id="846ce-108">參數</span><span class="sxs-lookup"><span data-stu-id="846ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="846ce-109">*iProperty* \[在\]</span><span class="sxs-lookup"><span data-stu-id="846ce-109">*iProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="846ce-110">第一個屬性之以零為起始的索引，其為其所要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="846ce-110">The zero-based index of the first property for which information is requested.</span></span>

</dd> <dt>

<span data-ttu-id="846ce-111">*cProperties* \[在\]</span><span class="sxs-lookup"><span data-stu-id="846ce-111">*cProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="846ce-112">要取得資訊的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="846ce-112">The number of properties to get information for.</span></span> <span data-ttu-id="846ce-113">這個引數會指定 *pPropBag* 中的陣列元素數目。</span><span class="sxs-lookup"><span data-stu-id="846ce-113">This argument specifies the number of array elements in *pPropBag*.</span></span>

</dd> <dt>

<span data-ttu-id="846ce-114">*pPropBag* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="846ce-114">*pPropBag* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="846ce-115">接收屬性資訊之 [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) 結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="846ce-115">Pointer to an array of [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures that receives the information for the properties.</span></span>

</dd> <dt>

<span data-ttu-id="846ce-116">*pcProperties* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="846ce-116">*pcProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="846ce-117">接收 **ULONG** 變數的指標，此變數會接收已抓取資訊的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="846ce-117">Receives a pointer to a **ULONG** variable that receives the number of properties for which information was retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="846ce-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="846ce-118">Return value</span></span>

<span data-ttu-id="846ce-119">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="846ce-119">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="846ce-120">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="846ce-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="846ce-121">備註</span><span class="sxs-lookup"><span data-stu-id="846ce-121">Remarks</span></span>

<span data-ttu-id="846ce-122">只有在 Windows XP 和 Windows Server 2003 上才支援 [**IItemPropertyBag**](iitempropertybag.md) 介面，且不應再使用。</span><span class="sxs-lookup"><span data-stu-id="846ce-122">The [**IItemPropertyBag**](iitempropertybag.md) interface is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="846ce-123">若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 [**IItemPropertyBag**](iitempropertybag.md) 介面和下列 Api： [**ISearchProtocolUI**](-search-isearchprotocolui.md)、 [**IItemPreviewerExt**](-search-iitempreviewerext.md) 和 [**ISearchItem**](-search-isearchitem.md) 介面、 [**LINKINFO**](-search-linkinfo.md) 和 [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) 結構，以及 [**LINKTYPE**](-search-linktype.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="846ce-123">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**IItemPropertyBag**](iitempropertybag.md) interface and the following APIs: the [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPreviewerExt**](-search-iitempreviewerext.md) and [**ISearchItem**](-search-isearchitem.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) and [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) structures, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="846ce-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="846ce-124">Requirements</span></span>



| <span data-ttu-id="846ce-125">需求</span><span class="sxs-lookup"><span data-stu-id="846ce-125">Requirement</span></span> | <span data-ttu-id="846ce-126">值</span><span class="sxs-lookup"><span data-stu-id="846ce-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="846ce-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="846ce-127">Minimum supported client</span></span><br/> | <span data-ttu-id="846ce-128">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="846ce-128">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="846ce-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="846ce-129">Minimum supported server</span></span><br/> | <span data-ttu-id="846ce-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="846ce-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="846ce-131">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="846ce-131">Redistributable</span></span><br/>          | <span data-ttu-id="846ce-132">Windows 桌面搜尋 (WDS) 3。0</span><span class="sxs-lookup"><span data-stu-id="846ce-132">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="846ce-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="846ce-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="846ce-134">**IItemPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="846ce-134">**IItemPropertyBag**</span></span>](iitempropertybag.md)
</dt> </dl>

 

 




