---
description: 此設定會在相同子網上的兩部主機之間建立 IPsec 安全性關聯 (SA) ，以使用驗證標頭 (AH) 和訊息摘要 5 (MD5) 雜湊演算法來執行驗證。
ms.assetid: ed88d8ee-ac65-4310-a988-ead50ff743fd
title: 設定3：在兩個本機連結主機之間使用 IPsec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b72485db34e8ff2c4e29a201df258dfb9d2ab9a00717ab515cda982e7ea867dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121428"
---
# <a name="configuration-3-using-ipsec-between-two-local-link-hosts"></a>設定3：在兩個本機連結主機之間使用 IPsec

此設定會在相同子網上的兩部主機之間建立 IPsec 安全性關聯 (SA) ，以使用驗證標頭 (AH) 和訊息摘要 5 (MD5) 雜湊演算法來執行驗證。 在此範例中，所顯示的設定會使用連結-本機位址 FE80：：2AA： FF： FE53： A92C 和主機2來保護兩個相鄰主機之間的所有流量，並使用連結-本機位址 FE80：：2AA： FF： FE92： D0F1。

**在兩個本機連結主機之間使用 IPsec**

1.  在主機1上，使用 ipsec6 c 命令 (SPD) 檔建立空白安全性關聯 (悲傷) 和安全性原則。 在此範例中，Ipsec6.exe 命令是 ipsec6 c test。 這會建立兩個檔案，以手動方式設定安全性關聯 (測試) 和安全性原則 (Test. spd) 。
2.  在主機1上，編輯 SPD 檔案以新增安全性原則，以保護主機1和主機2之間的所有流量。

    下表顯示在此範例中，第一個專案之前加入至測試. spd 檔案的安全性原則 (未修改) 中的第一個專案。

    | SPD 檔案功能變數名稱 | 範例值              |
    |---------------------|----------------------------|
    | **原則**          | 2                          |
    | **RemoteIPAddr**    | **FE80：：2AA： FF： FE92： D0F1** |
    | **LocalIPAddr**     | \*                         |
    | **Server.remoteport**      | \*                         |
    | **通訊協定**        | \*                         |
    | **LocalPort**       | \*                         |
    | **IPSecProtocol**   | **啊**                     |
    | **IPSecMode**       | **運輸**              |
    | **RemoteGWIPAddr**  | \*                         |
    | **SABundleIndex**   | **NONE**                   |
    | [方向]       | **BIDIRECT**               |
    | **動作**          | **應用**                  |
    | **InterfaceIndex**  | 0                          |

    

     

    將分號放在設定此安全性原則的行尾。 原則專案必須以遞減的數值順序放置。

