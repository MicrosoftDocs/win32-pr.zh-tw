---
title: 裝置類型
description: 裝置類型
ms.assetid: 6556fa6a-5906-4afb-ab7d-ef41a0e22d13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27ed77debb663a1d90e03512832ca83e6e276d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674844"
---
# <a name="device-types"></a>裝置類型

MCI 會辨識出一組基本的 *裝置類型*。 裝置類型是共用通用命令集的一組 MCI 驅動程式，可用來控制類似的多媒體裝置或資料檔案。 許多 MCI 命令（例如 [**open**](open.md) ([**MCI \_ 開啟**](mci-open.md)) ）都會要求您指定裝置類型。

下表列出已定義的裝置類型。 目前的 MCI 執行包含這些裝置子集的命令集。



| 裝置類型      | 常數                      | 描述                                      |
|------------------|-------------------------------|--------------------------------------------------|
| **cdaudio**      | MCI \_ DEVTYPE \_ CD \_ 音訊       | CD 音訊播放機                                  |
| **Dat**          | MCI \_ DEVTYPE \_ DAT             | 數位音訊磁帶播放機                        |
| **digitalvideo** | MCI \_ DEVTYPE \_ 數位 \_ 影片  | 視窗中的數位影片 (非 GDI 型)         |
| **其他**        | MCI \_ DEVTYPE \_ 其他           | 未定義的 MCI 裝置                             |
| **覆蓋**      | MCI \_ DEVTYPE 重迭 \_         | 在視窗中將裝置 (類比影片重迭)         |
| **掃描器**      | MCI \_ DEVTYPE \_ 掃描器         | 影像掃描器                                    |
| **排序器**    | MCI \_ DEVTYPE \_ SEQUENCER       | MIDI sequencer                                   |
| **錄影機**          | MCI \_ DEVTYPE \_ VCR             | 影片-卡帶錄製器或播放機                |
| **videodisc**    | MCI \_ DEVTYPE \_ VIDEODISC       | Videodisc player                                 |
| **waveaudio**    | MCI \_ DEVTYPE \_ 波形 \_ 音訊 | 播放數位化波形檔案的音訊裝置 |



 

在本檔中，裝置類型的名稱為粗體。 裝置類型名稱會與命令字串介面一起使用。 裝置類型常數可搭配命令訊息介面使用。

 

 




