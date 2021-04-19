---
description: 指定編解碼器應減少影片有效色彩範圍的程度。
ms.assetid: 7227957b-59c9-4dd9-ad2b-a383e888cd46
title: 'MFPKEY_RANGEREDUX 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ec326e5d21a72792aab38f08d8c8c9207ab867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988742"
---
# <a name="mfpkey_rangeredux-property"></a>MFPKEY \_ RANGEREDUX 屬性

指定編解碼器應減少影片有效色彩範圍的程度。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCRangeRedux

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

0

## <a name="remarks"></a>備註

範圍縮減：指定編解碼器應減少影片 luma 和色度範圍的程度。 減少範圍可減少編碼的影片畫面大小，但也會降低影片的色彩細節。

縮小範圍的方式包括：編碼期間的縮減，以及解碼期間的擴充。 您可以使擴充因素與減少因數不同，但不建議在範圍重新對應很實用的大部分案例中使用。

範圍縮減和展開會在 luma 和色度通道上分開執行。 減少範圍可能是降低低位速率影片複雜性的有效方法，而不會犧牲影像詳細資料。 將全部四個值設定為8，可將 luma 和色度資訊的數量降到一半，讓更多的位被導向以保留影像詳細資料。

編解碼器可以選擇在以非常低的位元速率編碼影片時自動使用範圍減少。 將全部四個值設定為0，可完全停用範圍減少，即使是低位速率的案例也一樣。

減少色彩範圍可減少影片框架的編碼大小，但可以在已解碼的框架中引進 blurriness。

如果未設定此屬性，則編解碼器會決定是否要在編碼時間使用範圍減少。 此選項通常只會以低位費率由編解碼器選取。

這個屬性的值是四個元件的組合（以零分隔），格式為0x0M0m0N0n，其中：

-   M 是 Y 元件的編碼範圍減少因數。
-   m 是 Y 元件的解碼範圍展開因數 (通常與 M) 相同。
-   N 是 UV 元件的編碼範圍減少因數。
-   n 是 UV 元件的解碼範圍展開因數 (通常與 N) 相同。

每個因素都是從0到8的數位，其中0不是縮減或展開，而8是最大縮減或擴大。

如果您將值設定為0x00000000，則會完全停用範圍減少。

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

 

 




