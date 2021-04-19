---
description: 以毫秒為單位，以毫秒為單位，指定受限制的變數位速率 (VBR) 資料流程的尖峰位元速率 (由 MFPKEY \_ RMAX) 指定。
ms.assetid: ef27b179-4d9b-4ce7-867a-f62b0f9b735d
title: 'MFPKEY_BMAX 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feaca172e97c27e6e8d97902fbe3c969efc933eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985367"
---
# <a name="mfpkey_bmax-property"></a>MFPKEY \_ BMAX 屬性

以毫秒為單位，以毫秒為單位，指定受限制的變數位速率 (VBR) 資料流程的尖峰位元速率 (由 [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md)) 指定。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCBMax

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

沒有預設值。

## <a name="remarks"></a>備註

您必須為尖峰限制的 VBR 編碼設定此值。 開始處理範例之後，必須等到您完成串流的編碼之後，才能查詢此值。 編解碼器會將此值的要求視為編碼會話的信號來解讀;您處理的下一個範例會被視為新會話的開頭。

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

 

 




