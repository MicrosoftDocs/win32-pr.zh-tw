---
description: 指定 (B 框架) 的雙向預測框架數目。
ms.assetid: 8bd95baa-c130-4616-8ab7-7d902162e4ed
title: 'MFPKEY_NUMBFRAMES 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc3b0655a4a5e24b92f9699b198f10232de8edf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980796"
---
# <a name="mfpkey_numbframes-property"></a>MFPKEY \_ NUMBFRAMES 屬性

指定 (B 框架) 的雙向預測框架數目。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCNumBFrames

## <a name="data-type"></a>資料類型

VT-I4

## <a name="default-value"></a>預設值

0

## <a name="remarks"></a>備註

根據預設，Windows Media 視訊9只會使用 intraframes (的畫面格) ，也稱為主要畫面格或錨定框架，其為完整編碼的畫面格，以及 (P 框架) 的預測性框架，其編碼為與上一個 I 框架的差異。 B 框架與 P 框架不同，因為它們會儲存與上一個框架之間的差異，以及與下列框架之間的差異。

當您將編解碼器設定為使用 B 型框架時，它會在 I 或 P 類型的每一對畫面格之間使用指定的 B 框架數目。

例如，如果沒有 B 框架的框架序列是 "IPPPPPPPPI"，則具有兩個 B 框架的相同序列編碼會是 "IBBPBBPBBI"。

針對大部分的內容，有一或兩個 B 框架是合適的。 以較高的資料速率而言，通常會有一個 B 框架是最佳選擇。 三個或更多很少用。

這個屬性值的有效範圍是0到7。

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

 

 




