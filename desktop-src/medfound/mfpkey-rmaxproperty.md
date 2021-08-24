---
description: 指定尖峰位速率（以每秒位數為單位），用於受條件約束的2傳遞變數位速率 (VBR) 播放。
ms.assetid: 51f161d2-f832-48d5-8f16-861e2a98a7f7
title: 'MFPKEY_RMAX 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e80f679d0ed1213a54a4f22bc5d8bfc79f41b93fa05c446c8b6ed0f589183b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119398398"
---
# <a name="mfpkey_rmax-property"></a>MFPKEY \_ RMAX 屬性

指定尖峰位速率（以每秒位數為單位），用於受條件約束的2傳遞變數位速率 (VBR) 播放。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCMaxBitrate

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

沒有預設值。

## <a name="remarks"></a>備註

此值代表播放的尖峰位元速率。 [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md)的值是用來根據這位速率來描述緩衝區; 實際上，條件約束的 VBR 類似于常數位元速率 (CBR) 使用此值做為位元速率。 不過，只要緩衝區增加，就可以用較低的位元速率播放受限的 VBR 資料流程。

您必須設定此值，以進行尖峰限制的雙通路 VBR 編碼。 開始處理範例之後，必須等到您完成串流的編碼之後，才能查詢此值。 編碼器會將此值的要求解讀為編碼會話結束的信號;您處理的下一個範例會被視為新會話的開頭。

通常，這個值是大於 [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)值的兩到三倍。

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

 

 




