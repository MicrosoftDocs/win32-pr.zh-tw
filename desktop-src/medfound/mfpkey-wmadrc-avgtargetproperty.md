---
description: 指定輸出音訊內容所需的平均音量層級。
ms.assetid: 2e59537f-ee14-4186-b312-297225e91120
title: 'MFPKEY_WMADRC_AVGTARGET 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c1cdd3143d7ca91be3856c9eaf3b7daecbfd80bff53fbd36c20c830dcb64e1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887608"
---
# <a name="mfpkey_wmadrc_avgtarget-property"></a>MFPKEY \_ WMADRC \_ AVGTARGET 屬性

指定輸出音訊內容所需的平均音量層級。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMADRCAverageTarget

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

請參閱＜備註＞。

## <a name="remarks"></a>備註

您可以針對動態範圍控制項的目的，在解碼器上設定此值，但只有在已設定 [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) 屬性時，才會有作用。

> [!Note]  
> 不建議設定平均目標值。 調整平均值不會影響高音和音效之間的差異。 相反地，它會剪下或提高整體平均量，而這可能會在播放期間造成不適當的失真。

 

如果您在未設定此屬性時，從編碼器要求動態範圍控制，則編解碼器會計算預設值。

您可以使用 [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md) 和 [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md) 屬性來計算這個屬性的適當值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




