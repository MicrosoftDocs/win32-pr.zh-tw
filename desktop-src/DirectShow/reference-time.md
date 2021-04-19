---
description: 參考 \_ 時間資料類型會定義 DirectShow 中參考時間的單位。 參考時間的每個單位為100毫微秒。
ms.assetid: 862c95bc-2e0a-42c0-b907-45f64f27bd41
title: 'REFERENCE_TIME (Strmif) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab88576f611674f5b208c5c39d328c77dcf57aec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983188"
---
# <a name="reference_time"></a>參考 \_ 時間

**參考 \_ 時間** 資料類型會定義 DirectShow 中參考時間的單位。 參考時間的每個單位為100毫微秒。


```C++
typedef LONGLONG REFERENCE_TIME;
```



## <a name="remarks"></a>備註

**參考 \_ 時間** 資料類型是64位整數。

參考時間通常是以下列其中一個基準來測量：

-   絕對時鐘時間。 在此情況下，基準將視時鐘的執行而定。 如需詳細資訊，請參閱 [參考時鐘](reference-clocks.md)。
-   相對於開始播放。

如需參考時間的詳細資訊，請參閱 [DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Strmif (包含 Dshow) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow 資料類型](directshow-data-types.md)
</dt> </dl>

 

 




