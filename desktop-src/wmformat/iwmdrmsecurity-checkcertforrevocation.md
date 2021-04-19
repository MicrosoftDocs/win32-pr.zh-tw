---
title: 'IWMDRMSecurity CheckCertForRevocation 方法 (Wmdrmsdk .h) '
description: CheckCertForRevocation 方法會判斷憑證是否已撤銷。
ms.assetid: 3efde398-f2ba-486e-b017-6787ca402e4c
keywords:
- CheckCertForRevocation 方法 windows Media 格式
- CheckCertForRevocation 方法 windows Media Format，IWMDRMSecurity 介面
- IWMDRMSecurity 介面 windows Media Format，CheckCertForRevocation 方法
topic_type:
- apiref
api_name:
- IWMDRMSecurity.CheckCertForRevocation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a2439085c6483720e84956ef9932f4f1ab95535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982542"
---
# <a name="iwmdrmsecuritycheckcertforrevocation-method"></a><span data-ttu-id="52a35-106">IWMDRMSecurity：： CheckCertForRevocation 方法</span><span class="sxs-lookup"><span data-stu-id="52a35-106">IWMDRMSecurity::CheckCertForRevocation method</span></span>

<span data-ttu-id="52a35-107">**CheckCertForRevocation** 方法會判斷憑證是否已撤銷。</span><span class="sxs-lookup"><span data-stu-id="52a35-107">The **CheckCertForRevocation** method determines whether a certificate has been revoked.</span></span>

## <a name="syntax"></a><span data-ttu-id="52a35-108">語法</span><span class="sxs-lookup"><span data-stu-id="52a35-108">Syntax</span></span>


```C++
HRESULT CheckCertForRevocation(
  [in]  REFGUID rguidRevocationList,
  [in]  BYTE    *pbCert,
  [in]  DWORD   cbCert,
  [out] BOOL    *fRevoked
);
```



## <a name="parameters"></a><span data-ttu-id="52a35-109">參數</span><span class="sxs-lookup"><span data-stu-id="52a35-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52a35-110">*rguidRevocationList* \[在\]</span><span class="sxs-lookup"><span data-stu-id="52a35-110">*rguidRevocationList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52a35-111">識別要使用之撤銷清單的 GUID。</span><span class="sxs-lookup"><span data-stu-id="52a35-111">GUID identifying the revocation list to use.</span></span> <span data-ttu-id="52a35-112">設定為下表中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="52a35-112">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="52a35-113">GUID 常數</span><span class="sxs-lookup"><span data-stu-id="52a35-113">GUID constant</span></span>                 | <span data-ttu-id="52a35-114">Description</span><span class="sxs-lookup"><span data-stu-id="52a35-114">Description</span></span>                                                                                |
|-------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="52a35-115">WMDRM \_ REVOCATIONTYPE \_ 應用程式</span><span class="sxs-lookup"><span data-stu-id="52a35-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="52a35-116">指定應用程式憑證撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="52a35-116">Specifies the application certificate revocation list.</span></span>                                     |
| <span data-ttu-id="52a35-117">WMDRM \_ REVOCATIONTYPE \_ 裝置</span><span class="sxs-lookup"><span data-stu-id="52a35-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="52a35-118">指定裝置憑證撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="52a35-118">Specifies the device certificate revocation list.</span></span>                                          |
| <span data-ttu-id="52a35-119">WMDRM \_ REVOCATIONTYPE \_ CARDEA</span><span class="sxs-lookup"><span data-stu-id="52a35-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="52a35-120">指定 Microsoft Windows Media DRM for Network Devices 憑證撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="52a35-120">Specifies the Microsoft Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="52a35-121">*pbCert* \[在\]</span><span class="sxs-lookup"><span data-stu-id="52a35-121">*pbCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52a35-122">包含要查閱之憑證的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="52a35-122">Buffer containing the certificate to look up.</span></span>

</dd> <dt>

<span data-ttu-id="52a35-123">*cbCert* \[在\]</span><span class="sxs-lookup"><span data-stu-id="52a35-123">*cbCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52a35-124">緩衝區 *pbCert* 的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="52a35-124">Size of the buffer *pbCert*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="52a35-125">*fRevoked* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="52a35-125">*fRevoked* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52a35-126">在 [輸出] 上，指出憑證是否存在於撤銷清單中。</span><span class="sxs-lookup"><span data-stu-id="52a35-126">On output, indicates whether the certificate is present in the revocation list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52a35-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="52a35-127">Return value</span></span>

<span data-ttu-id="52a35-128">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="52a35-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="52a35-129">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="52a35-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="52a35-130">傳回碼</span><span class="sxs-lookup"><span data-stu-id="52a35-130">Return code</span></span>                                                                          | <span data-ttu-id="52a35-131">Description</span><span class="sxs-lookup"><span data-stu-id="52a35-131">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="52a35-132"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="52a35-132"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="52a35-133">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="52a35-133">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="52a35-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="52a35-134">Requirements</span></span>



| <span data-ttu-id="52a35-135">需求</span><span class="sxs-lookup"><span data-stu-id="52a35-135">Requirement</span></span> | <span data-ttu-id="52a35-136">值</span><span class="sxs-lookup"><span data-stu-id="52a35-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52a35-137">標頭</span><span class="sxs-lookup"><span data-stu-id="52a35-137">Header</span></span><br/>  | <dl> <span data-ttu-id="52a35-138"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="52a35-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="52a35-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="52a35-139">Library</span></span><br/> | <dl> <span data-ttu-id="52a35-140"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="52a35-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52a35-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52a35-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52a35-142">**IWMDRMSecurity 介面**</span><span class="sxs-lookup"><span data-stu-id="52a35-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





