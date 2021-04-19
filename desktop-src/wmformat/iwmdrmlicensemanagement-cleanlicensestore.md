---
title: 'IWMDRMLicenseManagement CleanLicenseStore 方法 (Wmdrmsdk .h) '
description: CleanLicenseStore 方法會從暫時授權存放區中移除無法使用的授權，並重組本機授權存放區以改善效能。
ms.assetid: 07ddd6f8-a091-4c18-81d3-c4d0c6026b6b
keywords:
- CleanLicenseStore 方法 windows Media 格式
- CleanLicenseStore 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，CleanLicenseStore 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CleanLicenseStore
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9327fd836cf742f5495c29767be93d914c0f187
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989721"
---
# <a name="iwmdrmlicensemanagementcleanlicensestore-method"></a><span data-ttu-id="c86e5-106">IWMDRMLicenseManagement：： CleanLicenseStore 方法</span><span class="sxs-lookup"><span data-stu-id="c86e5-106">IWMDRMLicenseManagement::CleanLicenseStore method</span></span>

<span data-ttu-id="c86e5-107">**CleanLicenseStore** 方法會從暫時授權存放區中移除無法使用的授權，並重組本機授權存放區以改善效能。</span><span class="sxs-lookup"><span data-stu-id="c86e5-107">The **CleanLicenseStore** method removes unusable licenses from the temporary license store and defragments the local license store to improve performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="c86e5-108">語法</span><span class="sxs-lookup"><span data-stu-id="c86e5-108">Syntax</span></span>


```C++
HRESULT CleanLicenseStore(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="c86e5-109">參數</span><span class="sxs-lookup"><span data-stu-id="c86e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c86e5-110">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c86e5-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c86e5-111">旗標，指定要使用的授權存放清除選項。</span><span class="sxs-lookup"><span data-stu-id="c86e5-111">Flags specifying the license store cleaning options to use.</span></span> <span data-ttu-id="c86e5-112">設定為下表中的其中一個常數。</span><span class="sxs-lookup"><span data-stu-id="c86e5-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="c86e5-113">常數</span><span class="sxs-lookup"><span data-stu-id="c86e5-113">Constant</span></span>                            | <span data-ttu-id="c86e5-114">描述</span><span class="sxs-lookup"><span data-stu-id="c86e5-114">Description</span></span>                                                                                                                                                                    |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c86e5-115">WMDRM \_ CLEAN \_ LICENSE \_ STORE \_ 同步處理</span><span class="sxs-lookup"><span data-stu-id="c86e5-115">WMDRM\_CLEAN\_LICENSE\_STORE\_SYNC</span></span>  | <span data-ttu-id="c86e5-116">清除作業將會同步執行。</span><span class="sxs-lookup"><span data-stu-id="c86e5-116">The clean operation will be performed synchronously.</span></span> <span data-ttu-id="c86e5-117">在作業完成之前，不會傳回這個方法。</span><span class="sxs-lookup"><span data-stu-id="c86e5-117">This method will not return until the operation is complete.</span></span>                                                              |
| <span data-ttu-id="c86e5-118">WMDRM \_ 乾淨 \_ 授權 \_ 商店 \_ ASYNC</span><span class="sxs-lookup"><span data-stu-id="c86e5-118">WMDRM\_CLEAN\_LICENSE\_STORE\_ASYNC</span></span> | <span data-ttu-id="c86e5-119">清除作業將會以非同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="c86e5-119">The clean operation will be performed asynchronously.</span></span> <span data-ttu-id="c86e5-120">這個方法會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="c86e5-120">This method will return immediately.</span></span> <span data-ttu-id="c86e5-121">當作業完成時，將會傳送媒體事件 MELicenseStoreCleaned。</span><span class="sxs-lookup"><span data-stu-id="c86e5-121">When the operation is complete, the media event MELicenseStoreCleaned will be sent.</span></span> |



 

</dd> <dt>

<span data-ttu-id="c86e5-122">*ppunkCancelationCookie* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c86e5-122">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c86e5-123">指標，接收識別此非同步呼叫之物件的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="c86e5-123">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="c86e5-124">這個介面指標可透過呼叫 [**IWMDRMEventGenerator：： CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) 方法，用來取消非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="c86e5-124">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c86e5-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="c86e5-125">Return value</span></span>

<span data-ttu-id="c86e5-126">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="c86e5-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c86e5-127">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="c86e5-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c86e5-128">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c86e5-128">Return code</span></span>                                                                                            | <span data-ttu-id="c86e5-129">Description</span><span class="sxs-lookup"><span data-stu-id="c86e5-129">Description</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c86e5-130"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c86e5-130"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="c86e5-131">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="c86e5-131">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="c86e5-132"><dt>**DRM \_ E \_ LICENSENOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="c86e5-132"><dt>**DRM\_E\_LICENSENOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="c86e5-133">用戶端電腦上沒有暫時性的授權存放區。</span><span class="sxs-lookup"><span data-stu-id="c86e5-133">There is no temporary license store on the client computer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c86e5-134">備註</span><span class="sxs-lookup"><span data-stu-id="c86e5-134">Remarks</span></span>

<span data-ttu-id="c86e5-135">這個方法會以非同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="c86e5-135">This method executes asynchronously.</span></span> <span data-ttu-id="c86e5-136">它會在呼叫後立即傳回，然後在處理完成時產生 **MEWMDRMLicenseStoreCleaned** 事件。</span><span class="sxs-lookup"><span data-stu-id="c86e5-136">It returns immediately after being called and then generates an **MEWMDRMLicenseStoreCleaned** event when processing is complete.</span></span>

<span data-ttu-id="c86e5-137">如需使用 Windows Media DRM 用戶端擴充 Api 的非同步方法的詳細資訊，請參閱 [使用媒體基礎事件模型](using-the-media-foundation-model.md)。</span><span class="sxs-lookup"><span data-stu-id="c86e5-137">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c86e5-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="c86e5-138">Requirements</span></span>



| <span data-ttu-id="c86e5-139">需求</span><span class="sxs-lookup"><span data-stu-id="c86e5-139">Requirement</span></span> | <span data-ttu-id="c86e5-140">值</span><span class="sxs-lookup"><span data-stu-id="c86e5-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c86e5-141">標頭</span><span class="sxs-lookup"><span data-stu-id="c86e5-141">Header</span></span><br/>  | <dl> <span data-ttu-id="c86e5-142"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="c86e5-142"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="c86e5-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="c86e5-143">Library</span></span><br/> | <dl> <span data-ttu-id="c86e5-144"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c86e5-144"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c86e5-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c86e5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c86e5-146">**IWMDRMLicenseManagement 介面**</span><span class="sxs-lookup"><span data-stu-id="c86e5-146">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