3.  在主機1上，編輯悲傷檔案，新增 SA 專案以保護主機1和主機2之間的所有流量。 必須建立兩個安全性關聯，一個用於主機2的流量，另一個用於主機2的流量。

    下表顯示此範例 (的第一個 SA 專案加入至主機 2) 的流量。

    | 悲傷的檔案功能變數名稱 | 範例值              |
    |---------------------|----------------------------|
    | **SAEntry**         | 2                          |
    | **SPI**             | 3001                       |
    | **SADestIPAddr**    | **FE80：：2AA： FF： FE92： D0F1** |
    | **DestIPAddr**      | **原則**                 |
    | **SrcIPAddr**       | **原則**                 |
    | **通訊協定**        | **原則**                 |
    | **DestPort**        | **原則**                 |
    | **SrcPort**         | **原則**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **測試金鑰**               |
    | [方向]       | **出境**               |
    | **SecPolicyIndex**  | 2                          |

    

     

    在設定此 SA 的行尾放置分號。

    下表顯示在此範例中，針對來自主機 2) 的流量，將第二個 SA 專案新增至測試的 (。

    | 悲傷的檔案功能變數名稱 | 範例值              |
    |---------------------|----------------------------|
    | **SAEntry**         | 1                          |
    | **SPI**             | 3000                       |
    | **SADestIPAddr**    | **FE80：：2AA： FF： FE53： A92C** |
    | **DestIPAddr**      | **原則**                 |
    | **SrcIPAddr**       | **原則**                 |
    | **通訊協定**        | **原則**                 |
    | **DestPort**        | **原則**                 |
    | **SrcPort**         | **原則**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **測試金鑰**               |
    | [方向]       | **入境**                |
    | **SecPolicyIndex**  | 2                          |

    

     

    在設定此 SA 的行尾放置分號。 SA 專案必須以遞減的數位順序放置。

4.  在主機1上，建立一個文字檔，其中包含用來驗證主機2所建立之 SAs 的文字字串。 在此範例中，會使用「這是測試」內容來建立檔案測試。 您必須在索引鍵字串前後加上雙引號，才能讓 ipsec6 工具讀取金鑰。

    Microsoft IPv6 技術預覽僅支援手動設定的金鑰來驗證 IPsec SAs。 手動金鑰的設定方式是建立文字檔，其中包含手動按鍵的文字字串。 在此範例中，會在兩個方向使用相同的 SAs 金鑰。 您可以使用不同的金鑰來處理輸入和輸出 SAs，方法是建立不同的金鑰檔，然後使用 SAD 檔案中的 KeyFile 欄位來參考它們。

5.  在主機2上，使用 ipsec6 c 命令 (SPD) 檔建立空白安全性關聯 (悲傷) 和安全性原則。 在此範例中，Ipsec6.exe 命令是 ipsec6 c test。 這會建立兩個具有空白專案的檔案，以便手動設定安全性關聯 (測試) 和安全性原則 (Test. spd) 。

    為了簡化此範例，會在主機2上使用相同的悲傷和 SPD 檔案檔案名。 您可以選擇在每部主機上使用不同的檔案名。

6.  在主機2上，編輯 SPD 檔案以新增安全性原則，以保護主機2和主機1之間的所有流量。

    下表顯示在此範例中，將第一個專案加入至測試的測試檔中之前加入的安全性原則專案 (測試中的第一個專案未) 修改。

    | SPD 檔案功能變數名稱 | 範例值              |
    |---------------------|----------------------------|
    | **原則**          | 2                          |
    | **RemoteIPAddr**    | **FE80：：2AA： FF： FE53： A92C** |
    | **LocalIPAddr**     | \*                         |
    | **Server.remoteport**      | \*                         |
    | **通訊協定**        | \*                         |
    | **LocalPort**       | \*                         |
    | **IPSecProtocol**   | **啊**                     |
    | **IPSecMode**       | **運輸**              |
    | **RemoteGWIPAddr**  | \*                         |
    | **SABundleIndex**   | **NONE**                   |
    | [方向]       | **BIDIRECT**               |
    | **動作**          | **應用**                  |
    | **InterfaceIndex**  | 0                          |

    

     

    將分號放在設定此安全性原則的行尾。 原則專案必須以遞減的數值順序放置。

7.  在主機2上，編輯悲傷檔案，新增 SA 專案以保護主機2與主機1之間的所有流量。 必須建立兩個安全性關聯-一個用於主機1的流量，另一個用於主機1的流量。

    下表顯示在此範例中，針對來自主機 1) 的流量，將第一個 SA 新增至測試的 (。

    | 悲傷的檔案功能變數名稱 | 範例值              |
    |---------------------|----------------------------|
    | **SAEntry**         | 2                          |
    | **SPI**             | 3001                       |
    | **SADestIPAddr**    | **FE80：：2AA： FF： FE92： D0F1** |
    | **DestIPAddr**      | **原則**                 |
    | **SrcIPAddr**       | **原則**                 |
    | **通訊協定**        | **原則**                 |
    | **DestPort**        | **原則**                 |
    | **SrcPort**         | **原則**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **測試金鑰**               |
    | [方向]       | **入境**                |
    | **SecPolicyIndex**  | 2                          |

    

     

    在設定此 SA 的行尾放置分號。

    下表顯示在此範例中，新增至測試的測試悲傷檔案的第二個 SA 專案 (用於裝載 1) 的流量。

    | 悲傷的檔案功能變數名稱 | 範例值              |
    |---------------------|----------------------------|
    | **SAEntry**         | 1                          |
    | **SPI**             | 3000                       |
    | **SADestIPAddr**    | **FE80：：2AA： FF： FE53： A92C** |
    | **DestIPAddr**      | **原則**                 |
    | **SrcIPAddr**       | **原則**                 |
    | **通訊協定**        | **原則**                 |
    | **DestPort**        | **原則**                 |
    | **SrcPort**         | **原則**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **測試金鑰**               |
    | [方向]       | **出境**               |
    | **SecPolicyIndex**  | 2                          |

    

     

    在設定此 SA 的行尾放置分號。 SA 專案必須以遞減的數位順序放置。

8.  在主機2上，建立一個文字檔，其中包含用來驗證以主機1建立之 SAs 的文字字串。 在此範例中，會使用「這是測試」內容來建立檔案測試。 您必須在索引鍵字串前後加上雙引號，才能讓 ipsec6 工具讀取金鑰。
9.  在主機1上，使用 ipsec6 命令，從 SPD 和悲傷檔案新增設定的安全性原則和 SAs。 在此範例中，ipsec6 會在主機1上執行測試命令。
10. 在主機2上，使用 ipsec6 命令，從 SPD 和悲傷檔案新增設定的安全性原則和 SAs。 在此範例中，ipsec6 會在主機2上執行測試命令。
11. 使用 ping6 命令從主機2偵測主機1。

    如果您使用 Microsoft 網路監視器或另一個封包探測器來捕捉流量，您應該會看到 ICMPv6 Echo 要求和回應訊息的交換，以及 IPv6 標頭與 ICMPv6 標頭之間的驗證標頭。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IPv6 的建議設定](recommended-configurations-2.md)
</dt> <dt>

[具有連結-本機位址的單一子網](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[IPv4 網路上不同子網節點之間的 IPv6 流量 (6to4) ](configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4--2.md)
</dt> </dl>

 

 



