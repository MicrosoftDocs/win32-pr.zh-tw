---
description: 下列詞彙描述存在於遠端系統上的網域。
ms.assetid: a6ce5356-682a-46ae-a101-15227c3b8d1e
title: 主要和受信任的網域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d80f1bd4983a17725de1bac9c55aae0f7d64e85bc2768bfaea2ca1469ed3d3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005059"
---
# <a name="primary-and-trusted-domains"></a>主要和受信任的網域

下列詞彙描述存在於遠端系統上的網域。

-   [主要網域](#primary-domain)
-   [受信任的網域](#primary-and-trusted-domains)

## <a name="primary-domain"></a>主要網域

主域是負責建立進一步信任關係和執行驗證 (，或將驗證要求傳遞至適當受信任網域) 的網域。 主網域中的網域控制站會處理或傳遞源自工作站的驗證要求。

當登入發生時，LSA 會檢查內建帳戶網域的驗證資訊。 如果要登入的帳戶不在這兩個網域中，則會將登入要求交給系統的主要網域。

## <a name="trusted-domain"></a>受信任的網域

受信任的網域是本機系統信任以驗證使用者的網域。 換句話說，如果使用者或應用程式是由受信任的網域驗證，則信任驗證網域的所有網域都會接受此驗證。

每個次級網域都會自動與主要網域有雙向信任關係。 根據預設，此信任是可轉移的，也就是說，如果系統信任網域 A，它也會信任網域 A 所信任的所有網域。 Windows 2000 之前的作業系統也支援單向信任，而這種情況不支援可轉移的雙向信任。

 (LSA) 的「 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) 」具有物件類型 [**TrustedDomain**](the-trusteddomain-object-type.md)，可用來儲存信任關係的相關資訊，包括受信任網域的名稱和 [*安全性識別碼*](/windows/desktop/SecGloss/s-gly) (SID) 、用於驗證要求的網域帳戶、名稱和 SID 轉譯要求，以及受信任網域中網域控制站的名稱。

在網域控制站上，LSA 會為本機系統所信任的每個網域建立 [**TrustedDomain**](the-trusteddomain-object-type.md) 物件的實例。

例如，如果 Windows XP 工作站信任 Windows 2000 網域控制站，而該控制器接著信任其他四個系統，則使用可轉移信任連線的工作站在其本機系統上將會有五個 [**TrustedDomain**](the-trusteddomain-object-type.md)物件。

 

 
