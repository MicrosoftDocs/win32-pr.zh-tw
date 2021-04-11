---
description: 取得可能隨附于 Windows 映像取得的擴充介面 (WIA) 2.0 設備磁碟機。
ms.assetid: 70f20f33-905c-4a88-8065-1cf876e98302
title: 'IWiaItem2：： GetExtension 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2fea4c4b9a2dd909b7ec49097ee94664b47f7e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026247"
---
# <a name="iwiaitem2getextension-method"></a><span data-ttu-id="745a1-103">IWiaItem2：： GetExtension 方法</span><span class="sxs-lookup"><span data-stu-id="745a1-103">IWiaItem2::GetExtension method</span></span>

<span data-ttu-id="745a1-104">取得可能隨附于 Windows 映像取得的擴充介面 (WIA) 2.0 設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="745a1-104">Gets the extension interfaces that might come with a Windows Image Acquisition (WIA) 2.0 device driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="745a1-105">語法</span><span class="sxs-lookup"><span data-stu-id="745a1-105">Syntax</span></span>


```C++
HRESULT GetExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] VOID   **ppOut
);
```



## <a name="parameters"></a><span data-ttu-id="745a1-106">參數</span><span class="sxs-lookup"><span data-stu-id="745a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="745a1-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="745a1-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="745a1-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="745a1-108">Type: **LONG**</span></span>

<span data-ttu-id="745a1-109">目前未使用。</span><span class="sxs-lookup"><span data-stu-id="745a1-109">Currently unused.</span></span> <span data-ttu-id="745a1-110">應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="745a1-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="745a1-111">*bstrName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="745a1-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="745a1-112">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="745a1-112">Type: **BSTR**</span></span>

<span data-ttu-id="745a1-113">指定呼叫應用程式要求指標的延伸模組名稱。</span><span class="sxs-lookup"><span data-stu-id="745a1-113">Specifies the name of the extension that the calling application requires a pointer to.</span></span>

<dt>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>

<span data-ttu-id="745a1-114"><span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**SegmentationFilter**</span><span class="sxs-lookup"><span data-stu-id="745a1-114"><span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**SegmentationFilter**</span></span>


</dt> <dd>

<span data-ttu-id="745a1-115">分割篩選延伸。</span><span class="sxs-lookup"><span data-stu-id="745a1-115">The segmentation filter extension.</span></span> <span data-ttu-id="745a1-116">這是此參數目前唯一有效的值。</span><span class="sxs-lookup"><span data-stu-id="745a1-116">This is currently the only valid value for this parameter.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="745a1-117">*riidExtensionInterface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="745a1-117">*riidExtensionInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="745a1-118">類型： **REFIID**</span><span class="sxs-lookup"><span data-stu-id="745a1-118">Type: **REFIID**</span></span>

<span data-ttu-id="745a1-119">指定延伸模組介面的識別碼。</span><span class="sxs-lookup"><span data-stu-id="745a1-119">Specifies the identifier of the extension interface.</span></span>

</dd> <dt>

<span data-ttu-id="745a1-120">*ppOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="745a1-120">*ppOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="745a1-121">類型： **VOID \* \***</span><span class="sxs-lookup"><span data-stu-id="745a1-121">Type: **VOID\*\***</span></span>

<span data-ttu-id="745a1-122">接收擴充介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="745a1-122">Receives the address of a pointer to the extension interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="745a1-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="745a1-123">Return value</span></span>

<span data-ttu-id="745a1-124">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="745a1-124">Type: **HRESULT**</span></span>

<span data-ttu-id="745a1-125">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="745a1-125">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="745a1-126">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="745a1-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="745a1-127">備註</span><span class="sxs-lookup"><span data-stu-id="745a1-127">Remarks</span></span>

<span data-ttu-id="745a1-128">應用程式會叫用這個方法，以建立擴充物件來執行其中一個 WIA 2.0 驅動程式擴充功能介面。</span><span class="sxs-lookup"><span data-stu-id="745a1-128">An application invokes this method to create an extension object implementing one of the WIA 2.0 driver extension interfaces.</span></span> <span data-ttu-id="745a1-129">**IWiaItem2：： GetExtension** 會在 *riidExtensionInterface* 參數中儲存擴充物件的擴充功能介面位址。</span><span class="sxs-lookup"><span data-stu-id="745a1-129">**IWiaItem2::GetExtension** stores the address of the extension object's extension interface in the *riidExtensionInterface* parameter.</span></span> <span data-ttu-id="745a1-130">然後，應用程式會使用介面指標來呼叫其方法。</span><span class="sxs-lookup"><span data-stu-id="745a1-130">The application then uses the interface pointer to call its methods.</span></span>

<span data-ttu-id="745a1-131">應用程式必須在透過 *riidExtensionInterface* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。</span><span class="sxs-lookup"><span data-stu-id="745a1-131">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *riidExtensionInterface* parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="745a1-132">範例</span><span class="sxs-lookup"><span data-stu-id="745a1-132">Examples</span></span>

<span data-ttu-id="745a1-133">CreateSegmentationFilter 會在傳入的 [**IWiaItem2**](-wia-iwiaitem2.md)介面上呼叫 **IWiaItem2：： GetExtension** ，以建立驅動程式分割篩選的實例 ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)) 。</span><span class="sxs-lookup"><span data-stu-id="745a1-133">CreateSegmentationFilter creates an instance of the driver's segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)) by calling **IWiaItem2::GetExtension** on the passed-in [**IWiaItem2**](-wia-iwiaitem2.md) interface.</span></span>


```C++
HRESULT
CreateSegmentationFilter(
   IWiaItem2               *pWiaItem2,
   IWiaSegmentationFilter  **ppSegmentationFilter)
{
   HRESULT                 hr         = S_OK;
   IWiaSegmentationFilter *pSegFilter = NULL;
    
   if (!pWiaItem2 || !ppSegmentationFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_SEGMENTATION_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->GetExtension(0,
                                      bstrFilterString,
                                      IID_IWiaSegmentationFilter,
                                      (void**)&pSegFilter);
         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   if (SUCCEEDED(hr))
   {
     *ppSegmentationFilter = pSegFilter;
      pSegFilter = NULL;
   }
   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="745a1-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="745a1-134">Requirements</span></span>



| <span data-ttu-id="745a1-135">需求</span><span class="sxs-lookup"><span data-stu-id="745a1-135">Requirement</span></span> | <span data-ttu-id="745a1-136">值</span><span class="sxs-lookup"><span data-stu-id="745a1-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="745a1-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="745a1-137">Minimum supported client</span></span><br/> | <span data-ttu-id="745a1-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="745a1-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="745a1-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="745a1-139">Minimum supported server</span></span><br/> | <span data-ttu-id="745a1-140">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="745a1-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="745a1-141">標頭</span><span class="sxs-lookup"><span data-stu-id="745a1-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="745a1-142"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="745a1-142"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="745a1-143">Idl</span><span class="sxs-lookup"><span data-stu-id="745a1-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="745a1-144"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="745a1-144"><dt>Wia.idl</dt></span></span> </dl> |



 

 
