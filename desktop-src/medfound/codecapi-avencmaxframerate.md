---
description: 設定要送入編碼器的影片畫面最大即時輸入速率。
ms.assetid: ACBE8799-A81C-44C3-B985-88ADFB1E51B4
title: 'CODECAPI_AVEncMaxFrameRate 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb4202dd2079cc013560947ef11581cdb24b92ad0aaaf544e12923d5e46b319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974927"
---
# <a name="codecapi_avencmaxframerate-property"></a>CODECAPI \_ AVEncMaxFrameRate 屬性

設定要送入編碼器的影片畫面最大即時輸入速率。

## <a name="data-type"></a>資料類型

**ULONGULONG** (VT \_ UI8) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncMaxFrameRate**

## <a name="remarks"></a>備註

這個屬性可讓呼叫者指定將影片畫面送入編碼器的最大即時輸入速率。 這可讓編碼器指出處理傳入畫面所需的速率。 這對於根據來源影片的解析度和畫面播放速率，將本身設為特定電源狀態設定的編碼器很有用。

畫面播放速率以比例表示。 屬性值的上方32位包含分子，而較低的32位則包含分母。 例如，如果畫面播放速率是每秒30個畫面格 (fps) ，則比率為30/1。 如果畫面播放速率是 29.97 fps，則比率為 30000/1001。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

