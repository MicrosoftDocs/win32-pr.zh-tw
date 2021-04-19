---
title: 'IWMDRMLicenseManagement AcquireLicense 方法 (Wmdrmsdk .h) '
description: AcquireLicense 方法會以非同步方式從指定的 URL 取得授權。
ms.assetid: 2e134f39-1f45-4d3a-b7c7-460aa0a250d0
keywords:
- AcquireLicense 方法 windows Media 格式
- AcquireLicense 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，AcquireLicense 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.AcquireLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 279a3d4d84617c4a4fa5454d1f39f6f78f0cf3fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979424"
---
# <a name="iwmdrmlicensemanagementacquirelicense-method"></a><span data-ttu-id="f1457-106">IWMDRMLicenseManagement：： AcquireLicense 方法</span><span class="sxs-lookup"><span data-stu-id="f1457-106">IWMDRMLicenseManagement::AcquireLicense method</span></span>

<span data-ttu-id="f1457-107">**AcquireLicense** 方法會以非同步方式從指定的 URL 取得授權。</span><span class="sxs-lookup"><span data-stu-id="f1457-107">The **AcquireLicense** method asynchronously acquires a license from a specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1457-108">語法</span><span class="sxs-lookup"><span data-stu-id="f1457-108">Syntax</span></span>


