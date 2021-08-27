---
description: 若要在應用程式需要更高的 (（也就是系統) 的安裝許可權）時，以每個使用者的安裝方式公告應用程式，請使用下列清單中的指導方針：
ms.assetid: 0d2bd2d9-0eac-4519-862c-15f0ee5cbc40
title: 廣告以較高的許可權安裝的 Per-User 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdced246f90a345b5b2cc599541119a26e29e4d9a1d708be1ee8299d55d3c28d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082958"
---
# <a name="advertising-a-per-user-application-to-be-installed-with-elevated-privileges"></a>廣告以較高的許可權安裝的 Per-User 應用程式

若要在應用程式需要更高的 (（也就是系統) 的安裝許可權）時，以每個使用者的安裝方式公告應用程式，請使用下列清單中的指導方針：

-   您的進程必須是在 Windows XP 或更新版本上的 LocalSystem 系統帳戶下執行的服務。
-   藉由呼叫 [**MsiAdvertiseProduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) 或 [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)來產生公告腳本。
-   您的進程必須模擬作為廣告目標的使用者。
-   呼叫 [**MsiAdvertiseScript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)，然後使用旗標 SCRIPTFLAGS \_ CACHEINFO \| SCRIPTFLAGS \_ REGDATA \_ APPINFO \| SCRIPTFLAGS \_ REGDATA \_ CNFGINFO \| SCRIPTFLAGS \_ 快捷方式。

當您遵循指導方針時，您會將應用程式通告給指定的使用者，當使用者選擇安裝時，應用程式會以較高的許可權安裝。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[修補 Per-User 受控應用程式](patching-per-user-managed-applications.md)
</dt> </dl>

 

 



