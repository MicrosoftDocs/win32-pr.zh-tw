---
title: DRM_Level
description: DRM \_ 層級是 Windows Media 格式 SDK 在為以 DRM 第1版保護的檔案建立本機授權時所設定的授權屬性。
ms.assetid: 05357378-4d73-48df-a3b5-bdb2c543ec66
keywords:
- DRM_Level windows Media 格式
topic_type:
- apiref
api_name:
- DRM_Level
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3177197b9c149c2fca2c7678a8fe03c6b412e2d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314349"
---
# <a name="drm_level"></a>DRM \_ 層級

**DRM \_層級** 是 Windows Media 格式 SDK 在為以 DRM 第1版保護的檔案建立本機授權時所設定的授權屬性。 它包含呼叫應用程式必須有才能存取檔案內容的安全性層級。 預設值為 150。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ 層級

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ DWORD**

## <a name="remarks"></a>備註

應用程式的 DRM 安全性層級是由它在編譯時期連結到的特定 wmstubdrm 程式庫所決定。 如需這些安全性層級的詳細資訊，請參閱 [取得所需的 DRM 程式庫](obtaining-the-required-drm-library.md)。 使用 [**IWMHeaderInfo：： SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) 可在使用 DRM 第1版保護 ASF 檔案時設定此屬性。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM 屬性**](drm-properties.md)
</dt> </dl>

 

 




