---
description: CounterType 限定詞包含 Win32 PerfRawData 類別中屬性之屬性計數器類型的整數值 \_ 。 CookingType 包含 Win32 PerfFormattedData 類別中屬性公式類型的常數 \_ 。
ms.assetid: aa79fcdb-503f-4928-b2b7-f07baeaf9fb5
ms.tgt_platform: multiple
title: CounterType 辨識符號
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 883ee7aa2f230756d62294d46e6402fe7f962d4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982353"
---
# <a name="countertype-qualifier"></a>CounterType 辨識符號

**CounterType** 限定詞包含 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)類別中屬性之屬性計數器類型的整數值。 **CookingType** 包含 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)類別中屬性公式類型的常數。

如需詳細資訊和依函數的計數器類型細目，請參閱 [計數器類型](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))。



| CounterType | CookingType                              |
|-------------|------------------------------------------|
| 0           | 性能 \_ 計數器 \_ RAWCOUNT \_ HEX             |
| 256         | 性能 \_ 計數器 \_ 大型 \_ RAWCOUNT \_ HEX      |
| 2816        | 性能 \_ 計數器 \_ 文字                      |
| 65536       | 性能 \_ 計數器 \_ RAWCOUNT                  |
| 65792       | 性能 \_ 計數器 \_ 大型 \_ RAWCOUNT           |
| 73728       | 效能 \_ 雙重 \_ 原始                        |
| 4195328     | 性能 \_ 計數器 \_ DELTA                     |
| 4195584     | 性能 \_ 計數器 \_ 大型 \_ 差異              |
| 4260864     | 效能 \_ 範例 \_ 計數器                    |
| 4523008     | 性能 \_ 計數器 \_ QUEUELEN \_ 類型            |
| 4523264     | 性能 \_ 計數器 \_ 大型 \_ QUEUELEN \_ 類型     |
| 5571840     | 性能 \_ 計數器 \_ 100ns \_ QUEUELEN \_ 類型     |
| 6620416     | 性能 \_ 計數器 \_ OBJ \_ TIME \_ QUEUELEN \_ 類型 |
| 272696320   | 性能 \_ 計數器 \_ 計數器                   |
| 272696576   | 性能 \_ 計數器 \_ 大量 \_ 計數               |
| 537003008   | 效能 \_ 原始 \_ 分數                      |
| 541132032   | 性能 \_ 計數器 \_ 計時器                     |
| 541525248   | 效能 \_ 精確度 \_ 系統 \_ 計時器           |
| 542180608   | 效能 \_ 100NSEC \_ 計時器                     |
| 542573824   | 效能 \_ 精確度 \_ 100ns \_ 計時器            |
| 543229184   | 效能 \_ OBJ \_ 時間 \_ 計時器                   |
| 543622400   | 效能 \_ 精確度 \_ 物件 \_ 計時器           |
| 549585920   | 效能 \_ 範例 \_ 分數                   |
| 557909248   | 性能 \_ 計數器 \_ 計時器 \_ 清單                |
| 558957824   | 效能 \_ 100NSEC \_ 計時器 \_ 清單                |
| 574686464   | 性能 \_ 計數器 \_ 多重 \_ 計時器              |
| 575735040   | 效能 \_ 100NSEC \_ 多重 \_ 計時器              |
| 591463680   | 性能 \_ 計數器 \_ 多重 \_ 計時器 \_ 清單         |
| 592512256   | 效能 \_ 100NSEC \_ 多重 \_ 計時器 \_ 清單         |
| 805438464   | 效能 \_ 平均 \_ 計時器                     |
| 807666944   | 效能 \_ 經過 \_ 時間                      |
| 1073742336  | 性能 \_ 計數器 \_ NODATA                    |
| 1073874176  | 效能 \_ 平均 \_ 大量                      |
| 1073939457  | 效能 \_ 範例 \_ 基底                       |
| 1073939458  | 效能 \_ 平均 \_ 基底                      |
| 1073939459  | 性能 \_ 原始 \_ 基底                          |
| 1073939712  | 效能 \_ 精確度 \_ 時間戳記               |
| 1073939715  | 效能 \_ 大型 \_ 原始 \_ 基底                   |
| 1107494144  | 性能 \_ 計數器 \_ 多個 \_ 基底               |
| 2147483648  | 性能 \_ 計數器 \_ 長條圖 \_ 類型           |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WMI 效能類別專用的限定詞](qualifiers-specific-to-wmi-performance-classes.md)
</dt> </dl>

 

