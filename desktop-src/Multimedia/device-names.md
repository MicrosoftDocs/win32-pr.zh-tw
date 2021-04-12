---
title: 裝置名稱
description: 裝置名稱
ms.assetid: 0ba06439-cc33-43e1-a094-09bcc5e2f6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e516f7f8eed338067dc373f8509f46598e198c71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462469"
---
# <a name="device-names"></a>裝置名稱

針對每個裝置類型，可能會有數個 MCI 驅動程式共用命令集，但操作不同的資料格式。 為了唯一識別 MCI 驅動程式，MCI 會使用 *裝置名稱*。

裝置名稱會在 SYSTEM.INI 檔案的 \[ mci \] 區段或登錄的適當部分中識別。 此資訊可識別 Windows 的所有 MCI 驅動程式。 Mci 區段中的 \[ 專案 \] 使用下列格式：

*裝置 \_ 名稱*  =  *驅動程式 \_ 檔案名。副檔名*

下列範例顯示 SYSTEM.INI 的一般 \[ mci \] 區段：


```C++
[mci]
cdaudio=mcicda.drv 
sequencer=mciseq.drv 
waveaudio=mciwave.drv 
avivideo=mciavi.drv
```



如果使用 SYSTEM.INI 或登錄中已經存在的裝置名稱來安裝 MCI 驅動程式，系統會將整數附加至新驅動程式的裝置名稱，並建立唯一的裝置名稱。 在上述範例中，使用 "cdaudio" 裝置名稱安裝的額外驅動程式將會被指派裝置名稱 "cdaudio1"。

 

 




