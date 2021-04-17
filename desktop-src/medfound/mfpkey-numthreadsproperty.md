---
description: 指定編碼器將使用的執行緒數目。
ms.assetid: 2f463cba-2512-455d-9ce1-8797682d4d67
title: 'MFPKEY_NUMTHREADS 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c93f6d38e3bb79bbb692f9bec1b1dc0edb232d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513104"
---
# <a name="mfpkey_numthreads-property"></a>MFPKEY \_ NUMTHREADS 屬性

指定編碼器將使用的執行緒數目。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCNumThreads

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

1

## <a name="remarks"></a>備註

此值旨在將編碼劃分成多個執行緒，以利用具有多個處理器的電腦。 相較于單一執行緒，將編碼工作分割成多個執行緒可能會導致品質稍微降低。

針對 (wmvencod.dll) Windows XP 和 Windows Vista 發行的影片編碼器，這個屬性應該設定為1、2或4。 其他值將會四捨五入。

針對與 Windows 7 一起發行的影片編碼器 (wmvencod.dll) ，此屬性應該設定為1、2、4或8。 其他值將會四捨五入。

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

 

 




