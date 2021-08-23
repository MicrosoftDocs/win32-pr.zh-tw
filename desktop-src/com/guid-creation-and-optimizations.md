---
title: 建立和優化 GUID
description: 建立和優化 GUID
ms.assetid: 698322f2-db89-4553-90c6-4278e96716dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82dc1b0cc52312768759daca35824f8e7e515629131ac2c301a17d7ae99d6455
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731428"
---
# <a name="guid-creation-and-optimizations"></a>建立和優化 GUID

因為 CLSID （例如 (IID) 的介面識別碼）是 GUID，所以沒有其他類別，無論誰寫入，都有重複的 CLSID。 伺服器實作者通常會透過 [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) 函數取得 clsid。 這項功能保證會產生獨特的 Clsid，因此全球的伺服器實施者可以獨立開發和部署其軟體，而不會干擾其他人所撰寫的軟體。

使用唯一的 Clsid 可避免類別之間發生名稱衝突的可能性，因為 Clsid 無法連接到基礎執行中使用的名稱。 例如，兩個不同的廠商可以撰寫稱為 "StackClass" 的類別，但每個都有唯一的 CLSID，因此不會混淆。

COM 經常必須將 Guid (Iid 和 Clsid) 對應至某些任意大型的其他值集。 作為應用程式開發人員，您可以藉由將應用程式的 Guid 產生為連續值的區塊，以協助加速這類搜尋，進而提升系統效能。

產生連續 Guid 區塊最有效率的方法，是使用-n 和-x 參數來執行 uuidgen.exe 公用程式，這會產生一個 Uuid 區塊，其中每一個都是由其第一個 DWORD 值遞增。

例如，如果您要輸入

**uuidgen.exe-n5-x**

uuidgen.exe 公用程式會產生類似下列的 Uuid 區塊：

``` syntax
12340001-4980-1920-6788-123456789012
12340002-4980-1920-6788-123456789012
12340003-4980-1920-6788-123456789012
12340004-4980-1920-6788-123456789012
12340005-4980-1920-6788-123456789012
 
```

針對整個專案產生和追蹤 Guid 的一個方法，一開始會產生一些任意數目的 Uuid，例如500。 例如，如果您要輸入

**uuidgen.exe-n500-x > guids.txt**

公用程式會產生500個連續的 Uuid，並將它們寫入指定的文字檔。 然後，您可以將此檔案簽入您的來源樹狀結構中，為專案中使用的所有 Guid 提供單一存放庫。 當人們要求專案的部分需要 Guid 時，他們就可以簽出檔案，但需要有許多需要的 Guid，將它們標示為已使用，並在程式碼或「規格」中使用它們的位置留下附注。

除了改善系統效能，以這種方式產生連續 Guid 區塊的優點如下：

-   中央檔案包含應用程式的所有 Guid，可讓您輕鬆追蹤哪些 Guid 適用于哪些 Guid 以及哪些使用者正在使用它們。
-   與特定應用程式相關聯的連續 Guid 區塊，可協助開發人員和測試人員在偵錯工具期間辨識內部 Guid，並讓您更輕鬆地在系統登錄中找到它們，因為它們會依序儲存。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 伺服器責任](com-server-responsibilities.md)
</dt> </dl>

 

 




