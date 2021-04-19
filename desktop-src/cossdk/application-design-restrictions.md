---
description: 有些應用程式的設計方式是防止在電腦上安裝多個應用程式實例。
ms.assetid: 951d20c8-7908-40d8-a9d5-d321340c97f3
title: 應用程式設計限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c4307a979866e3df9f019e69b858e8347c295b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992390"
---
# <a name="application-design-restrictions"></a>應用程式設計限制

有些應用程式的設計方式是防止在電腦上安裝多個應用程式實例。 有了這樣的限制，應用程式就無法使用分割區功能。 您可能需要先修改下列應用程式設計功能，然後才能將資料分割用於該應用程式。

## <a name="tables-and-arrays"></a>資料表和陣列

有些應用程式會建立資料庫資料表、記憶體內部資料表或使用 CLSID 作為唯一登錄機碼的陣列。 在沒有磁碟分割的電腦上，此登錄機碼通常是每台電腦)  (一個 CLSID 的電腦/CLSID。

相反地，在具有磁碟分割的電腦上，此登錄機碼是電腦/磁碟分割識別碼/應用程式識別碼/CLSID (每一部電腦) 的多重 CLSID 實例。 因為分割區功能可讓 CLSID 的多個實例存在於電腦上，所以包含每一部電腦需要唯一 CLSID 之設計項目的應用程式可能會受到負面影響。

## <a name="global-resources"></a>全域資源

有些應用程式會使用全域資源，例如共用記憶體、資料檔案和登錄專案。 如果這類應用程式的多個實例同時執行，這可能會造成問題。

例如，如果元件使用共用記憶體來與其他元件互動，則必須修改元件，讓元件的每個實例都配置它自己的共用記憶體。

## <a name="type-libraries"></a>類型程式庫

類型程式庫提供元件介面和方法的相關資訊。 這項資訊可用於數個用途，包括下列各項：

-   進行函式呼叫時，封送處理元件之間的資料
-   協助 COM + 佇列元件和 COM + 事件服務
-   在 Microsoft Visual Basic 編輯器中提供正確的資訊

類型程式庫的參考會安裝在電腦的登錄中。 開發從磁碟分割中叫用的應用程式時，將最新版本的類型程式庫安裝在登錄中是很重要的。 這可確保所使用的 Visual Basic 編輯器將取得該元件可用方法的精確資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 佇列元件和分割區](com--queued-components-and-partitions.md)
</dt> <dt>

[分割區執行](partition-implementation.md)
</dt> <dt>

[在分割區中註冊和啟用元件](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[什麼是 COM + 磁碟分割？](what-are-com--partitions-.md)
</dt> </dl>

 

 



