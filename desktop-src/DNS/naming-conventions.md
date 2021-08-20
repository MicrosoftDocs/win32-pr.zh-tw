---
title: 命名規範
description: 命名慣例共用常見的目標，以明確地將名稱解析為網路位址，通常是 IP 位址。 命名慣例之間的差異在於每個慣例解決名稱的不同方法。
ms.assetid: 1ec96d2d-bb5a-4938-88c2-4d2802a326cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b378f9383f773cb24fb47c81cb92a066094a4ce528d7f3710212c6bb7cac0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076584"
---
# <a name="naming-conventions"></a>命名規範

命名慣例共用共同的目標：明確地將名稱解析為網路位址，通常是 IP 位址。 命名慣例之間的差異在於每個慣例解決名稱的不同方法。

下列命名慣例可用來識別各種系統名稱解析方法中的電腦，包括 Windows 2000 方法：

-   [電腦名稱稱](#computer-name)
-   [主機名稱](#host-name)
-   [ (FQDN) 的完整功能變數名稱 ](#fully-qualified-domain-name)
-   [相對辨別名稱](#relative-distinguished-name)

## <a name="computer-name"></a>電腦名稱

在一般 NetBIOS 命名空間中，單一名稱會將電腦名稱稱明確解析為網路位址。 這是先前 Windows 版本儲存在瀏覽器和主要瀏覽器清單中的名稱，可讓對等 Windows 網路流覽網路上 Windows 電腦上的資源。 在此案例中，與電腦相關聯的詞彙是 *電腦名稱稱*。 電腦名稱稱的註冊相依于網路廣播 (和主要瀏覽器，這取決於稍後所贏得的選舉 Windows 版本號碼或 Windows NT 使用方式，或) 的組合。 這對於小型、對等式 Windows 的網路很有用，但網路很快就會超過使用廣播和簡單一般檔案的主要瀏覽器清單所能提供的服務。

## <a name="host-name"></a>主機名稱

接下來是 Windows 的網際網路命名服務 (勝出) ，它已啟用以 NetBIOS 為基礎之電腦名稱稱的動態和集中式存放庫，儲存在 wins 伺服器上。 這些存放庫可以為較大的網路提供服務。 透過這種開發，可將名稱解析查詢導向至 WINS 伺服器 (而不是廣播) ，而且可能會集中仲裁衝突。 使用 WINS 時，會保留「電腦名稱稱」這一詞，但「 *主機名稱* 」一詞也會出現，並與電腦名稱稱交換使用。 當時，WINS 是 Windows 平臺的預設名稱解析程式，但 DNS 已獲得較大型和較大型網路的熱門程度和激增。

網路成長，且 WINS 變得較不能處理日益成長的名稱數量。 WINS 用來處理名稱解析負載的減少功能不是因為解決所需的處理能力，而是為大量電腦產生唯一名稱的事實，就是不斷增加的管理負擔。

## <a name="fully-qualified-domain-name"></a>完整網域名稱

DNS 是較佳的解決方案;使用其階層式命名空間時，唯一電腦名稱稱的需求會隔離到指定的網域，讓電腦名稱稱（例如 *server1* ）存在於相同階層中的不同網域位置。 由於具有在不同網域中具有相同主機名稱的功能，因此需要出現正確定址 DNS 階層的名稱。 名稱必須包含不只是電腦名稱稱或主機名稱，也必須包含可在整個 DNS 階層內明確識別或完全符合該電腦的名稱。 該名稱是 (FQDN) 的 [*完整功能變數名稱*](f-gly.md) ，例如 server1.widgets.microsoft.com。

不過，在某些情況下，FQDN 的網域階層部分相當繁瑣，而指定電腦 (或任何其他 DNS 主機) （相對於需要主機所在的 DNS 網域）則為本機名稱。 該名稱是 [*相對的分辨名稱*](r-gly.md)。 相對分辨名稱只是 FQDN 中最左邊點左邊的單一主機名稱，因此 server1.widgets.microsoft.com 的 FQDN 會有 server1 作為其相對分辨名稱。

## <a name="relative-distinguished-name"></a>相對辨別名稱

DNS 不會在 NetBIOS 名稱的使用者上採用新的名稱或新的命名慣例，而是使用 (主機名稱) 的電腦名稱稱做為相對辨別名稱，並將 DNS 網域階層附加至該名稱以建立 FQDN。 下圖說明如何識別電腦名稱稱 (或主機名稱，或) 部分 FQDN 的相對辨別名稱：

![rdn 和 dns 網域階層合併以建立 fqdn](images/fqdn.png)

 

 




