---
description: 監視器可以在僅限原生模式或混合模式中檢查畫面格。
ms.assetid: 4646f5bb-e3e3-4929-91b7-f68c5b70ccb3
title: Local-Only 和混合模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8155c968f82154712ec8926f114e63380cdb1099bf7908d5a4dde86d7646dc20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555888"
---
# <a name="local-only-and-promiscuous-modes"></a>Local-Only 和混合模式

監視器可以在僅限原生模式或混合模式中檢查畫面格。

在僅限原生模式中， (NPP) 的網路封包提供者會傳回執行監視的電腦所傳送的框架，包括導向至本機電腦的廣播和多播。 雖然受限於本機導向的框架，但原生模式也會比處理器密集。

在混合模式中，監視器也可以監看沒有導向至本機電腦或從本機電腦導向的流量。 除非監視器已指定旗標 [ \_ 不需要 MCS 建立 PMODE]，否則在 OnLoadingDLL 函式 \_ \_ \_ 中，監視器控制服務 (MCSVC) 會假設監視器在載入監視器 DLL 時需要混合模式。 [](onloadingdll.md)

 

 



