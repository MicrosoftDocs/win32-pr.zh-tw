---
description: ICE95 會檢查 Control table 和 BBControl 資料表，以確認該佈告欄控制項符合所有公告欄。
ms.assetid: 8ba73536-65a5-4658-846c-76356f16b81c
title: ICE95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f0f7d44554385c33648036f314406971193afc079b5aa8e72cf595695797ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315258"
---
# <a name="ice95"></a>ICE95

ICE95 會檢查 [Control table](control-table.md) 和 [BBControl 資料表](bbcontrol-table.md) ，以確認該佈告欄控制項符合所有公告欄。

## <a name="result"></a>結果

如果下列任何一項為 true，表示佈告欄控制項無法符合佈告欄。 ICE95 會張貼下列警告。



| ICE95 警告                                                                                                                                                                                                              | Description                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| BBControl 專案 ' \[ 1 \] . \[[BBControl] 資料表中的 [2] 不 \] 符合控制資料表中的所有佈告欄控制項。 X 座標超過最小佈告欄控制項寬度% s 的界限                   | 控制項的 X 座標在佈告欄的寬度之外。                          |
| BBControl 專案 ' \[ 1 \] . \[[BBControl] 資料表中的 [2] 不 \] 符合控制資料表中的所有佈告欄控制項。 Y 座標超過最小的佈告欄控制項高度% s 的界限                  | 控制項的 Y 座標位於佈告欄的底部。                           |
| BBControl 專案 ' \[ 1 \] . \[[BBControl] 資料表中的 [2] 不 \] 符合控制資料表中的所有佈告欄控制項。 X 座標和寬度組合在一起，超過最小的佈告欄控制項寬度% s   | 控制項的 X 座標加上控制項的寬度，在佈告欄的寬度之外。 |
| BBControl 專案 ' \[ 1 \] . \[[BBControl] 資料表中的 [2] 不 \] 符合控制資料表中的所有佈告欄控制項。 Y 座標和高度組合在一起，超過最小的佈告欄控制項高度% s | 控制項的 Y 座標加上控制項的高度，在佈告欄的底部。 |



 

## <a name="example"></a>範例

ICE95 會報告下列範例警告：

``` syntax
The BBControl item 'billboard1.bbcontrol1' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate exceeds the boundary of the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol2' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate exceeds the boundary of the minimum billboard control height 100
The BBControl item 'billboard1.bbcontrol3' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate and the width combined together exceeds the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol4' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate and the height combined together exceeds the minimum billboard control height 100
```

控制資料表 (部分)  (部分) 



| 控制  | 類型      | 寬度 | 高度 |
|----------|-----------|-------|--------|
| control1 | 廣告 牌 | 300   | 100    |
| Control2 | 廣告 牌 | 100   | 300    |



 

[BBControl 資料表](bbcontrol-table.md)



| 廣告 牌\_ | BBControl  | X   | Y   | 寬度 | 高度 |
|-------------|------------|-----|-----|-------|--------|
| billboard1  | bbcontrol1 | 200 | 0   | 100   | 100    |
| billboard1  | bbcontrol2 | 0   | 200 | 100   | 100    |
| billboard1  | bbcontrol3 | 50  | 0   | 100   | 50     |
| billboard1  | bbcontrol4 | 0   | 50  | 50    | 100    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



