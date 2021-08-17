---
title: 語音總機
description: 針對稱為「執行中狀態」的連接狀態，除非發生錯誤，否則通知處理常式不需要採取任何動作。
ms.assetid: 3f5ea9e0-f75a-4b02-a0dc-86cb5012c242
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f526dcd0cd52eaa15929f970debe3ba78788fdb7525e734ee2e26e348b32552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790992"
---
# <a name="informational-notifications"></a>語音總機

針對稱為「執行中狀態」的 [連接狀態](connection-states.md) ，除非發生錯誤，否則通知處理常式不需要採取任何動作。 執行狀態會在 RAS 處理的連接作業部分期間發生，例如連接到必要的裝置、驗證使用者，以及等待遠端伺服器的回呼。 通知只是用戶端的進度報表。

用戶端可以選擇將這些語音總機傳遞給使用者。 在某些執行狀態下，用戶端可能會想要顯示其他資訊。 例如，接收 RASCS ConnectDevice 通知的通知處理常式 \_ 可以呼叫 [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) 函式，以取得所連接裝置的名稱和類型。 另一個範例是用戶端收到 RASCS \_ 投射的通知。 當連接作業的 RAS 投影階段已完成時，就會發生這種情況。 用戶端可以呼叫 [**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) 函數，以取得有關投射的其他資訊。 用戶端可以使用這項資訊，通知使用者此連線可以使用的網路通訊協定。

您應該避免撰寫相依于特定告知性狀態之順序或出現位置的程式碼，因為這可能會因平臺而異。

 

 




