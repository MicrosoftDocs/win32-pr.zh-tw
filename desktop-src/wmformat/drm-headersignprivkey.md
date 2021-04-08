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
# <a name="drm_headersignprivkey"></a>DRM \_ HeaderSignPrivKey

**DRM \_ HeaderSignPrivKey** 屬性包含用來簽署 ASF 標頭的私密金鑰。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ HeaderSignPrivKey

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ 字串**

## <a name="remarks"></a>備註

這個屬性是使用 [**IWMDRMWriter：： GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair)產生的。 請保存此金鑰密碼，並只與授權服務共用公開金鑰。 設定此金鑰之後，DRM 元件會使用它來簽署 ASF 檔案標頭 (而不是使用數位簽章物件值（例如 DRM LASignaturePrivKey) ）簽署的 DRM 標頭 \_ 。 很明顯地， **DRM \_ HeaderSignPrivKey** 不包含在 headert 檔案中。

無法從 reader 物件存取這個屬性。 您可以使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)，從寫入器物件進行設定。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM 屬性**](drm-properties.md)
</dt> </dl>

 

 




