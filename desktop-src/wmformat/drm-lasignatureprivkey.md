---
title: DRM_LASignaturePrivKey
description: DRM \_ LASignaturePrivKey 屬性包含用來加密 DRM 標頭的私密金鑰。
ms.assetid: b7083237-da11-4f31-a143-c0278a54b5a6
keywords:
- DRM_LASignaturePrivKey windows Media 格式
topic_type:
- apiref
api_name:
- DRM_LASignaturePrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdb22f3abc57fc2331ff87bd05bc05d580d607c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374534"
---
# <a name="drm_lasignatureprivkey"></a><span data-ttu-id="f0a37-104">DRM \_ LASignaturePrivKey</span><span class="sxs-lookup"><span data-stu-id="f0a37-104">DRM\_LASignaturePrivKey</span></span>

<span data-ttu-id="f0a37-105">**Drm \_ LASignaturePrivKey** 屬性包含用來加密 DRM 標頭的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="f0a37-105">The **DRM\_LASignaturePrivKey** property contains the private key that is used to encrypt the DRM header.</span></span>

## <a name="global-constant"></a><span data-ttu-id="f0a37-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="f0a37-106">Global Constant</span></span>

<span data-ttu-id="f0a37-107">g \_ wszWMDRM \_ LASignaturePrivKey</span><span class="sxs-lookup"><span data-stu-id="f0a37-107">g\_wszWMDRM\_LASignaturePrivKey</span></span>

## <a name="data-type"></a><span data-ttu-id="f0a37-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="f0a37-108">Data Type</span></span>

<span data-ttu-id="f0a37-109">**WMT \_ 類型 \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="f0a37-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="f0a37-110">備註</span><span class="sxs-lookup"><span data-stu-id="f0a37-110">Remarks</span></span>

<span data-ttu-id="f0a37-111">這個屬性可以使用 [**IWMDRMWriter：： GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) 方法產生。</span><span class="sxs-lookup"><span data-stu-id="f0a37-111">This property can be generated using the [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) method.</span></span> <span data-ttu-id="f0a37-112">這個屬性應該只保留內容建立者知道的秘密。</span><span class="sxs-lookup"><span data-stu-id="f0a37-112">This property should remain a secret known only by the content creator.</span></span> <span data-ttu-id="f0a37-113">您可以使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 方法來設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="f0a37-113">This property can be set with the [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) method.</span></span> <span data-ttu-id="f0a37-114">讀取器物件無法存取它。</span><span class="sxs-lookup"><span data-stu-id="f0a37-114">It is not accessible to the reader object.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0a37-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0a37-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0a37-116">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="f0a37-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




