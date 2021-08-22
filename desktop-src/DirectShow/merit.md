---
description: '[指定值] 會定義篩選 Graph 管理員在圖形建立期間嘗試新增篩選的順序。'
ms.assetid: 9e026675-e0a9-4c82-9b57-ab0e7d9592ea
title: " (Dshow 的) "
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a55c112f1a08d63e45d5385f525371ae9642c1b01a1b4af5d7747b042efffe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073012"
---
# <a name="merit"></a>優點

[指定值] 會定義篩選 Graph 管理員在圖形建立期間嘗試新增篩選的順序。

<dl> <span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**業績 \_慣用** 的 (0x800000) 獲得 <span id="MERIT_NORMAL"></span> <span id="merit_normal"></span> **\_ 正常** 的 (0x600000) <span id="MERIT_UNLIKELY"></span> <span id="merit_unlikely"></span> 不 **\_ 太可能** 獲得 (0x400000) <span id="MERIT_DO_NOT_USE"></span> <span id="merit_do_not_use"></span> **\_ \_ 未 \_ 使用** (0x200000) 找出 <span id="MERIT_SW_COMPRESSOR"></span> <span id="merit_sw_compressor"></span> **\_ 軟體 \_ 壓縮** (0x100000) <span id="MERIT_HW_COMPRESSOR"></span> <span id="merit_hw_compressor"></span> **\_ 硬體 \_ 壓縮**
</dl>

## <a name="remarks"></a>備註

每個篩選器都是以「價值」值註冊。 當篩選圖形管理員建立圖形時，會列舉以正確媒體類型註冊的所有篩選準則。 然後，它會以最高至最低的方式來嘗試進行。  (它會使用其他準則，在具有相同相關的篩選準則之間進行選擇。 ) 它永遠不會嘗試值小於或等於 [ **\_ \_ 未 \_ 使用**] 的篩選。

永遠不會被視為一般播放的篩選準則應該 **\_ \_ 不 \_** 會有較多的考慮。 您可以使用未由此列舉定義的中繼值來註冊篩選準則，例如， **\_ 一般** 的 + 1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dshow。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[常數和 Guid](constants-and-guids.md)
</dt> <dt>

[註冊篩選準則的指導方針](guidelines-for-registering-filters.md)
</dt> <dt>

[智慧型連線](intelligent-connect.md)
</dt> </dl>

 

 




