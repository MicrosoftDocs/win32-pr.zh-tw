---
title: 遠端桌面服務中背景工作的指導方針
description: 若要讓所有使用者都能發揮最大的 CPU 可用性，請在遠端桌面服務環境中執行時停用背景工作，或建立不需耗用大量資源的有效率背景工作。
ms.assetid: c3688319-dbe7-4be5-8895-622a8f8797d2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b93169b248fb086b7ccad88aa57c0feae171f91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969645"
---
# <a name="guidelines-for-background-tasks-in-remote-desktop-services"></a>遠端桌面服務中背景工作的指導方針

背景工作—當應用程式的訊息迴圈閒置時所執行的工作，會提供在單一使用者環境中處理低優先順序工作的機制。 不過，在遠端桌面服務環境中，一位使用者的背景工作會與另一個使用者的前景工作競爭 CPU 週期。 當多個使用者同時執行前景和背景工作時，CPU 需求遠高於所有使用者只執行前景工作。 若要讓所有使用者都能發揮最大的 CPU 可用性，請在遠端桌面服務環境中執行時停用背景工作，或建立不需耗用大量資源的有效率背景工作。

如需詳細資訊，請參閱偵測 [遠端桌面服務環境](detecting-the-terminal-services-environment.md)。 偵測遠端桌面服務環境之後，您可以使用您用來管理工作的一組相同 Api 來停用或重新設定應用程式的背景工作。

 

 




