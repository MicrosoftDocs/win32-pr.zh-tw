---
description: 以品質為基礎的變數位元速率 (VBR) 音訊串流，指定每秒的平均位元組數。
ms.assetid: dcee969a-617e-4045-a468-8158afb06356
title: 'MFPKEY_WMAENC_AVGBYTESPERSEC 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ef88b9ea0cf46829a33cb7b9901c7c9f844c1e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512632"
---
# <a name="mfpkey_wmaenc_avgbytespersec-property"></a>MFPKEY \_ WMAENC \_ AVGBYTESPERSEC 屬性

以品質為基礎的變數位元速率 (VBR) 音訊串流，指定每秒的平均位元組數。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMACAvgBytesPerSecond

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="remarks"></a>備註

在串流編碼之後，您可以從解碼器取得此值。

音訊解碼器需要此值才能正確解壓縮內容。

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

 

 