```C++
HRESULT AcquireLicense(
  [in]  BSTR     bstrURL,
  [in]  BSTR     bstrHeaderData,
  [in]  BSTR     bstrActions,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="f1457-109">參數</span><span class="sxs-lookup"><span data-stu-id="f1457-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1457-110">*bstrURL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1457-110">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1457-111">取得授權之授權伺服器的 URL。</span><span class="sxs-lookup"><span data-stu-id="f1457-111">URL of the license server from which to acquire the license.</span></span> <span data-ttu-id="f1457-112">傳遞 **Null** 可讓方法剖析內容標頭中的 URL。</span><span class="sxs-lookup"><span data-stu-id="f1457-112">Pass **NULL** to have the method parse the URL from the content header.</span></span>

</dd> <dt>

<span data-ttu-id="f1457-113">*bstrHeaderData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1457-113">*bstrHeaderData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1457-114">要傳遞至授權伺服器的內容標頭。</span><span class="sxs-lookup"><span data-stu-id="f1457-114">Content header to be passed to the license server.</span></span> <span data-ttu-id="f1457-115">如果 *bstrURL* 為 **Null**，方法將會剖析此標頭中的 URL。</span><span class="sxs-lookup"><span data-stu-id="f1457-115">If *bstrURL* is **NULL**, the method will parse the URL from this header.</span></span> <span data-ttu-id="f1457-116">如果 *dwFlags* 設定為 [WMDRM \_ 取得 \_ 授權 \_ 舊版 \_ NONSILENT]，請將此值設定為金鑰識別碼，而不是整個內容標頭。</span><span class="sxs-lookup"><span data-stu-id="f1457-116">If *dwFlags* is set to WMDRM\_ACQUIRE\_LICENSE\_LEGACY\_NONSILENT, set this value to the key ID instead of the entire content header.</span></span>

</dd> <dt>

<span data-ttu-id="f1457-117">*bstrActions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1457-117">*bstrActions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1457-118">字串，包含要在授權中要求許可權的零或多個動作。</span><span class="sxs-lookup"><span data-stu-id="f1457-118">String containing zero or more actions for which to request permission in the license.</span></span> <span data-ttu-id="f1457-119">字串的格式必須如下：</span><span class="sxs-lookup"><span data-stu-id="f1457-119">The string must be formatted as follows:</span></span>

-   <span data-ttu-id="f1457-120">每個動作都必須定義于 ACTION 元素內。</span><span class="sxs-lookup"><span data-stu-id="f1457-120">Each action must be defined within an ACTION element.</span></span> <span data-ttu-id="f1457-121">元素的資料是動作字串。</span><span class="sxs-lookup"><span data-stu-id="f1457-121">The data of the element is the action string.</span></span>
-   <span data-ttu-id="f1457-122">所有動作元素都必須包含在時元素內。</span><span class="sxs-lookup"><span data-stu-id="f1457-122">All ACTION elements must be contained within an ACTIONLIST element.</span></span>

    <span data-ttu-id="f1457-123">例如，要求授權來播放內容的字串格式如下：</span><span class="sxs-lookup"><span data-stu-id="f1457-123">For example, the string to request a license to play content is formatted like this:</span></span>

    ```C++
    <ACTIONLIST><ACTION></ACTION></ACTIONLIST>
    ```

    

</dd> <dt>

<span data-ttu-id="f1457-124">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1457-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1457-125">授權取得選項旗標。</span><span class="sxs-lookup"><span data-stu-id="f1457-125">License acquisition option flags.</span></span> <span data-ttu-id="f1457-126">設定為下表中的其中一個常數。</span><span class="sxs-lookup"><span data-stu-id="f1457-126">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="f1457-127">常數</span><span class="sxs-lookup"><span data-stu-id="f1457-127">Constant</span></span>                                   | <span data-ttu-id="f1457-128">描述</span><span class="sxs-lookup"><span data-stu-id="f1457-128">Description</span></span>                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1457-129">WMDRM \_ 取得 \_ 授權 \_ 無訊息</span><span class="sxs-lookup"><span data-stu-id="f1457-129">WMDRM\_ACQUIRE\_LICENSE\_SILENT</span></span>            | <span data-ttu-id="f1457-130">系統會直接透過網際網路發出授權，而不會向用戶端應用程式進行任何確認。</span><span class="sxs-lookup"><span data-stu-id="f1457-130">The license will be issued directly over the Internet without any confirmation from the client application.</span></span>              |
| <span data-ttu-id="f1457-131">WMDRM \_ 取得 \_ 授權 \_ NONSILENT</span><span class="sxs-lookup"><span data-stu-id="f1457-131">WMDRM\_ACQUIRE\_LICENSE\_NONSILENT</span></span>         | <span data-ttu-id="f1457-132">DRM 子系統會建立授權要求，並以非同步方式傳回以張貼至授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="f1457-132">The DRM subsystem will create a license request which will be returned asynchronously for posting to the license server.</span></span> |
| <span data-ttu-id="f1457-133">WMDRM \_ 取得 \_ 授權 \_ 舊版 \_ NONSILENT</span><span class="sxs-lookup"><span data-stu-id="f1457-133">WMDRM\_ACQUIRE\_LICENSE\_LEGACY\_NONSILENT</span></span> | <span data-ttu-id="f1457-134">與 WMDRM \_ 取得 \_ 授權 NONSILENT 相同 \_ ，不同之處在于將會建立 DRM 版本1授權挑戰。</span><span class="sxs-lookup"><span data-stu-id="f1457-134">The same as WMDRM\_ACQUIRE\_LICENSE\_NONSILENT, except that a DRM version 1 license challenge will be created.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="f1457-135">*ppunkCancelationCookie* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f1457-135">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1457-136">指標，接收識別此非同步呼叫之物件的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="f1457-136">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="f1457-137">這個介面指標可透過呼叫 [**IWMDRMEventGenerator：： CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) 方法，用來取消非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="f1457-137">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1457-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1457-138">Return value</span></span>

<span data-ttu-id="f1457-139">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="f1457-139">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f1457-140">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="f1457-140">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f1457-141">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f1457-141">Return code</span></span>                                                                          | <span data-ttu-id="f1457-142">Description</span><span class="sxs-lookup"><span data-stu-id="f1457-142">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f1457-143"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f1457-143"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f1457-144">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="f1457-144">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f1457-145">備註</span><span class="sxs-lookup"><span data-stu-id="f1457-145">Remarks</span></span>

<span data-ttu-id="f1457-146">這個方法會以非同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="f1457-146">This method executes asynchronously.</span></span> <span data-ttu-id="f1457-147">它會在呼叫後立即傳回，然後在處理完成時產生 **MEWMDRMLicenseAcquisitionCompleted** 事件。</span><span class="sxs-lookup"><span data-stu-id="f1457-147">It returns immediately after being called and then generates an **MEWMDRMLicenseAcquisitionCompleted** event when processing is complete.</span></span> <span data-ttu-id="f1457-148">針對非無訊息授權取得作業，藉由呼叫 **IMFMediaEvent：： GetValue** 取得的事件值是 **IUnknown** 指標。</span><span class="sxs-lookup"><span data-stu-id="f1457-148">For non-silent license acquisition operations, the value of the event obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="f1457-149">您可以呼叫所抓取 **IUnknown** 介面的 **QueryInterface** 方法，以取得 [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md)介面的實例。</span><span class="sxs-lookup"><span data-stu-id="f1457-149">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) interface.</span></span>

<span data-ttu-id="f1457-150">如需使用 Windows Media DRM 用戶端擴充 Api 的非同步方法的詳細資訊，請參閱 [使用媒體基礎事件模型](using-the-media-foundation-model.md)。</span><span class="sxs-lookup"><span data-stu-id="f1457-150">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1457-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1457-151">Requirements</span></span>



| <span data-ttu-id="f1457-152">需求</span><span class="sxs-lookup"><span data-stu-id="f1457-152">Requirement</span></span> | <span data-ttu-id="f1457-153">值</span><span class="sxs-lookup"><span data-stu-id="f1457-153">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1457-154">標頭</span><span class="sxs-lookup"><span data-stu-id="f1457-154">Header</span></span><br/>  | <dl> <span data-ttu-id="f1457-155"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="f1457-155"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="f1457-156">程式庫</span><span class="sxs-lookup"><span data-stu-id="f1457-156">Library</span></span><br/> | <dl> <span data-ttu-id="f1457-157"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1457-157"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1457-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1457-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1457-159">**IWMDRMLicenseManagement 介面**</span><span class="sxs-lookup"><span data-stu-id="f1457-159">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> <dt>

[<span data-ttu-id="f1457-160">**無訊息授權取得**</span><span class="sxs-lookup"><span data-stu-id="f1457-160">**Silent License Acquisition**</span></span>](silent-license-acquisition.md)
</dt> </dl>

 

 





