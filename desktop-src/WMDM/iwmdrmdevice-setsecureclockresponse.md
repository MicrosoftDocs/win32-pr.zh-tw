---
title: IWMDRMDevice SetSecureClockResponse 方法
description: SetSecureClockResponse 方法會設定安全的時鐘回應。
ms.assetid: 3f0a1487-d8c4-478d-bfb0-8d09931fd4b6
keywords:
- SetSecureClockResponse 方法 windows Media 裝置管理員
- SetSecureClockResponse 方法 windows Media 裝置管理員，IWMDRMDevice 介面
- IWMDRMDevice interface windows Media 裝置管理員，SetSecureClockResponse 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetSecureClockResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821aceda734aceb7a80774db05465f31213eec47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986597"
---
# <a name="iwmdrmdevicesetsecureclockresponse-method"></a><span data-ttu-id="8684a-106">IWMDRMDevice：： SetSecureClockResponse 方法</span><span class="sxs-lookup"><span data-stu-id="8684a-106">IWMDRMDevice::SetSecureClockResponse method</span></span>

<span data-ttu-id="8684a-107">**SetSecureClockResponse** 方法會設定安全的時鐘回應。</span><span class="sxs-lookup"><span data-stu-id="8684a-107">The **SetSecureClockResponse** method sets the secure clock response.</span></span>

## <a name="syntax"></a><span data-ttu-id="8684a-108">語法</span><span class="sxs-lookup"><span data-stu-id="8684a-108">Syntax</span></span>


```C++
HRESULT SetSecureClockResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a><span data-ttu-id="8684a-109">參數</span><span class="sxs-lookup"><span data-stu-id="8684a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8684a-110">*pbResponse* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8684a-110">*pbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8684a-111">要設定的安全時鐘回應。</span><span class="sxs-lookup"><span data-stu-id="8684a-111">The secure clock response to be set.</span></span>

</dd> <dt>

<span data-ttu-id="8684a-112">*cbResponse* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8684a-112">*cbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8684a-113">指定的安全時鐘回應大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8684a-113">The specified size of the secure clock response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8684a-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="8684a-114">Return value</span></span>

<span data-ttu-id="8684a-115">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="8684a-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8684a-116">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="8684a-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8684a-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8684a-117">Return code</span></span>                                                                          | <span data-ttu-id="8684a-118">Description</span><span class="sxs-lookup"><span data-stu-id="8684a-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8684a-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8684a-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8684a-120">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="8684a-120">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8684a-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="8684a-121">Requirements</span></span>



| <span data-ttu-id="8684a-122">需求</span><span class="sxs-lookup"><span data-stu-id="8684a-122">Requirement</span></span> | <span data-ttu-id="8684a-123">值</span><span class="sxs-lookup"><span data-stu-id="8684a-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8684a-124">標頭</span><span class="sxs-lookup"><span data-stu-id="8684a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8684a-125"><dt>WMDDRMSP .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8684a-125"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="8684a-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="8684a-126">Library</span></span><br/> | <dl> <span data-ttu-id="8684a-127"><dt>Mssachlp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8684a-127"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8684a-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8684a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8684a-129">**GetSecureClock**</span><span class="sxs-lookup"><span data-stu-id="8684a-129">**GetSecureClock**</span></span>](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[<span data-ttu-id="8684a-130">**IWMDRMDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="8684a-130">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





