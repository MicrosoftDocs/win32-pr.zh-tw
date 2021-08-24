---
title: 線上音樂商店的常見內部問題
description: 線上音樂商店的常見內部問題
ms.assetid: 4210aabb-d1ad-4f98-88e0-941933d77303
keywords:
- Windows Media Player線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c4cb38f088f463d6bea8ca15b3a92cea9610cc8541f27d55c48df07f9286d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763958"
---
# <a name="common-on-boarding-problems-for-online-music-stores"></a>線上音樂商店的常見內部問題

以下是您應該嘗試避免的常見 Windows Media Player 內建問題清單。 任何這些問題都會導致您的存放區無法通過驗證測試。 若未通過 RC2，將會延遲啟動，直到下一個可用的啟動視窗為止。

1.  無法從測試伺服器轉換到實際執行伺服器
    -   遺漏的頁面
    -   IIS 設定 (存取、VRoots、HTTPs 或其他安全性設定) 
    -   測試帳戶無法再運作。
    -   測試帳戶未套用信用額度。
    -   服務託管標誌不會被移動。
    -   先前已有重複發生的 IP 限制。 尤其是，電子商務系統可能會有一組不同于音樂網站的限制。
    -   ServiceInfo 檔不會更新以指向生產環境。
2.  立即播放區域中的 [購買] 連結 (或 [商店] 連結) 無效。 這是經常被忽略的問題，而且會導致您的存放區即使在其他任何專案都處於正常運作的情況下也會失敗。
3.  Microsoft 的測試人員必須有足夠的購買能力。 Microsoft 的驗證小組將會在數個購買案例中執行，範圍從小型購買到極大型的購買。 您必須提供充電方式，讓它們作為商店內的取用者。 這可以透過提供虛擬信用卡來提供各種不同的帳戶。 例如，如果驗證測試人員嘗試購買專輯，但只有足夠的信用額度來購買單一曲目，則存放區在 RC2 中將會失敗。
4.  如果您在服務頁面內使用 ActiveX 控制項，請確保它們都能在所有適用的 Windows 版本上完整安裝和卸載。 若未這麼做，就會發生一般問題。 線上商店上的開發人員和測試人員通常會在自己的電腦上註冊 ActiveX 控制項，但忘了在使用者的電腦上安裝控制項。

    如果您的存放區安裝了外掛程式或 ActiveX 控制項，您必須提供使用者簡單的方法來將它卸載。 例如，Microsoft 最近發現某些線上商店安裝了 Windows Media Player 11 Windows 的 ActiveX 控制項，無法透過 [新增/移除程式] 功能表移除。 經過一些調查之後，Microsoft 發現 ActiveX 控制項可以透過 Internet Explorer 的附加元件管理員來移除。 請務必透過說明檔傳達 (，至少) 安裝和卸載 ActiveX 控制項和外掛程式的方式。

    如需有關如何將您的存放區與 Windows Vista 中的安全性基礎結構整合的詳細資訊，請參閱標題為「[應用程式在最低許可權環境中的開發人員最佳做法和指導方針](/previous-versions/aa905330(v=msdn.10))」一文。

 

 