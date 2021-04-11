---
description: .
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: 將沒有回應的服務降至最低的最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e1fbad7fe60c4165ebb97847c303482314f68e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852479"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a>將沒有回應的服務降至最低的最佳作法

## <a name="affected-platform"></a>受影響的平臺

 **用戶端** -windows Vista \| windows 7  

## <a name="description"></a>Description

沒有回應的服務可能會導致超時、終止會話，甚至遺失資料。 採用最佳作法可大幅減少沒有回應的服務發生。

## <a name="best-practices"></a>最佳做法

請確定您的應用程式及其所有相依的服務和驅動程式都會回應系統電源和關機通知。

-   所有應用程式都應該立即和適當地回應，以關閉指出正在進行關機的訊息，例如 WM \_ QUERYENDSESSION 和 wm \_ ENDSESSION。
-   所有服務都應該立即回應 SCM 關機通知。 如果無法這麼做，電腦會將它們視為沒有回應，並起始20秒的時間，並將其停止，以開啟遺失資料的可能性。 這也增加了20秒的時間，關閉電腦關機的關機時間。
-   具有核心設備磁碟機相依性的所有服務都應該立即和適當地回應，以 \_ \_ 在其 DispatchShutdown 常式中 IRP MJ 關閉通知。

## <a name="links-to-other-resources"></a>其他資源的連結

<dl>

[Windows Performance Toolkit](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 



