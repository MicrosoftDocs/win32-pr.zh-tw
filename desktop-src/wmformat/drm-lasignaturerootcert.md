---
title: DRM_LASignatureRootCert
description: DRM \_ LASignatureRootCert 屬性包含憑證連結中的根憑證，用來驗證 DRM LASignatureLicSrvCert 中包含的憑證 \_ 。
ms.assetid: b1e44a80-5fff-4a6a-bacd-6384546673c6
keywords:
- DRM_LASignatureRootCert windows Media 格式
topic_type:
- apiref
api_name:
- DRM_LASignatureRootCert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecb36cca2a98e74a027c427a79440fe9989c7ef0
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374535"
---
# <a name="drm_lasignaturerootcert"></a><span data-ttu-id="164fb-104">DRM \_ LASignatureRootCert</span><span class="sxs-lookup"><span data-stu-id="164fb-104">DRM\_LASignatureRootCert</span></span>

<span data-ttu-id="164fb-105">**Drm \_ LASignatureRootCert** 屬性包含憑證連結中的根憑證，用來驗證 [**DRM \_ LASignatureLicSrvCert**](drm-lasignaturelicsrvcert.md)中包含的憑證。</span><span class="sxs-lookup"><span data-stu-id="164fb-105">The **DRM\_LASignatureRootCert** attribute contains the root certificate in the certification chain that is used to authenticate the certificate contained in [**DRM\_LASignatureLicSrvCert**](drm-lasignaturelicsrvcert.md).</span></span>

## <a name="global-constant"></a><span data-ttu-id="164fb-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="164fb-106">Global Constant</span></span>

<span data-ttu-id="164fb-107">g \_ wszWMDRM \_ LASignatureRootCert</span><span class="sxs-lookup"><span data-stu-id="164fb-107">g\_wszWMDRM\_LASignatureRootCert</span></span>

## <a name="data-type"></a><span data-ttu-id="164fb-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="164fb-108">Data Type</span></span>

<span data-ttu-id="164fb-109">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="164fb-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="164fb-110">備註</span><span class="sxs-lookup"><span data-stu-id="164fb-110">Remarks</span></span>

<span data-ttu-id="164fb-111">您可以使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 方法來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="164fb-111">This property can be set with the [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) method.</span></span> <span data-ttu-id="164fb-112">讀取器物件無法存取它。</span><span class="sxs-lookup"><span data-stu-id="164fb-112">It is not accessible to the reader object.</span></span>

## <a name="see-also"></a><span data-ttu-id="164fb-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="164fb-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="164fb-114">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="164fb-114">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




