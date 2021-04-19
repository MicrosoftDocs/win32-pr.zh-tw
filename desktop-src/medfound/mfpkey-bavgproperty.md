---
description: 以毫秒為單位，以毫秒為單位，指定受限制的變數位速率 (VBR) 資料流程的平均位元速率 (由 MFPKEY \_ RAVG) 指定。
ms.assetid: 7eabceb5-976e-4ebc-9042-9c203044634c
title: 'MFPKEY_BAVG 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f2cc9984b803fc37c84fee032f95098c52a9b47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983606"
---
# <a name="mfpkey_bavg-property"></a>MFPKEY \_ BAVG 屬性

以毫秒為單位，以毫秒為單位，指定受限制的變數位速率 (VBR) 資料流程的平均位元速率 (由 [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)) 指定。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCBAvg

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

沒有預設值，但編解碼器會根據其他受限制的 VBR 設定來計算適當的值。

## <a name="remarks"></a>備註

此值是由編解碼器在最終編碼傳遞之後計算。 在編碼完成之前，您不應該查詢此值。 編解碼器會將此值的要求視為編碼會話的信號來解讀;您處理的下一個範例會被視為新會話的開頭。

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

 

 




