---
title: 使用狀態伺服器
description: NPS 會使用 NPS 伺服器網站上設定的資料庫來執行驗證。
ms.assetid: 8313ba91-5ed1-44d0-80db-cfb82c641100
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d79ff46802d53109c7bb8b40fe3a2db2480949e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965851"
---
# <a name="working-with-a-state-server"></a>使用狀態伺服器

> [!Note]  
> 從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。 本主題的內容適用于 IAS 和 NPS。 在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。

 

NPS 會使用 NPS 伺服器網站上設定的資料庫來執行驗證。 此驗證資料庫可以是 Windows 網域的使用者資料庫，也可以在從 Windows Active Directory 取得的使用者資訊上進行繪製。 下圖說明的一般設定會顯示 NPS 如何與驗證資料庫（例如 Windows 網域使用者資料庫或 Active Directory）互動。 此圖也顯示 NPS 如何與協力廠商所提供的狀態伺服器互動。 狀態伺服器的主要目的是要限制單一使用者可以執行的同時登入會話數目。

![nps 與狀態伺服器和驗證資料庫互動](images/ias02.png)

NPS 與狀態伺服器之間有兩種互動點。 當 NPS 收到來自 NAS 的驗證要求時，就會發生一個互動。 狀態伺服器會從其資料庫提供資訊，以判斷是否接受或拒絕要求。 當 NPS 收到來自 NAS 的帳戶處理要求時，會發生其他互動。 狀態伺服器會使用此資訊形成這些帳戶處理要求，以更新其資料庫。

如需有關狀態伺服器的詳細資訊，請參閱：

-   [狀態伺服器設計考慮](/windows/desktop/Nps/ias-state-server-design-considerations)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[網際網路驗證服務和網路原則伺服器](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[RADIUS 驗證、授權和帳戶處理](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[使用網路原則伺服器進行記錄](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> </dl>

 

 