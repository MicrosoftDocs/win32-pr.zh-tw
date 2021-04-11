---
title: DNS 概觀
description: DNS 是一種業界標準的服務，用來在網際網路通訊協定上找出 (IP) 網路的電腦。
ms.assetid: 98ecf24b-8bd5-4a75-a487-8af3080e8987
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 470807a5775b022834a3ca2f0ee3f91db8bdd5de
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "104196157"
---
# <a name="dns-overview"></a>DNS 概觀

DNS 是一種業界標準的服務，用來在網際網路通訊協定上找出 (IP) 網路的電腦。 IP 網路（例如網際網路和 Windows 2000 網路）依賴以數位為基礎的位址，例如 207.46.131.137) 簡單以 ferry 整個網路中的資訊。 網路使用者依賴以字元為基礎的名稱，例如 `www.microsoft.com` 。 因此，您必須將字元或方便使用的位址轉譯 (`www.microsoft.com`) 到網路可辨識的 (207.46.131.137) 簡單) 數位位址。 DNS 是 Windows 2000 中選擇的服務，用來找出資源並將其轉譯成對應的 IP 位址。

DNS 會使用資源記錄的特製化資料庫（通常稱為 Rr）來回應用戶端名稱解析查詢。 在 DNS 之前，網際網路上的名稱解析是透過 [*主機*](h-gly.md)檔案來達成，這是以手動方式建立的檔案，與 IP 位址相關聯的主機名稱。

當新的用戶端新增至網路時，系統管理員必須手動更新 hosts 檔案，然後將 (複寫) 該檔案複製到網路上的所有其他電腦，讓新的主機可以全部連線。 隨著網際網路的成長，這種形式的名稱解析顯然沒有足夠;管理密集，而且沒有 [*調整*](s-gly.md)。 Hosts 檔案變得更大，因為它使用了一般 [*命名空間*](f-gly.md) (另請參閱 [命名空間](name-space.md)) ，它無法進行分割，而且必須全部散發。 解決方案是 DNS。

-   DNS 已將主機檔案的一般命名空間取代為 [*階層式命名空間*](h-gly.md)。 使用階層式命名空間時，可分割和散發主機名稱和 IP 位址的相關資訊;因此，可進行擴充性。 例如，在虛構的 widgets.products.microsoft.com 網域中，可以分割名稱解析的責任，讓不同的伺服器可以針對命名空間的不同部分處理名稱解析：
    -   一部伺服器可以負責解析第一個部分 (microsoft.com) ，然後可以將名稱解析要求轉送到階層中的下一個 DNS 伺服器。
    -   下一部 DNS 伺服器可以負責解析 (產品) 的下一個部分的命名空間。
    -   最後，您可以將要求轉送到第三部 DNS 伺服器，該伺服器負責解析名稱 (widget) 的最後部分。

在階層式命名空間的每個部分中的 DNS 伺服器，都必須維護主機的資源記錄資料庫，但只限于階層中的部分。 因此，widgets.products.microsoft.com 的 products 部分中的伺服器 (或伺服器) 只針對階層式命名空間的 products 部分維護 Rr，而不是針對 microsoft.com 部分或命名空間的 widget 部分。

 

 




