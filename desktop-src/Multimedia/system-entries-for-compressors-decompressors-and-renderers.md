---
title: 壓縮機、Decompressors 和轉譯器的系統專案
description: 壓縮機、Decompressors 和轉譯器的系統專案
ms.assetid: b27bbd5b-a218-49bb-b179-b24ce39869a1
keywords:
- Windows (VFW) 的影片、壓縮程式系統專案
- 適用于 Windows) 的 VFW (影片、壓縮程式系統專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b46d9c6fd8974511698bcb687c580e68be3757ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675067"
---
# <a name="system-entries-for-compressors-decompressors-and-renderers"></a>壓縮機、Decompressors 和轉譯器的系統專案

系統會使用登錄中的專案來尋找 BC-VCM-LVM-HYPERV 驅動程式。 這些專案的格式為 2 4 個字元的代碼，並以句號分隔。 前四個字元的程式碼是由系統所定義，而且可以是下列其中一項：



| 四個字元的程式碼 | Description                               |
|---------------------|-------------------------------------------|
| 程式              | 識別壓縮機和 decompressors。 |
| VIDS              | 識別影片資料流程轉譯器。        |
| "TXTS"              | 識別文字資料流程轉譯器。         |
| "AUDS"              | 識別音訊資料流程處理常式。         |



 

自訂轉譯器可以定義自己的四個字元的代碼。

第二個四個字元的程式碼是由驅動程式所定義。 一般來說，第二個四個字元的程式碼會對應至驅動程式可處理的資料類型。

開啟 BC-VCM-LVM-HYPERV 驅動程式時，應用程式會指定驅動程式的類型，以及它所需的資料處理程式類型。 一般而言，這是來自資料流程標頭的資訊。 系統會嘗試開啟指定的資料處理程式，但如果失敗，系統就會在登錄中搜尋具有必要處理常式的驅動程式。

搜尋驅動程式時，系統會嘗試比對驅動程式類型和資料處理程式所指定的四個字元碼與驅動程式專案中所指定的代碼。 例如，如果應用程式指定了壓縮程式 MSSQ，系統就會在登錄中搜尋驅動程式專案程式. MSSQ。 如果找不到相符項，則會開啟對應至驅動程式類型的每個驅動程式，並找出可處理您應用程式所指定之資料類型的驅動程式。 在上述範例中，如果系統找不到程式 MSSQ，則會以 "程式" 四個字元的程式碼開啟所有驅動程式，並找出可處理資料的驅動程式。

 

 




