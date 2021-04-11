---
title: 中繼資料 (instrumentationManifest) 元素
description: 包含您可以在其他資訊清單中參考的全域值。
ms.assetid: 5bf3bb1e-47c9-4d6e-86e3-3316e21b76b3
keywords:
- 中繼資料元素 EventLog
topic_type:
- apiref
api_name:
- metadata
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c14dc8772dee66fcce9ff07e9918c11b463aa414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093880"
---
# <a name="metadata-instrumentationmanifest-element"></a>中繼資料 (instrumentationManifest) 元素

包含您可以在其他資訊清單中參考的全域值。 如需範例，請參閱 Windows SDK 的 Include 資料夾中包含的 Winmeta.xml 檔案 \\ 。

``` syntax
<xs:element name="metadata"
    type="MetadataType"
 />
```

**中繼資料** 元素是由 [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md)元素所定義。

## <a name="remarks"></a>備註

雖然您可以建立包含中繼資料區段的資訊清單，但服務將不會使用它。服務唯一可辨識的中繼資料是 Winmeta.xml 檔案中找到的中繼資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**父元素**
</dt> <dt>

[**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md)
</dt> </dl>

 

 





