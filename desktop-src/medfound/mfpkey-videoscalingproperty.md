---
description: 指定編解碼器是否會使用影片調整優化。
ms.assetid: a21d0100-e020-4e74-b8e3-bb7071194828
title: 'MFPKEY_VIDEOSCALING 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 555cec22533b7817c509d5419391039b10c92576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848723"
---
# <a name="mfpkey_videoscaling-property"></a>MFPKEY \_ VIDEOSCALING 屬性

指定編解碼器是否會使用影片調整優化。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCVideoScaling

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

0

## <a name="remarks"></a>備註

影片調整是一種可感知的優化，可改善以低位費率編碼的視覺效果品質。 影片調整優化可減少發音構件，但可能會犧牲影像詳細資料。 這項優化會影響編碼影片的 luma 範圍（如下所述），但不會影響輸出影片的實體解析度。

這個屬性可以設定為下列其中一個值。



| 值 | 描述                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------|
| 0     | 不會使用影片縮放。                                                                                       |
| 1     | 編碼器將使用保守的視頻調整優化。 Luma 範圍將會從 0 ... 255 調整為 26 ... 229。 |
| 2     | 編碼器將使用主動式的視頻調整優化。 Luma 範圍將會從0到255的範圍調整為 ... 224。   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




