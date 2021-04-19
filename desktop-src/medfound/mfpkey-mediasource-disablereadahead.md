---
description: 啟用或停用媒體來源的預先讀取。
ms.assetid: b2b8711f-ba63-4fba-bb88-8d254135eb21
title: 'MFPKEY_MediaSource_DisableReadAhead 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d06fe354431a24e15152268ba0ea6352e535c5e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990630"
---
# <a name="mfpkey_mediasource_disablereadahead-property"></a>MFPKEY \_ MediaSource \_ DisableReadAhead 屬性

啟用或停用媒體來源的預先讀取。



資料類型

PROPVARIANT 類型 (vt) 

PROPVARIANT 成員

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>備註

應用程式可以使用此屬性來設定某些媒體來源。 若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。 如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。

如果值為 **VARIANT \_ TRUE**，就不會在位元組資料流程中向前讀取媒體來源。 如果您打算從媒體來源讀取有限數量的資料，這項設定可以優化效能，例如，從影片檔案取得縮圖影像。

針對一般音訊/影片播放，此屬性應該設定為 **VARIANT \_ FALSE**。 預設值為 **VARIANT \_ FALSE**。

並非每個媒體來源都支援此屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 用戶端<br/> | Windows 7<br/>                                                               |
| 標頭<br/> | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




