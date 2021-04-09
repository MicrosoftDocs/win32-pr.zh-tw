---
description: 通知應用程式，已完成對 MTP/Bluetooth 裝置的先前排程連線或中斷連接要求。
ms.assetid: 1588d0ec-0d6a-4379-bfdc-4ba5fdaa4665
title: 'IConnectionRequestCallback：： OnComplete 方法 (Devpkey .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback.OnComplete
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 922169b7e17335c47425665bb9a9e54891e68723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850407"
---
# <a name="iconnectionrequestcallbackoncomplete-method"></a><span data-ttu-id="f1caa-103">IConnectionRequestCallback：： OnComplete 方法</span><span class="sxs-lookup"><span data-stu-id="f1caa-103">IConnectionRequestCallback::OnComplete method</span></span>

<span data-ttu-id="f1caa-104">**OnComplete** 方法會通知應用程式先前已排程的連線，或對 MTP/Bluetooth 裝置的中斷連接要求已完成</span><span class="sxs-lookup"><span data-stu-id="f1caa-104">The **OnComplete** method notifies an application that a previously scheduled Connect or Disconnect request to the MTP/Bluetooth device has completed</span></span>

## <a name="syntax"></a><span data-ttu-id="f1caa-105">語法</span><span class="sxs-lookup"><span data-stu-id="f1caa-105">Syntax</span></span>


```C++
HRESULT OnComplete(
  [in] HRESULT hrStatus
);
```



## <a name="parameters"></a><span data-ttu-id="f1caa-106">參數</span><span class="sxs-lookup"><span data-stu-id="f1caa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1caa-107">*hrStatus* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1caa-107">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1caa-108">連接或中斷指定裝置連線的要求狀態。</span><span class="sxs-lookup"><span data-stu-id="f1caa-108">The status of the request to connect or disconnect a given device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1caa-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1caa-109">Return value</span></span>

<span data-ttu-id="f1caa-110">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="f1caa-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f1caa-111">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="f1caa-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f1caa-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f1caa-112">Return code</span></span>                                                                          | <span data-ttu-id="f1caa-113">Description</span><span class="sxs-lookup"><span data-stu-id="f1caa-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f1caa-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f1caa-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f1caa-115">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="f1caa-115">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f1caa-116">備註</span><span class="sxs-lookup"><span data-stu-id="f1caa-116">Remarks</span></span>

<span data-ttu-id="f1caa-117">應用程式會執行 [**IConnectionRequestCallback**](iconnectionrequestcallback.md) 介面，以接收有關已完成要求的通知，以及解除擱置的要求。</span><span class="sxs-lookup"><span data-stu-id="f1caa-117">An application implements the [**IConnectionRequestCallback**](iconnectionrequestcallback.md) interface to receive notifications about completed requests and to cancel pending requests.</span></span>

<span data-ttu-id="f1caa-118">Windows 可攜式裝置 (WPD) 呼叫這個方法，以通知應用程式先前已排程的要求已完成。</span><span class="sxs-lookup"><span data-stu-id="f1caa-118">Windows Portable Devices (WPD) calls this method to notify an application that a previously scheduled request has completed.</span></span> <span data-ttu-id="f1caa-119">每個要求都可以透過應用程式提供的回呼來追蹤和取消。</span><span class="sxs-lookup"><span data-stu-id="f1caa-119">Each request can be tracked and canceled by its application-supplied callback.</span></span> <span data-ttu-id="f1caa-120">因此，如果應用程式需要使用相同的 [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) 物件同時傳送多個要求，則每個要求都應傳遞唯一的 [**IConnectionRequestCallback**](iconnectionrequestcallback.md) 物件做為 [**IPortableDeviceConnector：： Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) 和 [**IPortableDeviceConnector：:D isconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) 方法的輸入參數。</span><span class="sxs-lookup"><span data-stu-id="f1caa-120">Therefore, if the application needs to send multiple requests at the same time using the same [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) object, each request should be passed a unique [**IConnectionRequestCallback**](iconnectionrequestcallback.md) object as the input parameter to the [**IPortableDeviceConnector::Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) and [**IPortableDeviceConnector::Disconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1caa-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1caa-121">Requirements</span></span>



| <span data-ttu-id="f1caa-122">需求</span><span class="sxs-lookup"><span data-stu-id="f1caa-122">Requirement</span></span> | <span data-ttu-id="f1caa-123">值</span><span class="sxs-lookup"><span data-stu-id="f1caa-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1caa-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1caa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f1caa-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1caa-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="f1caa-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1caa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f1caa-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="f1caa-127">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="f1caa-128">標頭</span><span class="sxs-lookup"><span data-stu-id="f1caa-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1caa-129"><dt>Devpkey .h;</dt><dt>Portabledeviceconnectapi .h</dt></span><span class="sxs-lookup"><span data-stu-id="f1caa-129"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="f1caa-130">Idl</span><span class="sxs-lookup"><span data-stu-id="f1caa-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f1caa-131"><dt>Portabledeviceconnectapi .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f1caa-131"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="f1caa-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="f1caa-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="f1caa-133"><dt>PortableDeviceGuids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1caa-133"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="f1caa-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1caa-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1caa-135">**IConnectionRequestCallback**</span><span class="sxs-lookup"><span data-stu-id="f1caa-135">**IConnectionRequestCallback**</span></span>](iconnectionrequestcallback.md)
</dt> </dl>

 

 




