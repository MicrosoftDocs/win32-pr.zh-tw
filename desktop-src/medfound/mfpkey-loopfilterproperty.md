---
description: 指定編解碼器是否應在編碼期間使用 in 迴圈 deblocking 篩選。
ms.assetid: 395a356a-5f58-46b4-b2ff-47f98106f487
title: 'MFPKEY_LOOPFILTER 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fbb723c4145f9769cc157d5db8eb7893d89b389
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988743"
---
# <a name="mfpkey_loopfilter-property"></a>MFPKEY \_ LOOPFILTER 屬性

指定編解碼器是否應在編碼期間使用 in 迴圈 deblocking 篩選。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCLoopFilter

## <a name="data-type"></a>資料類型

VT \_ BOOL

## <a name="remarks"></a>備註

「迴圈中」篩選器是一種在編碼和解碼期間套用的 deblocking 方法，可在編碼時間減少封鎖成品 ( 「在迴圈中」 ) ，讓未來的 P 框架和 B 框架不會將這些專案向前推進。

套用「迴圈」篩選的效果，是輸出影片畫面格中宏區塊的邊緣比較不明顯。 在此同時，影像在外觀上可能會變柔和。

雖然「迴圈中」篩選可能會導致某些框架中的影像詳細資料減少，但整體的影片品質將會明顯受益。 使用迴圈中篩選的最大缺點是額外的解碼效能成本。

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

 

 




