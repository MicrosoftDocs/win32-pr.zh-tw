---
description: 指定編解碼器是否應嘗試偵測出雜訊的框架邊緣並將其移除。
ms.assetid: fdb4f3a8-1447-4e1e-a208-0f9b717f7626
title: 'MFPKEY_NOISEEDGEREMOVAL 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30acd92bae7693d0714e42d6b4f832a521557bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192252"
---
# <a name="mfpkey_noiseedgeremoval-property"></a>MFPKEY \_ NOISEEDGEREMOVAL 屬性

指定編解碼器是否應嘗試偵測出雜訊的框架邊緣並將其移除。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCNoiseEdgeRemoval

## <a name="data-type"></a>資料類型

VT \_ BOOL

## <a name="default-value"></a>預設值

FALSE

## <a name="remarks"></a>備註

雜訊畫面邊緣通常是垂直的空白間隔， (從廣播電視的畫面格) 資料 VBI。 VBI 是電視框架的前21個掃描行。 這些掃描行不包含影片資料，而是包含廣播的相關資料。 當捕捉卡錄製電視信號時，通常會從框架中移除 VBI。 編解碼器所執行的雜訊邊緣偵測和更正只能更正有三個或更少的雜訊行的邊緣。 如果捕捉的影片包含三條以上的雜訊線，則用來捕捉影片的硬體有問題。

如果編解碼器設定為移除有雜訊的邊緣，則會複製與雜訊邊緣連續的線條以填滿框架。

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

 

 




