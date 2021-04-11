---
title: DRM_KeyID
description: DRM \_ KeyID 屬性包含金鑰識別碼。
ms.assetid: 90406809-76d9-4559-afe8-6812efbc1477
keywords:
- DRM_KeyID windows Media 格式
topic_type:
- apiref
api_name:
- DRM_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a60afa330a7cf967b42a4d06009d9c921d8f56
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023074"
---
# <a name="drm_keyid"></a>DRM \_ KeyID

**DRM \_ KeyID** 屬性包含金鑰識別碼。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ KeyID

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ 字串**

## <a name="remarks"></a>備註

只有 DRM 版本7內容有此屬性。 您可以使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 來設定它，也可以使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)來取出。 您可以使用 [**DRM \_ DRMHeader \_ KeyID**](drm-drmheader-keyid.md)來取出相同的檔案屬性。

金鑰識別碼會與金鑰種子搭配使用，以建立用來加密和解密檔案的內容金鑰。 寫入器應用程式會使用金鑰識別碼來加密檔案，然後將金鑰識別碼儲存在檔案標頭中。 當播放程式應用程式要求檔案的授權時，DRM 元件會將金鑰識別碼 (以及 DRM 標頭的其餘部分傳送) 至授權伺服器。 具有秘密金鑰種子的授權伺服器會使用它和金鑰識別碼來建立檔案的金鑰，然後將它插入授權，以及將套用至該檔案的各種許可權。

通常會搭配許多金鑰識別碼使用一個金鑰種子。 金鑰種子是唯一由內容建立者和授權散發者共用的秘密。 金鑰識別碼是由 DRM 用戶端應用程式使用，並以純文字儲存在 DRM 標頭中。

這個屬性與 [**DRM \_ DRMHeader \_ KeyID**](drm-drmheader-keyid.md)相同。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




