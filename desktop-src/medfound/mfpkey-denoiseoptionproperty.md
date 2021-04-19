---
description: 指定編解碼器是否會在編碼時使用雜訊篩選器。
ms.assetid: 9e099378-bb77-4dca-9171-7fe58e0139de
title: 'MFPKEY_DENOISEOPTION 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f318e294f69095758fe300fce19043c23cf376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974634"
---
# <a name="mfpkey_denoiseoption-property"></a>MFPKEY \_ DENOISEOPTION 屬性

指定編解碼器是否會在編碼時使用雜訊篩選器。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCDenoiseOption

## <a name="data-type"></a>資料類型

VT \_ BOOL

## <a name="default-value"></a>預設值

FALSE

## <a name="remarks"></a>備註

雜訊篩選器可以改善雜訊影片來源的品質，例如包含很多細微性或影片的電影。 此篩選準則可用於無法選擇外部前置處理的即時編碼案例中。

這項篩選器應該針對乾淨的影片來源停用，因為它可以在品質適合開始時降低影像品質。

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

 

 




