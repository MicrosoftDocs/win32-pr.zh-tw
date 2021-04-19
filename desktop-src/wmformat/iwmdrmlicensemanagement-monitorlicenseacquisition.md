---
title: 'IWMDRMLicenseManagement MonitorLicenseAcquisition 方法 (Wmdrmsdk .h) '
description: MonitorLicenseAcquisition 方法會起始授權取得程式的監視。
ms.assetid: 725cd51a-a50b-4ff5-a880-7f551f6dba8f
keywords:
- MonitorLicenseAcquisition 方法 windows Media 格式
- MonitorLicenseAcquisition 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，MonitorLicenseAcquisition 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.MonitorLicenseAcquisition
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25171d36a9d360f7c8eb77211c580c4f7676618f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986562"
---
# <a name="iwmdrmlicensemanagementmonitorlicenseacquisition-method"></a><span data-ttu-id="eb5a3-106">IWMDRMLicenseManagement：： MonitorLicenseAcquisition 方法</span><span class="sxs-lookup"><span data-stu-id="eb5a3-106">IWMDRMLicenseManagement::MonitorLicenseAcquisition method</span></span>

<span data-ttu-id="eb5a3-107">**MonitorLicenseAcquisition** 方法會起始授權取得程式的監視。</span><span class="sxs-lookup"><span data-stu-id="eb5a3-107">The **MonitorLicenseAcquisition** method initiates monitoring for a license acquisition process.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb5a3-108">語法</span><span class="sxs-lookup"><span data-stu-id="eb5a3-108">Syntax</span></span>


```C++
HRESULT MonitorLicenseAcquisition(
  [in]  BSTR     bstrKID,
  [in]  BSTR     bstrHeader,
  [in]  BSTR     bstrActions,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="eb5a3-109">參數</span><span class="sxs-lookup"><span data-stu-id="eb5a3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb5a3-110">*bstrKID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb5a3-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb5a3-111">取得的授權 (小孩) 的金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb5a3-111">Key ID (KID) of the license being acquired.</span></span>

</dd> <dt>

<span data-ttu-id="eb5a3-112">*bstrHeader* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb5a3-112">*bstrHeader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb5a3-113">[**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md)方法呼叫中使用的內容標頭。</span><span class="sxs-lookup"><span data-stu-id="eb5a3-113">Content header that was used in the call to the [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="eb5a3-114">*bstrActions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb5a3-114">*bstrActions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb5a3-115">字串，包含在呼叫 **AcquireLicense** 方法時所要求的動作。</span><span class="sxs-lookup"><span data-stu-id="eb5a3-115">String containing the actions requested in the call to the **AcquireLicense** method.</span></span>

</dd> <dt>

<span data-ttu-id="eb5a3-116">*ppunkCancelationCookie* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="eb5a3-116">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb5a3-117">指標，接收識別此非同步呼叫之物件的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="eb5a3-117">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="eb5a3-118">這個介面指標可透過呼叫 [**IWMDRMEventGenerator：： CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) 方法，用來取消非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="eb5a3-118">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb5a3-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb5a3-119">Return value</span></span>

<span data-ttu-id="eb5a3-120">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="eb5a3-120">The method returns an **HRESULT**.</span></span> <span data-ttu-id="eb5a3-121">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="eb5a3-121">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="eb5a3-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="eb5a3-122">Return code</span></span>                                                                          | <span data-ttu-id="eb5a3-123">Description</span><span class="sxs-lookup"><span data-stu-id="eb5a3-123">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="eb5a3-124"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="eb5a3-124"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="eb5a3-125">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="eb5a3-125">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eb5a3-126">備註</span><span class="sxs-lookup"><span data-stu-id="eb5a3-126">Remarks</span></span>

<span data-ttu-id="eb5a3-127">無。</span><span class="sxs-lookup"><span data-stu-id="eb5a3-127">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb5a3-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb5a3-128">Requirements</span></span>



| <span data-ttu-id="eb5a3-129">需求</span><span class="sxs-lookup"><span data-stu-id="eb5a3-129">Requirement</span></span> | <span data-ttu-id="eb5a3-130">值</span><span class="sxs-lookup"><span data-stu-id="eb5a3-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb5a3-131">標頭</span><span class="sxs-lookup"><span data-stu-id="eb5a3-131">Header</span></span><br/>  | <dl> <span data-ttu-id="eb5a3-132"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="eb5a3-132"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb5a3-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="eb5a3-133">Library</span></span><br/> | <dl> <span data-ttu-id="eb5a3-134"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb5a3-134"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb5a3-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb5a3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb5a3-136">**IWMDRMLicenseManagement 介面**</span><span class="sxs-lookup"><span data-stu-id="eb5a3-136">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





