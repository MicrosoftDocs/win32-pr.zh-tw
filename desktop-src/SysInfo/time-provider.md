---
description: Microsoft Windows 作業系統使用時間提供者架構，提供各種硬體裝置和網路時間通訊協定的支援。
ms.assetid: a7575373-eeda-4f2a-85e5-d1b50994e7ae
title: 時間提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67f2073e94bdf893793b4ae1df2974226aa197de4ff429be9ce8f2a2e4b5f597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117957902"
---
# <a name="time-provider"></a>時間提供者

Microsoft Windows 作業系統使用 *時間提供者* 架構，提供各種硬體裝置和網路時間通訊協定的支援。 輸入時間提供者會從硬體或網路取得準確的時間戳記，而輸出時間提供者則會提供時間戳記給網路上的其他用戶端。

時間提供者是由 *時間提供者管理員* 管理。 它負責載入、啟動和停止服務控制管理員所導向的時間提供者。 這個介面讓撰寫時間提供者的程式比撰寫完整的服務更容易。

-   [建立時間提供者](creating-a-time-provider.md)
-   [註冊時間提供者](registering-a-time-provider.md)
-   [範例時間提供者](sample-time-provider.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Time 服務](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03mngd/26_s3wts.mspx)
</dt> </dl>

 

 



