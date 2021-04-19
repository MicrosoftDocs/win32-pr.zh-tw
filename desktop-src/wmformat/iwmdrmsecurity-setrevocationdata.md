---
title: 'IWMDRMSecurity SetRevocationData 方法 (Wmdrmsdk .h) '
description: SetRevocationData 方法會在本機存放區中設定憑證撤銷清單。
ms.assetid: 7e1c6d50-7a22-41b7-b29f-b1e5809a2097
keywords:
- SetRevocationData 方法 windows Media 格式
- SetRevocationData 方法 windows Media Format，IWMDRMSecurity 介面
- IWMDRMSecurity 介面 windows Media Format，SetRevocationData 方法
topic_type:
- apiref
api_name:
- IWMDRMSecurity.SetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3ece5a9285420261add123a61d0b7123896e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990117"
---
# <a name="iwmdrmsecuritysetrevocationdata-method"></a><span data-ttu-id="11a5b-106">IWMDRMSecurity：： SetRevocationData 方法</span><span class="sxs-lookup"><span data-stu-id="11a5b-106">IWMDRMSecurity::SetRevocationData method</span></span>

<span data-ttu-id="11a5b-107">**SetRevocationData** 方法會在本機存放區中設定憑證撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="11a5b-107">The **SetRevocationData** method sets a certificate revocation list in the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="11a5b-108">語法</span><span class="sxs-lookup"><span data-stu-id="11a5b-108">Syntax</span></span>


```C++
HRESULT SetRevocationData(
  [in] REFGUID f_guidRevocationType,
  [in] BYTE    *f_pbCRL,
  [in] DWORD   f_cbCRL
);
```



## <a name="parameters"></a><span data-ttu-id="11a5b-109">參數</span><span class="sxs-lookup"><span data-stu-id="11a5b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11a5b-110">*f \_ guidRevocationType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11a5b-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11a5b-111">指定撤銷清單類型的 GUID。</span><span class="sxs-lookup"><span data-stu-id="11a5b-111">GUID specifying the type of revocation list.</span></span> <span data-ttu-id="11a5b-112">設定為下表中的其中一個常數。</span><span class="sxs-lookup"><span data-stu-id="11a5b-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="11a5b-113">GUID 常數</span><span class="sxs-lookup"><span data-stu-id="11a5b-113">GUID constant</span></span>                 | <span data-ttu-id="11a5b-114">Description</span><span class="sxs-lookup"><span data-stu-id="11a5b-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="11a5b-115">WMDRM \_ REVOCATIONTYPE \_ 應用程式</span><span class="sxs-lookup"><span data-stu-id="11a5b-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="11a5b-116">指定應用程式憑證撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="11a5b-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="11a5b-117">WMDRM \_ REVOCATIONTYPE \_ 裝置</span><span class="sxs-lookup"><span data-stu-id="11a5b-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="11a5b-118">指定裝置憑證撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="11a5b-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="11a5b-119">WMDRM \_ REVOCATIONTYPE \_ CARDEA</span><span class="sxs-lookup"><span data-stu-id="11a5b-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="11a5b-120">指定「網路裝置的 Windows Media DRM」憑證撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="11a5b-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="11a5b-121">*f \_ pbCRL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11a5b-121">*f\_pbCRL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11a5b-122">包含憑證撤銷清單的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="11a5b-122">Buffer containing the certificate revocation list.</span></span>

</dd> <dt>

<span data-ttu-id="11a5b-123">*f \_ cbCRL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11a5b-123">*f\_cbCRL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11a5b-124">緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="11a5b-124">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11a5b-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="11a5b-125">Return value</span></span>

<span data-ttu-id="11a5b-126">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="11a5b-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="11a5b-127">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="11a5b-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="11a5b-128">傳回碼</span><span class="sxs-lookup"><span data-stu-id="11a5b-128">Return code</span></span>                                                                          | <span data-ttu-id="11a5b-129">Description</span><span class="sxs-lookup"><span data-stu-id="11a5b-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="11a5b-130"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="11a5b-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="11a5b-131">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="11a5b-131">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="11a5b-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="11a5b-132">Requirements</span></span>



| <span data-ttu-id="11a5b-133">需求</span><span class="sxs-lookup"><span data-stu-id="11a5b-133">Requirement</span></span> | <span data-ttu-id="11a5b-134">值</span><span class="sxs-lookup"><span data-stu-id="11a5b-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11a5b-135">標頭</span><span class="sxs-lookup"><span data-stu-id="11a5b-135">Header</span></span><br/>  | <dl> <span data-ttu-id="11a5b-136"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="11a5b-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="11a5b-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="11a5b-137">Library</span></span><br/> | <dl> <span data-ttu-id="11a5b-138"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="11a5b-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11a5b-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11a5b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11a5b-140">**GetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="11a5b-140">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[<span data-ttu-id="11a5b-141">**GetRevocationDataVersion**</span><span class="sxs-lookup"><span data-stu-id="11a5b-141">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[<span data-ttu-id="11a5b-142">**IWMDRMSecurity 介面**</span><span class="sxs-lookup"><span data-stu-id="11a5b-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





