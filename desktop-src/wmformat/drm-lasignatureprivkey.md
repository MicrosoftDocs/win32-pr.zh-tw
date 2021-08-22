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
ms.openlocfilehash: 9354cc652bfce22183370b1183062d6cf7f27ce60b3681862f150f565d444a6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704322"
---
# <a name="drm_lasignatureprivkey"></a>DRM \_ LASignaturePrivKey

**Drm \_ LASignaturePrivKey** 屬性包含用來加密 DRM 標頭的私密金鑰。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ LASignaturePrivKey

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ 字串**

## <a name="remarks"></a>備註

這個屬性可以使用 [**IWMDRMWriter：： GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) 方法產生。 這個屬性應該只保留內容建立者知道的秘密。 您可以使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 方法來設定這個屬性。 讀取器物件無法存取它。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




