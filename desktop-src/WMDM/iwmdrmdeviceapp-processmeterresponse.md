---
title: 'IWMDRMDeviceApp ProcessMeterResponse 方法 (WMDRMDeviceApp .h) '
description: ProcessMeterResponse 方法會重設裝置上的部分或所有計量計數，之後裝置的資料就會由伺服器傳送和處理。
ms.assetid: bafc4bb2-aa3c-4b2a-a818-1a78577cefc5
keywords:
- ProcessMeterResponse 方法 windows Media 裝置管理員
- ProcessMeterResponse 方法 windows Media 裝置管理員，IWMDRMDeviceApp 介面
- IWMDRMDeviceApp interface windows Media 裝置管理員，ProcessMeterResponse 方法
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.ProcessMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b57312dc2f401207e41f38f5bf75cddf69a13b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998809"
---
# <a name="iwmdrmdeviceappprocessmeterresponse-method"></a><span data-ttu-id="0255f-106">IWMDRMDeviceApp：:P rocessMeterResponse 方法</span><span class="sxs-lookup"><span data-stu-id="0255f-106">IWMDRMDeviceApp::ProcessMeterResponse method</span></span>

<span data-ttu-id="0255f-107">**ProcessMeterResponse** 方法會重設裝置上的部分或所有計量計數，之後裝置的資料就會由伺服器傳送和處理。</span><span class="sxs-lookup"><span data-stu-id="0255f-107">The **ProcessMeterResponse** method resets some or all of the metering counts on a device, after data from the device has been sent to and processed by the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="0255f-108">語法</span><span class="sxs-lookup"><span data-stu-id="0255f-108">Syntax</span></span>


