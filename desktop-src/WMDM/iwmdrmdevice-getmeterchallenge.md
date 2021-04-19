---
title: IWMDRMDevice GetMeterChallenge 方法
description: GetMeterChallenge 方法會捕獲計量挑戰。
ms.assetid: 4c122886-46bd-4e63-8e7d-5e6132363662
keywords:
- GetMeterChallenge 方法 windows Media 裝置管理員
- GetMeterChallenge 方法 windows Media 裝置管理員，IWMDRMDevice 介面
- IWMDRMDevice interface windows Media 裝置管理員，GetMeterChallenge 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a916afa90d1db310041f9b92be94d3af9154df4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979890"
---
# <a name="iwmdrmdevicegetmeterchallenge-method"></a><span data-ttu-id="bf1a7-106">IWMDRMDevice：： GetMeterChallenge 方法</span><span class="sxs-lookup"><span data-stu-id="bf1a7-106">IWMDRMDevice::GetMeterChallenge method</span></span>

<span data-ttu-id="bf1a7-107">**GetMeterChallenge** 方法會捕獲計量挑戰。</span><span class="sxs-lookup"><span data-stu-id="bf1a7-107">The **GetMeterChallenge** method retrieves the metering challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf1a7-108">語法</span><span class="sxs-lookup"><span data-stu-id="bf1a7-108">Syntax</span></span>


```C++
HRESULT GetMeterChallenge(
  [in]  BSTR  bstrMeterCert,
  [out] BYTE  **ppbMeterChallenge,
  [out] DWORD *pcbMeterChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="bf1a7-109">參數</span><span class="sxs-lookup"><span data-stu-id="bf1a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf1a7-110">*bstrMeterCert* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bf1a7-110">*bstrMeterCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf1a7-111">內容擁有者傳送給主機電腦以收集裝置上相關計量資料的計量憑證</span><span class="sxs-lookup"><span data-stu-id="bf1a7-111">Metering certificate that the content owner sends to the host computer for collecting the associated metering data on the device</span></span>

</dd> <dt>

<span data-ttu-id="bf1a7-112">*ppbMeterChallenge* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bf1a7-112">*ppbMeterChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf1a7-113">已取出計量挑戰結果。</span><span class="sxs-lookup"><span data-stu-id="bf1a7-113">Retrieved metering challenge result.</span></span>

</dd> <dt>

<span data-ttu-id="bf1a7-114">*pcbMeterChallenge* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bf1a7-114">*pcbMeterChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf1a7-115">計量挑戰的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="bf1a7-115">The size of the metering challenge, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf1a7-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf1a7-116">Return value</span></span>

<span data-ttu-id="bf1a7-117">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="bf1a7-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bf1a7-118">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="bf1a7-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bf1a7-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bf1a7-119">Return code</span></span>                                                                          | <span data-ttu-id="bf1a7-120">Description</span><span class="sxs-lookup"><span data-stu-id="bf1a7-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bf1a7-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="bf1a7-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="bf1a7-122">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="bf1a7-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bf1a7-123">備註</span><span class="sxs-lookup"><span data-stu-id="bf1a7-123">Remarks</span></span>

<span data-ttu-id="bf1a7-124">計量資料會收集並儲存在裝置上的 DRM 資料存放區中，以啟用計量的內容。</span><span class="sxs-lookup"><span data-stu-id="bf1a7-124">Metering data is collected and stored in the DRM data store on the device for content with metering enabled.</span></span> <span data-ttu-id="bf1a7-125">將會記錄播放等動作。</span><span class="sxs-lookup"><span data-stu-id="bf1a7-125">Actions such as play will be recorded.</span></span> <span data-ttu-id="bf1a7-126">呼叫此函式時，裝置會以 XML 檔的形式收集 DRM 資料存放區中的計量資料，並將其傳送至 hostcomputer。</span><span class="sxs-lookup"><span data-stu-id="bf1a7-126">When this function is called, the device collects the metering data in the DRM data store in the form of an XML document and sends it to the hostcomputer.</span></span> <span data-ttu-id="bf1a7-127">如果有太多資料，則會分階段傳送。</span><span class="sxs-lookup"><span data-stu-id="bf1a7-127">If there is too much data, it is sent in phases.</span></span>

<span data-ttu-id="bf1a7-128">當主機電腦收到計量資料時，它會透過網際網路將資料傳送到計量憑證中指定的 URL。</span><span class="sxs-lookup"><span data-stu-id="bf1a7-128">When the host computer receives the metering data, it sends the data over the Internet to the URL specified in the metering certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf1a7-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf1a7-129">Requirements</span></span>



| <span data-ttu-id="bf1a7-130">需求</span><span class="sxs-lookup"><span data-stu-id="bf1a7-130">Requirement</span></span> | <span data-ttu-id="bf1a7-131">值</span><span class="sxs-lookup"><span data-stu-id="bf1a7-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf1a7-132">標頭</span><span class="sxs-lookup"><span data-stu-id="bf1a7-132">Header</span></span><br/>  | <dl> <span data-ttu-id="bf1a7-133"><dt>WMDDRMSP .idl</dt></span><span class="sxs-lookup"><span data-stu-id="bf1a7-133"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="bf1a7-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="bf1a7-134">Library</span></span><br/> | <dl> <span data-ttu-id="bf1a7-135"><dt>Mssachlp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf1a7-135"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf1a7-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf1a7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf1a7-137">**IWMDRMDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="bf1a7-137">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





