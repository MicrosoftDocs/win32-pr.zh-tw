---
description: 從 IPv4 到 IPv6 的最明顯變更之一，就是 IP 位址的大小。 許多使用者介面提供的對話方塊，可讓使用者輸入 IP 位址，如下圖中的查詢示。
ms.assetid: e2d7fd41-297a-400b-ae59-5d67db2be6f6
title: IPv6 Winsock 應用程式的消費者介面問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03305073687cdd77e17c529d70ffe5959df40960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971546"
---
# <a name="user-interface-issues-for-ipv6-winsock-applications"></a>IPv6 Winsock 應用程式的消費者介面問題

從 IPv4 到 IPv6 的最明顯變更之一，就是 IP 位址的大小。 許多使用者介面提供的對話方塊，可讓使用者輸入 IP 位址，如下圖中的查詢示。

![使用者介面中的一般 ipv4 位址方塊](images/portingguide001.jpg)

因為許多因素，例如長度、複雜度，以及 IPv6 位址空間內各區段的重要性等因素，所以在 IPv6 中定址不採用遭利用由使用者修改或規格。 因此，讓使用者能夠指定自己的位址的需求也會降低。 此外，由於與 IPv6 定址相關的複雜度，讓系統管理員能夠指定 IPv6 位址資訊，不太可能會以每個節點為基礎。

在 UI 中顯示 IPv6 位址並不會 inconceivable，因此開發人員應該在修改應用程式以支援 IPv6 時，考慮 IPv6 位址的大小變化。

本節的其餘部分將討論 IPv4 位址長度可預測性和 IPv6 位址長度考慮之間的差異。 本節假設 IPv6 位址會顯示在其十六進位標記法中。

IPv4 位址的大小是可預測的，因為它們會以小數點的十進位標記法為依據，如下列位址範例所示：

``` syntax
10.10.256.1
```

IPv6 位址不是可預測的，因為 IPv6 位址慣例可讓您使用雙冒號 (：： ) 來代表一連串的零。 因此，下列 IPv6 位址表示等同于相同的 IPv6 位址：

``` syntax
1040:0:0:0:0:0:0:1
1040::1
```

以雙冒號表示一系列零的功能，會導致任何指定 IPv6 的長度無法預期，這需要程式設計人員在建立 IPv6 位址的使用者介面顯示時，將這項功能納入考慮。 當然，開發人員應確定使用者介面能夠顯示不使用雙冒號的 IP 位址，以代表一系列的零 (第一個位址) ，以及能夠顯示以下的最長可能 IPv6 位址 (第二個位址，並在建立具備 IPv6 功能的使用者介面時) 內嵌的 IPv4 位址。 也請注意，將範圍識別碼 (識別碼) 新增至下列位址，將會增加其長度，最多可達另一個11個字元：

``` syntax
21DA:00D3:0010:2F3B:02AA:00FF:FE28:9C5A
0000:0000:0000:0000:0000:ffff:123.123.123.123
```

另一個重要考慮是，以名稱為基礎的位址是否更適合以數位為基礎的 IPv6 位址。 如果以名稱為基礎的位址更適合，則應該在使用者介面中內建命名慣例考慮，包括適用于工作的任何輸入錯誤檢查。

當您在修改應用程式時，以及設計 IPv6 位址的使用者介面標記法時，會顯示開發人員必須考慮的 IPv6 位址，還有其他一些複雜性。 其中一些考慮如下：

-   位址是否包含所有零的序列，或使用雙冒號標記法？
-   是否更適合使用以數位為基礎的位址表示或以名稱為基礎的表示方式？
-   使用者是否有興趣辨識定址配置的特定層面，例如子網首碼、範圍識別碼或其他子欄位？
-   使用者是否有興趣決定位址的其他層面，例如 TLA 識別碼、NLA 識別碼或 SLA 識別碼？
-   您的使用者介面是否能夠辨識內嵌的 IPv6 位址，如果有的話，該如何處理和顯示？ 當您向使用者顯示位址資訊時，您會在 IPv4 相容的位址和 IPv4 對應的 IPv6 位址之間辨別嗎？

另外還有其他考慮，開發人員應在開發 IP 位址使用者介面時，仔細考慮他們的客戶物件。

最佳做法

-   在修改應用程式以支援 IPv6 時，開發人員必須針對每個使用者介面考慮適當的方法。 確定使用者介面包含足夠的長度來顯示 IPv6 位址是必要的，因為它會判斷該位址是以數位或名稱為基礎。
-   使用 IPv6 位址時，請盡可能使用現有的 Winsock 和 IP Helper 函式，而不是重新執行此邏輯。 例如，您可以使用 [**RtlIpv6AddressToString**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa)、 [**RtlIpv6AddressToStringEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)、 [**RtlIpv6StringToAddress**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)和 [**RtlIpv6StringToAddressEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw) 函數，在 ipv6 位址和這些 ipv6 位址的字串表示之間進行轉換。

要避免的程式碼

-   相依于 IPv4 大小之位址的使用者介面元素必須經過審查，而該審查的一部分應該包含您在 IPv4) 提供 (的資訊是否適合 IPv6。
-   指定 IP 位址的功能也應該取決於 IPv4 是否正在使用中，或 IPv6 是否可用。 如果有 IPv6 可用，是否適合指定以數位為基礎的 (十六進位) 位址或以名稱為基礎的位址？

編寫工作的程式碼

**從 IPv4 將現有的程式碼基底修改為 IPv4 和 IPv6 互通性**

1.  執行使用者介面的視覺化查看，尋找相依于 IP 位址字串特定長度的任何元素。 具有容易識別之四個區段的小數點小數點標記法的控制項很容易找到，但其他控制項則否。 可能會有一些可能會顯示 IP 位址的位置，例如在對話方塊中，IPv6 位址可能會用盡顯示空間。
2.  在尋找任何這些控制項時，請在使用 IPv6 時，仔細確認是否適合顯示位址。 如果有可能是 IPv4 或 IPv6 正在使用中，請確定使用者介面可以容納其中一種。 以可顯示整個 IPv6 位址的使用者介面控制項來取代或增強任何控制項。
3.  追蹤使用者介面的測試，以確保在使用 IPv4 位址時，允許 IPv6 位址顯示的變更維持預期的可用性。 此外，也請測試通訊協定位址顯示位置，例如資訊對話方塊，以確保它們能夠正確地處理 IPv6 位址。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[適用于 Windows 通訊端應用程式的 IPv6 指南](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[變更 IPv6 Winsock Html5 應用程式的資料結構](changing-data-structures-2.md)
</dt> <dt>

[IPv6 Winsock 應用程式的雙重堆疊通訊端](dual-stack-sockets.md)
</dt> <dt>

[IPv6 Winsock 應用程式的函式呼叫](function-calls-2.md)
</dt> <dt>

[使用硬式編碼的 IPv4 位址](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[IPv6 Winsock 應用程式的基礎通訊協定](underlying-protocols-2.md)
</dt> </dl>

 

 
