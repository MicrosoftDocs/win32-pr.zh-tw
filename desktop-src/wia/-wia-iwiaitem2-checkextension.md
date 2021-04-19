---
description: 檢查指定的延伸模組是否可在電腦上使用，並可供 IWiaItem2：： GetExtension 方法使用。
ms.assetid: 672f6418-4ce3-4570-a412-fe639c9f5eb8
title: 'IWiaItem2：： CheckExtension 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CheckExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 65b0b5b3ace1634a20dfa63382d82099fef0686e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974137"
---
# <a name="iwiaitem2checkextension-method"></a><span data-ttu-id="4a610-103">IWiaItem2：： CheckExtension 方法</span><span class="sxs-lookup"><span data-stu-id="4a610-103">IWiaItem2::CheckExtension method</span></span>

<span data-ttu-id="4a610-104">檢查指定的延伸模組是否可在電腦上使用，並可供 [**IWiaItem2：： GetExtension**](-wia-iwiaitem2-getextension.md) 方法使用。</span><span class="sxs-lookup"><span data-stu-id="4a610-104">Checks whether a specified extension is available on the machine and can be used by the [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a610-105">語法</span><span class="sxs-lookup"><span data-stu-id="4a610-105">Syntax</span></span>


```C++
HRESULT CheckExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] BOOL   *pbExtensionExists
);
```



## <a name="parameters"></a><span data-ttu-id="4a610-106">參數</span><span class="sxs-lookup"><span data-stu-id="4a610-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a610-107">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4a610-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a610-108">類型： **LONG**</span><span class="sxs-lookup"><span data-stu-id="4a610-108">Type: **LONG**</span></span>

<span data-ttu-id="4a610-109">目前未使用。</span><span class="sxs-lookup"><span data-stu-id="4a610-109">Currently unused.</span></span> <span data-ttu-id="4a610-110">應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="4a610-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="4a610-111">*bstrName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4a610-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a610-112">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="4a610-112">Type: **BSTR**</span></span>

<span data-ttu-id="4a610-113">指定擴充功能的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a610-113">Specifies the name of the extension.</span></span>

</dd> <dt>

<span data-ttu-id="4a610-114">*riidExtensionInterface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4a610-114">*riidExtensionInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a610-115">類型： **REFIID**</span><span class="sxs-lookup"><span data-stu-id="4a610-115">Type: **REFIID**</span></span>

<span data-ttu-id="4a610-116">目前未使用。</span><span class="sxs-lookup"><span data-stu-id="4a610-116">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="4a610-117">*pbExtensionExists* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4a610-117">*pbExtensionExists* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a610-118">類型： \**BOOL \** _</span><span class="sxs-lookup"><span data-stu-id="4a610-118">Type: \**BOOL\** _</span></span>

<span data-ttu-id="4a610-119">接收 _ \* BOOL \* \* 的指標。</span><span class="sxs-lookup"><span data-stu-id="4a610-119">Receives a pointer to a _\*BOOL\*\*.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="4a610-120"><span id="FALSE"></span><span id="false"></span>**假**</span><span class="sxs-lookup"><span data-stu-id="4a610-120"><span id="FALSE"></span><span id="false"></span>**FALSE**</span></span>


</dt> <dd>

<span data-ttu-id="4a610-121">無法使用指定的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="4a610-121">The specified extension is not available.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="4a610-122"><span id="TRUE"></span><span id="true"></span>**真**</span><span class="sxs-lookup"><span data-stu-id="4a610-122"><span id="TRUE"></span><span id="true"></span>**TRUE**</span></span>


</dt> <dd>

<span data-ttu-id="4a610-123">指定的擴充功能可供使用。</span><span class="sxs-lookup"><span data-stu-id="4a610-123">The specified extension is available.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a610-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a610-124">Return value</span></span>

<span data-ttu-id="4a610-125">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4a610-125">Type: **HRESULT**</span></span>

<span data-ttu-id="4a610-126">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4a610-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4a610-127">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4a610-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a610-128">備註</span><span class="sxs-lookup"><span data-stu-id="4a610-128">Remarks</span></span>

<span data-ttu-id="4a610-129">使用這個方法，應用程式可以在呼叫 [**IWiaItem2：： GetExtension**](-wia-iwiaitem2-getextension.md) 方法之前，檢查是否有可用的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="4a610-129">Using this method, applications can check whether an extension is available before calling the [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) method.</span></span> <span data-ttu-id="4a610-130">此外，應用程式也可以檢查有哪些延伸模組可供使用，而不需要共同建立每個擴充功能，然後決定要使用哪一個。</span><span class="sxs-lookup"><span data-stu-id="4a610-130">Also, the application can check which extensions are available without co-creating each of them, and then decide which one to use.</span></span>

## <a name="examples"></a><span data-ttu-id="4a610-131">範例</span><span class="sxs-lookup"><span data-stu-id="4a610-131">Examples</span></span>

<span data-ttu-id="4a610-132">CheckImgFilter 會檢查驅動程式是否有影像處理篩選。</span><span class="sxs-lookup"><span data-stu-id="4a610-132">CheckImgFilter checks if the driver has an image processing filter.</span></span> <span data-ttu-id="4a610-133">在呼叫預覽元件之前，應用程式應該確定驅動程式具有影像處理篩選。</span><span class="sxs-lookup"><span data-stu-id="4a610-133">Before calling into the preview component, an application should ensure that the driver has an image processing filter.</span></span>


```C++
HRESULT
CheckImgFilter(
   IN  IWiaItem2 *pWiaItem2,
   OUT BOOL      *pbHasImgFilter)
{
   HRESULT     hr = S_OK;

   if (!pWiaItem2 || !pbHasImgFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
     *pbHasImgFilter = FALSE;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_IMAGEPROC_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->CheckExtension(0,
                                        bstrFilterString,
                                        IID_IWiaSegmentationFilter,
                                        pbHasImgFilter);

         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   return hr;

}
```



## <a name="requirements"></a><span data-ttu-id="4a610-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a610-134">Requirements</span></span>



| <span data-ttu-id="4a610-135">需求</span><span class="sxs-lookup"><span data-stu-id="4a610-135">Requirement</span></span> | <span data-ttu-id="4a610-136">值</span><span class="sxs-lookup"><span data-stu-id="4a610-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4a610-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a610-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4a610-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a610-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4a610-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a610-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4a610-140">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a610-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4a610-141">標頭</span><span class="sxs-lookup"><span data-stu-id="4a610-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a610-142"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="4a610-142"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a610-143">Idl</span><span class="sxs-lookup"><span data-stu-id="4a610-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4a610-144"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="4a610-144"><dt>Wia.idl</dt></span></span> </dl> |



 

 




