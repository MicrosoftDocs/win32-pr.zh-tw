---
title: DRM_KeySeed
description: DRM \_ KeySeed 屬性包含將與 KeyID 搭配使用來建立金鑰的金鑰種子。
ms.assetid: 38613d50-89c2-4422-9265-5e89de030ae9
keywords:
- DRM_KeySeed windows Media 格式
topic_type:
- apiref
api_name:
- DRM_KeySeed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 698db5fe5a1123af0a7b4623d304bf0569bbf253
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106993726"
---
# <a name="drm_keyseed"></a>DRM \_ KeySeed

**DRM \_ KeySeed** 屬性包含將與 KeyID 搭配使用來建立金鑰的金鑰種子。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ KeySeed

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ 字串**

## <a name="remarks"></a>備註

您可以使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)來設定這個屬性。 讀取器物件無法存取它。

金鑰種子通常用來保護多個檔案或檔案集，例如授權伺服器所發行的所有檔案，或特定演出者可能的所有檔案。 不過，KeyID 對每個檔案而言是唯一的。

金鑰種子必須保留只在內容建立者與授權散發者之間共用的秘密。 此值不會儲存在 DRM 標頭中，也不需要它，也不能存取 DRM 播放機應用程式。

您可以使用 [**IWMDRMWriter：： GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) 方法或任何其他適當的方式來產生新的金鑰種子。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM 屬性**](drm-properties.md)
</dt> </dl>

 

 




