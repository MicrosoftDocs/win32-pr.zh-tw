---
title: DRM_Flags
description: '[DRM \_ 旗標] 屬性僅適用于 drm 第1版內容，以指定將包含在本機授權中的許可權。'
ms.assetid: d9a776d3-da22-4111-b1ed-e3607a5576ef
keywords:
- DRM_Flags windows Media 格式
topic_type:
- apiref
api_name:
- DRM_Flags
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f2f8eb2baa401f1bc8519da5ca555a1fe428ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932927"
---
# <a name="drm_flags"></a>DRM \_ 旗標

[ **Drm \_ 旗標** ] 屬性僅適用于 drm 第1版內容，以指定將包含在本機授權中的許可權。 許可權是使用 **WMT \_ 許可權** 列舉類型所定義的值來指定。 藉由將一個以上的值與位 **or** 運算子結合，即可選取多個值。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ 旗標

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ DWORD**

## <a name="remarks"></a>備註

存取寫入器物件的 **IWMHeaderInfo3** 介面時，您可以加入或變更此值。 在其他物件 (中繼資料編輯器、讀取器和同步讀取器) ，此值是唯讀的。 建立 DRM 第1版內容時，請使用 [**IWMHeaderInfo：： SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) 來設定此屬性。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM 屬性**](drm-properties.md)
</dt> </dl>

 

 




