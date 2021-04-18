---
description: 指定音訊解碼器將使用的動態範圍控制模式。
ms.assetid: 0dbe0c40-39ac-4c1b-9da2-9b142b5bb0eb
title: 'MFPKEY_WMADEC_DRCMODE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb612e08ff8bd799ec94faae68763f04db8ad052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191789"
---
# <a name="mfpkey_wmadec_drcmode-property"></a>MFPKEY \_ WMADEC \_ DRCMODE 屬性

指定音訊解碼器將使用的動態範圍控制模式。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMACDRCSetting

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

0

## <a name="remarks"></a>備註

這個整數值的範圍是從0到2。 值愈大，未壓縮音訊輸出的動態範圍就越小。 0值表示編解碼器不執行任何動態範圍控制，也就是說，編解碼器不會改變編碼內容的固有動態範圍。

如果此值設為1或2，則編解碼器會使用下列屬性來判斷所需的動態範圍控制項：

-   [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md)
-   [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md)
-   [MFPKEY \_ WMADRC \_ AVGTARGET](mfpkey-wmadrc-avgtargetproperty.md)
-   [MFPKEY \_ WMADRC \_ PEAKTARGET](mfpkey-wmadrc-peaktargetproperty.md)

如果您未提供目標值，編解碼器將會提供它自己的值。

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

 

 




