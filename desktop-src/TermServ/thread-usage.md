---
title: 執行緒使用方式
description: 您應該針對多使用者、多處理器遠端桌面服務環境，調整應用程式執行緒的使用方式並進行平衡。
ms.assetid: 88f4e61f-4a59-4a84-8dca-fdb661835b51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a3b432cf4960c6ec7a8e51b458b9f574663ffe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968016"
---
# <a name="thread-usage"></a>執行緒使用方式

執行緒提供一個便利的方式，讓應用程式能夠充分利用系統中 CPU 資源的使用，尤其是在多處理器設定中。 不過，在遠端桌面服務環境中，多個使用者可以執行多執行緒應用程式，而所有使用者的所有線程都會爭用該系統的中央 CPU 資源。 考慮到這一點，您應該針對多使用者、多處理器遠端桌面服務環境，調整應用程式執行緒的使用方式並進行平衡。 雖然使用閒置或浪費執行緒的不佳設計多執行緒應用程式可能會在用戶端電腦上順利執行，但相同的應用程式可能無法在多使用者遠端桌面服務伺服器上正常執行。

 

 




