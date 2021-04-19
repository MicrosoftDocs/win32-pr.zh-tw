---
title: DRM_DRMHeader_IndividualizedVersion
description: DRM \_ DRMHeaderIndividualizedVersion 屬性包含播放檔案所需的最小個別版本。
ms.assetid: 2ac24660-8b7a-4dba-9f9f-ad8b13a22f5c
keywords:
- DRM_DRMHeader_IndividualizedVersion windows Media 格式
topic_type:
- apiref
api_name:
- DRM_DRMHeader_IndividualizedVersion
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 167065f99a72245c6d7cc677ce24fa1ff96dec84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106966230"
---
# <a name="drm_drmheader_individualizedversion"></a>DRM \_ DRMHeader \_ IndividualizedVersion

**DRM \_ DRMHeaderIndividualizedVersion** 屬性包含播放檔案所需的最小個別版本。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ 字串**

## <a name="remarks"></a>備註

這個屬性只有 DRM 版本7內容存在。 您可以使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)來取出它。 若要使用 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 在檔案上設定個別的版本 (也稱為安全性版本) ，您必須使用 [**DRM \_ IndividualizedVersion**](drm-individualizedversion.md) 屬性。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




