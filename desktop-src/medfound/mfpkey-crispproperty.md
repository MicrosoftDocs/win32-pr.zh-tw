---
description: 指定以數位表示的方式來表示動畫平滑與影像品質的編解碼器輸出之間的取捨。
ms.assetid: 63915450-71c5-4097-91d7-5817249c1cda
title: 'MFPKEY_CRISP 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ff20b37bcedf3995ec3e16178b823c40b352ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692420"
---
# <a name="mfpkey_crisp-property"></a>MFPKEY \_ 清晰屬性

指定以數位表示的方式來表示動畫平滑與影像品質的編解碼器輸出之間的取捨。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCCrisp

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

75

## <a name="remarks"></a>備註

這個整數值的範圍可以從0到100。 值愈高，編解碼器將會針對個別畫面格的影像品質優化編碼，這通常會減少動畫平滑。

這個屬性應該只針對常數位速率 (CBR) 編碼進行設定。 變數位元速率 (VBR) 編碼的優化會以不同的方式運作。

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

 

 




