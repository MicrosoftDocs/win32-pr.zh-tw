---
description: Protected 儲存體為應用程式提供了一個介面，可儲存必須保持安全或無需修改的使用者資料。
ms.assetid: 85c1a009-c4f7-4b5a-ad96-6845a4e80de9
title: PStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e78732fc68c38585f04d61909addfac3f100ab10f497d8c5930d90e71b926981
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386058"
---
# <a name="pstore"></a>PStore

\[受保護的儲存體 (Pstore) 可在 Windows 伺服器2003和 Windows XP 中使用。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀作業，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

Protected 儲存體為應用程式提供了一個介面，可儲存必須保持安全或無需修改的使用者資料。

儲存的資料單位稱為「專案」。 所儲存資料的結構和內容對受保護的儲存體系統而言是不透明的。 存取專案時，可能會根據使用者定義的安全性樣式進行確認，這會指定存取資料所需的確認，例如是否需要密碼。 此外，對專案的存取會受到存取規則集的規範。 每個存取模式都有存取規則：例如，讀取/寫入。 存取規則集是由存取子句所組成。 目前支援兩種存取子句：呼叫端的 Authenticode 和二元檢查。 通常在應用程式設定時，會提供一種機制，讓新的應用程式向使用者要求可能已由其他應用程式建立的專案存取權。

專案是由索引鍵、類型、子類型和名稱的組合來唯一識別。 索引鍵是一個常數，可指定專案是否為此電腦的全域專案，或僅與此使用者相關聯。 名稱是一個字串，通常是由使用者選擇。 類型和子類型為 **GUID** s，通常是由應用程式指定。 類型和子類型的其他資訊會保存在系統登錄中，並包含顯示名稱和 UI 提示等屬性。 子類型的父類型是固定的，並且包含在系統登錄中做為屬性。 類型群組專案是用於一般用途：例如，付款或識別。 子類型群組專案共用一般的資料格式。

## <a name="in-this-section"></a>本節內容

-   [**IEnumPStoreItems**](ienumpstoreitems.md)
-   [**IEnumPStoreProviders**](ienumpstoreproviders.md)
-   [**IEnumPStoreTypes**](ienumpstoretypes.md)
-   [**IPStore**](ipstore.md)
-   [**PStoreCreateInstance**](pstorecreateinstance.md)
-   [**PStoreEnumProviders**](pstoreenumproviders.md)
-   [**PStore 常數**](pstore-constants.md)
-   [**PStore 類型**](pstore-types.md)

 

 
