---
title: 管理對等快取
description: 注意：從 Windows 7 開始，背景智慧型傳送服務 (位) 3.0 對等快取模型已被取代。
ms.assetid: a33a43e5-02f9-4902-ad3a-ec65b0d80520
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b3ea1dd19c9aca855ffd73e174dcb3b588a54d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671783"
---
# <a name="administering-the-peer-cache"></a>管理對等快取

> [!Note]  
> 從 Windows 7 開始，背景智慧型傳送服務 (位) 3.0 對等快取模型已被取代。 如果已安裝 BITS 4.0，BITS 3.0 對等快取模型就無法使用。

 

為了改善下載效能，BITS 可讓您從對等電腦下載內容。 若要啟用這項功能，系統管理員必須啟用 EnablePeerCaching 群組原則設定。 啟用時，對等可以從對等下載內容，並將內容提供給對等。 系統管理員也可以使用 DisablePeerCachingClient 和 DisablePeerCachingServer 原則設定，以防止從對等下載內容，或將內容分別提供給對等。

如果未設定群組原則設定，則應用程式可以呼叫 [**IBitsPeerCacheAdministration：： SetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setconfigurationflags) 方法來設定電腦的對等快取喜好設定。 請注意，如果稍後設定這些喜好設定，這些喜好設定會由群組原則設定覆寫。 若要判斷電腦是否啟用對等快取，請呼叫 [**IBitsPeerCacheAdministration：： GetConfigurationFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-getconfigurationflags) 方法。

如果已啟用對等快取，則只有在作業明確允許快取其內容時，BITS 才會快取作業的內容。 只有當作業明確允許時，BITS 也會從對等下載內容。 若要啟用作業的對等快取，請呼叫 [**IBackgroundCopyJob4：： SetPeerCachingFlags**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-setpeercachingflags) 方法。

除了使用群組原則或 [**IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) 介面啟用對等快取，您也可以使用任一種方法來變更預設快取大小，以及在快取中保留非存取檔案的時間長度。 若要使用 **IBitsPeerCacheAdministration** 介面變更預設值，請呼叫 [**SetMaximumCacheSize**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setmaximumcachesize) 和 [**SetMaximumContentAge**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-setmaximumcontentage) 方法。 因為這些方法會設定喜好設定，所以這些設定會由群組原則設定覆寫。

若要列出位將嘗試下載內容的對等，請呼叫 [**IBitsPeerCacheAdministration：： EnumPeers**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-enumpeers) 方法。

若要列出快取中 BITS 將提供給對等的檔案，請呼叫 [**IBitsPeerCacheAdministration：： EnumRecords**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibitspeercacheadministration-enumrecords) 方法。

在探索對等或刪除快取記錄時，您應該永遠不需要管理對等快取。 這項功能已包含在 [**IBitsPeerCacheAdministration**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibitspeercacheadministration) 介面中，以提供完整性。

 

 




