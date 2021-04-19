---
description: 建立可搭配網路監視器的捕獲篩選是五個步驟的程式。
ms.assetid: 04be791c-43c5-44c2-8ab0-799a99974bf6
title: 建立監視捕獲篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097a8276bd6a1f311b343787b3f06175d9b7091f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986917"
---
# <a name="creating-a-monitor-capture-filter"></a>建立監視捕獲篩選

建立可搭配網路監視器的捕獲篩選是五個步驟的程式：

-   [設定 Etype 或 SAP 篩選器](writing-etypesap-filter-portion.md)
-   [寫入 ADDRESSTABLE 篩選](writing-addresstable-filter-portion.md)
-   [撰寫 PATTERNMATCH 篩選](writing-the-patternmatch-filter.md)
-   [裁剪框架](clipping-a-frame.md)
-   [執行捕獲篩選器程式碼](implementing-the-capture-filter-code.md)

「 [*捕獲篩選*](c.md) 」是一系列 NPP BLOB 的新增專案，可選取要傳回給監視器的畫面。 如果監視未改變 NPP BLOB，則 NPP 會進入混合模式，並將所有網路流量傳送至監視器。 如果 NPP 可以減少傳至驅動程式的資料，就能發揮最高效率，因此監視器應該建立一個 capture 篩選器。 監視會藉由在 [DoConfigure](imonitor-doconfigure.md) 函式的呼叫中寫入 NPP BLOB 來設定其捕捉篩選。 然後，MCSVC 會使用 NPP BLOB 來呼叫 NPP。 如需有關 capture 篩選器、NPPs 上的[網路封包提供者](network-packet-providers.md)，以及 blob 函式上[網路監視器 blob](network-monitor-blobs.md)的詳細資訊，請參閱「取得[篩選](capture-filters.md)」。

 

 



