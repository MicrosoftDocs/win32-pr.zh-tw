---
title: DRM_HeaderSignPrivKey
description: DRM \_ HeaderSignPrivKey 屬性包含用來簽署 ASF 標頭的私密金鑰。
ms.assetid: 0f32e63d-d416-4a1d-b10c-2534b747adf3
keywords:
- DRM_HeaderSignPrivKey windows Media 格式
topic_type:
- apiref
api_name:
- DRM_HeaderSignPrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af73ea90acca6c20817f35a035f8f297aa56e90b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681406"
---
# <a name="drm_headersignprivkey"></a><span data-ttu-id="c953c-104">DRM \_ HeaderSignPrivKey</span><span class="sxs-lookup"><span data-stu-id="c953c-104">DRM\_HeaderSignPrivKey</span></span>

<span data-ttu-id="c953c-105">**DRM \_ HeaderSignPrivKey** 屬性包含用來簽署 ASF 標頭的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="c953c-105">The **DRM\_HeaderSignPrivKey** property contains the private key used to sign the ASF header.</span></span>

## <a name="global-constant"></a><span data-ttu-id="c953c-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="c953c-106">Global Constant</span></span>

<span data-ttu-id="c953c-107">g \_ wszWMDRM \_ HeaderSignPrivKey</span><span class="sxs-lookup"><span data-stu-id="c953c-107">g\_wszWMDRM\_HeaderSignPrivKey</span></span>

## <a name="data-type"></a><span data-ttu-id="c953c-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="c953c-108">Data Type</span></span>

<span data-ttu-id="c953c-109">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="c953c-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="c953c-110">備註</span><span class="sxs-lookup"><span data-stu-id="c953c-110">Remarks</span></span>

<span data-ttu-id="c953c-111">這個屬性是使用 [**IWMDRMWriter：： GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair)產生的。</span><span class="sxs-lookup"><span data-stu-id="c953c-111">This property is generated using the [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).</span></span> <span data-ttu-id="c953c-112">請保存此金鑰密碼，並只與授權服務共用公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="c953c-112">Keep this key secret and share the public key only with the license service.</span></span> <span data-ttu-id="c953c-113">設定此金鑰之後，DRM 元件會使用它來簽署 ASF 檔案標頭 (而不是使用數位簽章物件值（例如 DRM LASignaturePrivKey) ）簽署的 DRM 標頭 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c953c-113">After you set this key, the DRM component will use it to sign the ASF file header (not the DRM header which is signed with the digital signature object values such as DRM\_LASignaturePrivKey).</span></span> <span data-ttu-id="c953c-114">很明顯地， **DRM \_ HeaderSignPrivKey** 不包含在 headert 檔案中。</span><span class="sxs-lookup"><span data-stu-id="c953c-114">Obviously, **DRM\_HeaderSignPrivKey** is not included in the file headert.</span></span>

<span data-ttu-id="c953c-115">無法從 reader 物件存取這個屬性。</span><span class="sxs-lookup"><span data-stu-id="c953c-115">This property is not accessible from the reader object.</span></span> <span data-ttu-id="c953c-116">您可以使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)，從寫入器物件進行設定。</span><span class="sxs-lookup"><span data-stu-id="c953c-116">It can be set from the writer object using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span>

## <a name="see-also"></a><span data-ttu-id="c953c-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c953c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c953c-118">**DRM 屬性**</span><span class="sxs-lookup"><span data-stu-id="c953c-118">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




