---
description: 叫用驅動程式分割篩選，並將 IWiaPreview：： GetNewPreview 方法快取的未篩選影像傳遞至篩選。
ms.assetid: 4ae817b5-7091-432e-b004-0e53ae14fdb2
title: 'IWiaPreview：:D etectRegions 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 40665d2aae6e1e2dffa4356540afb05d45050492
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191400"
---
# <a name="iwiapreviewdetectregions-method"></a><span data-ttu-id="65de3-103">IWiaPreview：:D etectRegions 方法</span><span class="sxs-lookup"><span data-stu-id="65de3-103">IWiaPreview::DetectRegions method</span></span>

<span data-ttu-id="65de3-104">叫用驅動程式分割篩選，並將 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md) 方法快取的未篩選影像傳遞至篩選。</span><span class="sxs-lookup"><span data-stu-id="65de3-104">Invokes the driver segmentation filter and passes the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method to the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="65de3-105">語法</span><span class="sxs-lookup"><span data-stu-id="65de3-105">Syntax</span></span>


```C++
HRESULT DetectRegions(
  [in] LONG lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="65de3-106">參數</span><span class="sxs-lookup"><span data-stu-id="65de3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65de3-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="65de3-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65de3-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="65de3-108">Type: **LONG**</span></span>

<span data-ttu-id="65de3-109">未使用。</span><span class="sxs-lookup"><span data-stu-id="65de3-109">Not used.</span></span> <span data-ttu-id="65de3-110">設定為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="65de3-110">Set to zero (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65de3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="65de3-111">Return value</span></span>

<span data-ttu-id="65de3-112">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="65de3-112">Type: **HRESULT**</span></span>

<span data-ttu-id="65de3-113">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="65de3-113">This method can return one of these values.</span></span>



| <span data-ttu-id="65de3-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="65de3-114">Return code</span></span>                                                                               | <span data-ttu-id="65de3-115">Description</span><span class="sxs-lookup"><span data-stu-id="65de3-115">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="65de3-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="65de3-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="65de3-117">作業成功。</span><span class="sxs-lookup"><span data-stu-id="65de3-117">The operation is successful.</span></span><br/>              |
| <dl> <span data-ttu-id="65de3-118"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="65de3-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="65de3-119">驅動程式不支援分割。</span><span class="sxs-lookup"><span data-stu-id="65de3-119">The driver does not support segmentation.</span></span><br/> |
| <dl> <span data-ttu-id="65de3-120"><dt>**否則**</dt></span><span class="sxs-lookup"><span data-stu-id="65de3-120"><dt>**otherwise**</dt></span></span> </dl>  | <span data-ttu-id="65de3-121">標準 COM 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="65de3-121">A standard COM error code.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="65de3-122">備註</span><span class="sxs-lookup"><span data-stu-id="65de3-122">Remarks</span></span>

<span data-ttu-id="65de3-123">應用程式必須先呼叫 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md) ，才能呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="65de3-123">An application must call [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) before it calls this function.</span></span>

<span data-ttu-id="65de3-124">當 Windows 映像取得 (WIA) 2.0 Preview 元件呼叫 **IWiaPreview：:D etectregions** 時，它會叫用驅動程式分割篩選，並傳遞先前傳遞給 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md)的 [**IWiaItem2**](-wia-iwiaitem2.md)介面。</span><span class="sxs-lookup"><span data-stu-id="65de3-124">When the Windows Image Acquisition (WIA) 2.0 Preview Component calls **IWiaPreview::DetectRegions**, it invokes the driver segmentation filter and passes the [**IWiaItem2**](-wia-iwiaitem2.md) interface that was previously passed to [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="65de3-125">它也會將內部快取的影像傳遞至篩選。</span><span class="sxs-lookup"><span data-stu-id="65de3-125">It also passes the internally cached image to the filter.</span></span> <span data-ttu-id="65de3-126">分割篩選器會使用快取的影像來建立子範圍。</span><span class="sxs-lookup"><span data-stu-id="65de3-126">The segmentation filter uses the cached image to create the child extents.</span></span>

<span data-ttu-id="65de3-127">如果應用程式在呼叫 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md)之後變更 [**IWiaItem2**](-wia-iwiaitem2.md)介面的任何屬性，則必須先還原原始屬性，應用程式才能呼叫 **IWiaPreview：:D etectregions**。</span><span class="sxs-lookup"><span data-stu-id="65de3-127">If an application changes any properties of the [**IWiaItem2**](-wia-iwiaitem2.md) interface after it calls [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md), then the original properties must be restored before the application calls **IWiaPreview::DetectRegions**.</span></span> <span data-ttu-id="65de3-128">使用 [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) 和 [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) 還原原始屬性。</span><span class="sxs-lookup"><span data-stu-id="65de3-128">Use [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) and [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) to restore the original properties.</span></span>

<span data-ttu-id="65de3-129">**IWiaPreview：:D etectregions** 用來判斷快取影像的「子領域」。</span><span class="sxs-lookup"><span data-stu-id="65de3-129">**IWiaPreview::DetectRegions** is used to determine the "sub-regions" of the cached image.</span></span> <span data-ttu-id="65de3-130">針對每個偵測到的子領域，會在 [**IWiaItem2**](-wia-iwiaitem2.md) 介面下建立新的子 WIA 2.0 專案。</span><span class="sxs-lookup"><span data-stu-id="65de3-130">For each sub-region detected, a new child WIA 2.0 item is created under the [**IWiaItem2**](-wia-iwiaitem2.md) interface.</span></span> <span data-ttu-id="65de3-131">針對每個子專案，分割篩選必須設定下列 WIA 2.0 屬性的值： WIA \_ ip \_ XPOS、wia \_ IP \_ YPOS、WIA \_ ips \_ 範圍和 wia \_ ips \_ YEXTENT。</span><span class="sxs-lookup"><span data-stu-id="65de3-131">For each child item, the segmentation filter must set the values for the following WIA 2.0 properties: WIA\_IPS\_XPOS, WIA\_IPS\_YPOS, WIA\_IPS\_XEXTENT, and WIA\_IPS\_YEXTENT.</span></span> <span data-ttu-id="65de3-132">\_ \_ \_ \_ \_ \_ 如果驅動程式支援消除扭曲，則更高階的篩選會設定其他 wia 2.0 屬性，例如 WIA ip 反扭曲 X 和 wia ip。</span><span class="sxs-lookup"><span data-stu-id="65de3-132">A more advanced filter sets other WIA 2.0 properties, such as WIA\_IPS\_DESKEW\_X and WIA\_IPS\_DESKEW\_Y, if the driver supports de-skewing.</span></span> <span data-ttu-id="65de3-133">WIA \_ ip \_ XPOS、wia \_ IP \_ YPOS、WIA \_ ips \_ 範圍和 wia \_ ips \_ YEXTENT 屬性代表要掃描之區域的周框。</span><span class="sxs-lookup"><span data-stu-id="65de3-133">The WIA\_IPS\_XPOS, WIA\_IPS\_YPOS, WIA\_IPS\_XEXTENT, and WIA\_IPS\_YEXTENT properties represent the bounding rectangle of the area to scan.</span></span>

<span data-ttu-id="65de3-134">驅動程式可能不支援分割。</span><span class="sxs-lookup"><span data-stu-id="65de3-134">The driver might not support segmentation.</span></span> <span data-ttu-id="65de3-135">在呼叫 **IWiaPreview：:D etectregions** 之前，應用程式通常會檢查驅動程式是否支援 WIA \_ ip \_ 分割屬性。</span><span class="sxs-lookup"><span data-stu-id="65de3-135">Before calling **IWiaPreview::DetectRegions**, an application typically checks whether the driver supports the WIA\_IPS\_SEGMENTATION property.</span></span> <span data-ttu-id="65de3-136">如果未執行屬性，則不支援分割，而且 **IWiaPreview：:D etectregions** 失敗，並傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="65de3-136">If the property is not implemented, segmentation is not supported, and **IWiaPreview::DetectRegions** fails and returns E\_NOTIMPL.</span></span>

<span data-ttu-id="65de3-137">應用程式必須清除透過呼叫 **IWiaPreview：:D etectregions** 所建立的子專案。</span><span class="sxs-lookup"><span data-stu-id="65de3-137">The application must clean up the child items that are created by calling **IWiaPreview::DetectRegions**.</span></span> <span data-ttu-id="65de3-138">例如，如果應用程式在相同的專案上對 **IWiaPreview：:D etectregions** 進行額外的呼叫，就必須清除先前的子專案。</span><span class="sxs-lookup"><span data-stu-id="65de3-138">For example, if an application makes an additional call to **IWiaPreview::DetectRegions** on the same item, it must clean up the previous child items.</span></span>

## <a name="requirements"></a><span data-ttu-id="65de3-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="65de3-139">Requirements</span></span>



| <span data-ttu-id="65de3-140">需求</span><span class="sxs-lookup"><span data-stu-id="65de3-140">Requirement</span></span> | <span data-ttu-id="65de3-141">值</span><span class="sxs-lookup"><span data-stu-id="65de3-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="65de3-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65de3-142">Minimum supported client</span></span><br/> | <span data-ttu-id="65de3-143">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65de3-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="65de3-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65de3-144">Minimum supported server</span></span><br/> | <span data-ttu-id="65de3-145">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65de3-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="65de3-146">標頭</span><span class="sxs-lookup"><span data-stu-id="65de3-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="65de3-147"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="65de3-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="65de3-148">Idl</span><span class="sxs-lookup"><span data-stu-id="65de3-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="65de3-149"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="65de3-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 




