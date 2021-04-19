---
title: IWMDRMDevice GetSecureClock 方法
description: GetSecureClock 方法會抓取安全時鐘，因此可以強制執行以時間為基礎的授權。
ms.assetid: 6de9b7ce-9c2a-44e5-9de7-40cfbaf4d92c
keywords:
- GetSecureClock 方法 windows Media 裝置管理員
- GetSecureClock 方法 windows Media 裝置管理員，IWMDRMDevice 介面
- IWMDRMDevice interface windows Media 裝置管理員，GetSecureClock 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClock
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa92c3bc2ee82facf2f2e1043e71467a0c55bd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976762"
---
# <a name="iwmdrmdevicegetsecureclock-method"></a><span data-ttu-id="8f951-106">IWMDRMDevice：： GetSecureClock 方法</span><span class="sxs-lookup"><span data-stu-id="8f951-106">IWMDRMDevice::GetSecureClock method</span></span>

<span data-ttu-id="8f951-107">**GetSecureClock** 方法會抓取安全時鐘，因此可以強制執行以時間為基礎的授權。</span><span class="sxs-lookup"><span data-stu-id="8f951-107">The **GetSecureClock** method retrieves the secure clock, so time-based licenses can be enforced.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f951-108">語法</span><span class="sxs-lookup"><span data-stu-id="8f951-108">Syntax</span></span>


```C++
HRESULT GetSecureClock(
  [out] BYTE  **ppbSecureClock,
  [out] DWORD *pcbSecureClock,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8f951-109">參數</span><span class="sxs-lookup"><span data-stu-id="8f951-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f951-110">*ppbSecureClock* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8f951-110">*ppbSecureClock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f951-111">已取出安全時鐘。</span><span class="sxs-lookup"><span data-stu-id="8f951-111">Retrieved secure clock.</span></span>

</dd> <dt>

<span data-ttu-id="8f951-112">*pcbSecureClock* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8f951-112">*pcbSecureClock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f951-113">安全時鐘的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8f951-113">Size of the secure clock, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8f951-114">*pdwFlags* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8f951-114">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f951-115">裝置狀態旗標。</span><span class="sxs-lookup"><span data-stu-id="8f951-115">Device status flags.</span></span> <span data-ttu-id="8f951-116">此值必須是下列其中一個旗標。</span><span class="sxs-lookup"><span data-stu-id="8f951-116">This value must be one of the following flags.</span></span>



| <span data-ttu-id="8f951-117">旗標</span><span class="sxs-lookup"><span data-stu-id="8f951-117">Flag</span></span>                     | <span data-ttu-id="8f951-118">描述</span><span class="sxs-lookup"><span data-stu-id="8f951-118">Description</span></span>                            |
|--------------------------|----------------------------------------|
| <span data-ttu-id="8f951-119">WMDRM \_ 裝置 \_ ISWMDRM</span><span class="sxs-lookup"><span data-stu-id="8f951-119">WMDRM\_DEVICE\_ISWMDRM</span></span>   | <span data-ttu-id="8f951-120">裝置支援 Windows Media DRM。</span><span class="sxs-lookup"><span data-stu-id="8f951-120">The device supports Windows Media DRM.</span></span> |
| <span data-ttu-id="8f951-121">WMDRM \_ 裝置 \_ NEEDCLOCK</span><span class="sxs-lookup"><span data-stu-id="8f951-121">WMDRM\_DEVICE\_NEEDCLOCK</span></span> | <span data-ttu-id="8f951-122">裝置需要時鐘。</span><span class="sxs-lookup"><span data-stu-id="8f951-122">The device needs clock.</span></span>                |
| <span data-ttu-id="8f951-123">已 \_ 撤銷 WMDRM 裝置 \_</span><span class="sxs-lookup"><span data-stu-id="8f951-123">WMDRM\_DEVICE\_REVOKED</span></span>   | <span data-ttu-id="8f951-124">裝置已遭撤銷。</span><span class="sxs-lookup"><span data-stu-id="8f951-124">The device has been revoked.</span></span>           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f951-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="8f951-125">Return value</span></span>

<span data-ttu-id="8f951-126">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="8f951-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8f951-127">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="8f951-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8f951-128">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8f951-128">Return code</span></span>                                                                          | <span data-ttu-id="8f951-129">Description</span><span class="sxs-lookup"><span data-stu-id="8f951-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8f951-130"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8f951-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8f951-131">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="8f951-131">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8f951-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f951-132">Requirements</span></span>



| <span data-ttu-id="8f951-133">需求</span><span class="sxs-lookup"><span data-stu-id="8f951-133">Requirement</span></span> | <span data-ttu-id="8f951-134">值</span><span class="sxs-lookup"><span data-stu-id="8f951-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f951-135">標頭</span><span class="sxs-lookup"><span data-stu-id="8f951-135">Header</span></span><br/>  | <dl> <span data-ttu-id="8f951-136"><dt>WMDDRMSP .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8f951-136"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="8f951-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="8f951-137">Library</span></span><br/> | <dl> <span data-ttu-id="8f951-138"><dt>Mssachlp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f951-138"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f951-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f951-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f951-140">**GetSecureClockChallenge**</span><span class="sxs-lookup"><span data-stu-id="8f951-140">**GetSecureClockChallenge**</span></span>](iwmdrmdevice-getsecureclockchallenge.md)
</dt> <dt>

[<span data-ttu-id="8f951-141">**IWMDRMDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="8f951-141">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> <dt>

[<span data-ttu-id="8f951-142">**SetSecureClockResponse**</span><span class="sxs-lookup"><span data-stu-id="8f951-142">**SetSecureClockResponse**</span></span>](iwmdrmdevice-setsecureclockresponse.md)
</dt> </dl>

 

 





