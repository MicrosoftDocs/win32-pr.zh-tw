---
title: 'IWMDRMSecurity GetRevocationData 方法 (Wmdrmsdk .h) '
description: GetRevocationData 方法會從本機存放區抓取憑證撤銷清單。
ms.assetid: 218f4f3a-02bc-4b1d-9320-e35ed8cc3b11
keywords:
- GetRevocationData 方法 windows Media 格式
- GetRevocationData 方法 windows Media Format，IWMDRMSecurity 介面
- IWMDRMSecurity 介面 windows Media Format，GetRevocationData 方法
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e9e0b428a3922f84141ef855d8468b79b3bb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989720"
---
# <a name="iwmdrmsecuritygetrevocationdata-method"></a><span data-ttu-id="3a1ec-106">IWMDRMSecurity：： GetRevocationData 方法</span><span class="sxs-lookup"><span data-stu-id="3a1ec-106">IWMDRMSecurity::GetRevocationData method</span></span>

<span data-ttu-id="3a1ec-107">**GetRevocationData** 方法會從本機存放區抓取憑證撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="3a1ec-107">The **GetRevocationData** method retrieves a certificate revocation list from the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a1ec-108">語法</span><span class="sxs-lookup"><span data-stu-id="3a1ec-108">Syntax</span></span>


```C++
HRESULT GetRevocationData(
  [in]      REFGUID f_guidRevocationType,
  [out]     BYTE    *f_pbCRL,
  [in, out] DWORD   *f_pcbCRL
);
```



## <a name="parameters"></a><span data-ttu-id="3a1ec-109">參數</span><span class="sxs-lookup"><span data-stu-id="3a1ec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a1ec-110">*f \_ guidRevocationType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a1ec-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a1ec-111">識別要取出的撤銷清單類型的 GUID。</span><span class="sxs-lookup"><span data-stu-id="3a1ec-111">GUID identifying the type of revocation list to retrieve.</span></span> <span data-ttu-id="3a1ec-112">使用下表中的其中一個常數。</span><span class="sxs-lookup"><span data-stu-id="3a1ec-112">Use one of the constants in the following table.</span></span>



| <span data-ttu-id="3a1ec-113">GUID 常數</span><span class="sxs-lookup"><span data-stu-id="3a1ec-113">GUID constant</span></span>                 | <span data-ttu-id="3a1ec-114">Description</span><span class="sxs-lookup"><span data-stu-id="3a1ec-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3a1ec-115">WMDRM \_ REVOCATIONTYPE \_ 應用程式</span><span class="sxs-lookup"><span data-stu-id="3a1ec-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="3a1ec-116">指定應用程式憑證撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="3a1ec-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="3a1ec-117">WMDRM \_ REVOCATIONTYPE \_ 裝置</span><span class="sxs-lookup"><span data-stu-id="3a1ec-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="3a1ec-118">指定裝置憑證撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="3a1ec-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="3a1ec-119">WMDRM \_ REVOCATIONTYPE \_ CARDEA</span><span class="sxs-lookup"><span data-stu-id="3a1ec-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="3a1ec-120">指定「網路裝置的 Windows Media DRM」憑證撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="3a1ec-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="3a1ec-121">*f \_ pbCRL* \[ 輸出\]</span><span class="sxs-lookup"><span data-stu-id="3a1ec-121">*f\_pbCRL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a1ec-122">接收撤銷清單的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3a1ec-122">Buffer that receives the revocation list.</span></span> <span data-ttu-id="3a1ec-123">設定為 **Null** 可取得所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="3a1ec-123">Set to **NULL** to get the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="3a1ec-124">*f \_ pcbCRL* \[ in，out\]</span><span class="sxs-lookup"><span data-stu-id="3a1ec-124">*f\_pcbCRL* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a1ec-125">以位元組為單位的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="3a1ec-125">Size of the buffer in bytes.</span></span> <span data-ttu-id="3a1ec-126">如果 *f \_ PbCRL* 為 **Null**，則會在輸出時將此值設定為所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="3a1ec-126">If *f\_pbCRL* is **NULL**, this value is set to the required buffer size on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a1ec-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a1ec-127">Return value</span></span>

<span data-ttu-id="3a1ec-128">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="3a1ec-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3a1ec-129">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="3a1ec-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3a1ec-130">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3a1ec-130">Return code</span></span>                                                                          | <span data-ttu-id="3a1ec-131">Description</span><span class="sxs-lookup"><span data-stu-id="3a1ec-131">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3a1ec-132"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3a1ec-132"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3a1ec-133">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="3a1ec-133">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3a1ec-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a1ec-134">Requirements</span></span>



| <span data-ttu-id="3a1ec-135">需求</span><span class="sxs-lookup"><span data-stu-id="3a1ec-135">Requirement</span></span> | <span data-ttu-id="3a1ec-136">值</span><span class="sxs-lookup"><span data-stu-id="3a1ec-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a1ec-137">標頭</span><span class="sxs-lookup"><span data-stu-id="3a1ec-137">Header</span></span><br/>  | <dl> <span data-ttu-id="3a1ec-138"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="3a1ec-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a1ec-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="3a1ec-139">Library</span></span><br/> | <dl> <span data-ttu-id="3a1ec-140"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a1ec-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a1ec-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a1ec-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a1ec-142">**自動化元件撤銷和更新**</span><span class="sxs-lookup"><span data-stu-id="3a1ec-142">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="3a1ec-143">**GetRevocationDataVersion**</span><span class="sxs-lookup"><span data-stu-id="3a1ec-143">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[<span data-ttu-id="3a1ec-144">**IWMDRMSecurity 介面**</span><span class="sxs-lookup"><span data-stu-id="3a1ec-144">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="3a1ec-145">**SetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="3a1ec-145">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





