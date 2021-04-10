---
description: 指定如何在移動搜尋作業中使用色彩資訊。
ms.assetid: a625b103-0a55-4268-a01a-6a464a56fec2
title: 'MFPKEY_MOTIONSEARCHLEVEL 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 231c2c0ae70466d41f4bf348ec47ee0a74cb135b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026570"
---
# <a name="mfpkey_motionsearchlevel-property"></a>MFPKEY \_ MOTIONSEARCHLEVEL 屬性

指定如何在移動搜尋作業中使用色彩資訊。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCMotionSearchLevel

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

0

## <a name="remarks"></a>備註

這個屬性可以設定為下列其中一個值。



| 值 | 使用的影片資訊                           |
|-------|--------------------------------------------------|
| 0     | 僅 Luma。                                       |
| 1     | 具有最接近整數色度的 Luma。                |
| 2     | Luma 與真實色度。                           |
| -1    | 巨大區塊-使用 true 色度的彈性。            |
| -2    | 巨大區塊-具有最接近整數色度的彈性。 |



 

根據預設，編解碼器只會在 luma 頻道中執行動作搜尋。 在移動估計中包含色度資訊可大幅提升編碼影片的品質。 使用 luma 和 true 色度的動作搜尋會產生最佳的影片品質，但最高的效能成本。 這兩個動態模式 (-1 和-2) ，而具有最接近整數色度模式的 luma，將可提供品質與效能之間合理的折衷。

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

 

 