```C++
HRESULT ProcessMeterResponse(
  [in]  IWMDMDevice *pDevice,
  [in]  BYTE        *pbResponse,
  [in]  DWORD       cbResponse,
  [out] DWORD       *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="0255f-109">參數</span><span class="sxs-lookup"><span data-stu-id="0255f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0255f-110">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0255f-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0255f-111">[**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="0255f-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="0255f-112">*pbResponse* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0255f-112">*pbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0255f-113">傳送使用 [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md)產生的資料之後，從計量伺服器收到的回應。</span><span class="sxs-lookup"><span data-stu-id="0255f-113">Response received from a metering server, after sending data generated using [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).</span></span>

</dd> <dt>

<span data-ttu-id="0255f-114">*cbResponse* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0255f-114">*cbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0255f-115">*PbResponse* 的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0255f-115">Size of *pbResponse*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0255f-116">*pdwFlags* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0255f-116">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0255f-117">下表中的 **DWORD** ，指出裝置上是否有更多需要處理的計量資料。</span><span class="sxs-lookup"><span data-stu-id="0255f-117">A **DWORD** from the following table indicating whether there is more metering data on the device that needs to be processed.</span></span>



| <span data-ttu-id="0255f-118">旗標</span><span class="sxs-lookup"><span data-stu-id="0255f-118">Flag</span></span>                            | <span data-ttu-id="0255f-119">描述</span><span class="sxs-lookup"><span data-stu-id="0255f-119">Description</span></span>                                     |
|---------------------------------|-------------------------------------------------|
| <span data-ttu-id="0255f-120">WMDRM \_ 計量 \_ 回應 \_ 全部</span><span class="sxs-lookup"><span data-stu-id="0255f-120">WMDRM\_METER\_RESPONSE\_ALL</span></span>     | <span data-ttu-id="0255f-121">已處理所有計量資料。</span><span class="sxs-lookup"><span data-stu-id="0255f-121">All metering data has been processed.</span></span>           |
| <span data-ttu-id="0255f-122">WMDRM \_ 計量 \_ 回應 \_ 部分</span><span class="sxs-lookup"><span data-stu-id="0255f-122">WMDRM\_METER\_RESPONSE\_PARTIAL</span></span> | <span data-ttu-id="0255f-123">需要處理額外的計量資料。</span><span class="sxs-lookup"><span data-stu-id="0255f-123">Additional metering data needs to be processed.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0255f-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="0255f-124">Return value</span></span>

<span data-ttu-id="0255f-125">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="0255f-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0255f-126">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="0255f-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0255f-127">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0255f-127">Return code</span></span>                                                                                                      | <span data-ttu-id="0255f-128">Description</span><span class="sxs-lookup"><span data-stu-id="0255f-128">Description</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0255f-129"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0255f-129"><dt>**S\_OK**</dt></span></span> </dl>                             | <span data-ttu-id="0255f-130">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="0255f-130">The method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="0255f-131"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0255f-131"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="0255f-132">一或多個引數無效。</span><span class="sxs-lookup"><span data-stu-id="0255f-132">One or more arguments are not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="0255f-133"><dt>**裝置的錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="0255f-133"><dt>**Errors from the device**</dt></span></span> </dl>            | <span data-ttu-id="0255f-134">有許多裝置錯誤。</span><span class="sxs-lookup"><span data-stu-id="0255f-134">Any of a number of device errors.</span></span><br/>                                  |
| <dl> <span data-ttu-id="0255f-135"><dt>**DRM 用戶端的錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="0255f-135"><dt>**Errors from the DRM Client**</dt></span></span> </dl>        | <span data-ttu-id="0255f-136">許多內部 DRM 用戶端錯誤。</span><span class="sxs-lookup"><span data-stu-id="0255f-136">Any of a number of internal DRM client errors.</span></span><br/>                     |
| <dl> <span data-ttu-id="0255f-137"><dt>**NS \_ E \_ 裝置 \_ 不是 \_ WMDRM \_ 裝置**</dt></span><span class="sxs-lookup"><span data-stu-id="0255f-137"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl> | <span data-ttu-id="0255f-138">指定的裝置不是 Windows Media DRM 相容裝置。</span><span class="sxs-lookup"><span data-stu-id="0255f-138">The specified device is not a Windows Media DRM compatible device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0255f-139">備註</span><span class="sxs-lookup"><span data-stu-id="0255f-139">Remarks</span></span>

<span data-ttu-id="0255f-140">如需有關計量的詳細資訊（包括程式碼範例），請參閱 MSDN 網站上的 [使用 Windows MEDIA DRM 10 的數位媒體內容的計量](/previous-versions//bb614723(v=vs.85)) 技術白皮書。</span><span class="sxs-lookup"><span data-stu-id="0255f-140">More information on metering, including code examples, can be found in the whitepaper [Metering the Use of Digital Media Content with Windows Media DRM 10](/previous-versions//bb614723(v=vs.85)) on the MSDN Web site.</span></span>

## <a name="requirements"></a><span data-ttu-id="0255f-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="0255f-141">Requirements</span></span>



| <span data-ttu-id="0255f-142">需求</span><span class="sxs-lookup"><span data-stu-id="0255f-142">Requirement</span></span> | <span data-ttu-id="0255f-143">值</span><span class="sxs-lookup"><span data-stu-id="0255f-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0255f-144">標頭</span><span class="sxs-lookup"><span data-stu-id="0255f-144">Header</span></span><br/>  | <dl> <span data-ttu-id="0255f-145"><dt>WMDRMDeviceApp (也需要 Wmdrmdeviceapp \_ WMDRMDeviceApp，它是由 .idl 所建立) </dt></span><span class="sxs-lookup"><span data-stu-id="0255f-145"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="0255f-146">程式庫</span><span class="sxs-lookup"><span data-stu-id="0255f-146">Library</span></span><br/> | <dl> <span data-ttu-id="0255f-147"><dt>Mssachlp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0255f-147"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="0255f-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0255f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0255f-149">**處理應用程式中受保護的內容**</span><span class="sxs-lookup"><span data-stu-id="0255f-149">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="0255f-150">**IWMDMDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="0255f-150">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="0255f-151">**IWMDRMDeviceApp 介面**</span><span class="sxs-lookup"><span data-stu-id="0255f-151">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

