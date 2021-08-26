---
description: 指定以數位表示的方式來表示動畫平滑與影像品質的編解碼器輸出之間的取捨。
ms.assetid: 63915450-71c5-4097-91d7-5817249c1cda
title: 'MFPKEY_CRISP 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 177ae5e9d1c8a9aba359000e04483c8e45c44f823c9db924155dd5ef3d5989a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954258"
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
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




