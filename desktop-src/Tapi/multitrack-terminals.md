---
description: TAPI 3.1 引進 multitrack 終端機的概念，基本上，終端機是 &0034 的集合 \# ; 追蹤&\# 0034; 端子。
ms.assetid: 8dd6f792-a29e-40fd-9f5b-ee5525028c2e
title: Multitrack 終端機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9e5f9c6d614308370b3d9211f578d5fcb2650bd3c5ba7f8a81dbc981ad2687
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575518"
---
# <a name="multitrack-terminals"></a>Multitrack 終端機

TAPI 3.1 引進 multitrack 終端機的概念，而終端機其實是「追蹤」終端機的集合。 Multitrack 終端機可讓程式設計人員在多個媒體串流參與通訊會話的情況下，讓程式設計人員的負載更輕鬆。

檔案 [記錄終端](file-playback-terminal-and-file-recording-terminal.md) 機即為 multitrack 終端機的範例。 它是由「追蹤」所組成，其中每個「追蹤」是對應至所記錄檔案中資料流程的終端機。

[追蹤終端](track-terminals.md)機可以是另一個 multitrack 終端機或單一追蹤終端機。 單一追蹤終端機是沒有任何追蹤終端機的終端機。 單一追蹤終端機是此單字的 TAPI 3 意義的終端機。

如需 multitrack 終端機的詳細資訊，請參閱下列主題：

-   [關於 Multitrack 終端機](about-multitrack-terminals.md)
-   [預設終端機選取機制](default-terminal-selection-mechanism.md)
-   [手動選取終端機](manual-terminal-selection.md)
-   [使用 Multitrack 終端機和預設選取機制](using-multitrack-terminals-and-the-default-selection-mechanism.md)

 

 



