---
title: 管理 DNS 資源記錄
description: 瞭解如何管理資源記錄。 資源記錄是 DNS 區域檔案中的資訊專案單位，用來解析所有 DNS 查詢。
ms.assetid: ddad5f14-5a2d-4966-87b7-b354666f9e24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6c818899414cc541a1c89bfd11747051b2f5f1
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011111"
---
# <a name="managing-dns-resource-records"></a>管理 DNS 資源記錄

資源記錄（通常稱為 RR）是 DNS 區域檔案中的資訊專案單位。Rr 是主機名稱和 IP 資訊的基本組建區塊，可用來解析所有 DNS 查詢。 資源記錄會有相當廣泛的類型，以提供擴充的名稱解析服務。

不同類型的 Rr 具有不同的格式，因為它們包含不同的資料。 許多 Rr 共用一個通用的格式。 每一部 DNS 伺服器都會包含其所授權之命名空間部分的 Rr。

DNS WMI 提供者目前支援下列 RR 類型。 按一下資源記錄的名稱，以跳至其參考頁面。



| 提供者) 中的資源記錄 (                             | Description                                                  |
|-----------------------------------------------------------|--------------------------------------------------------------|
| [**MicrosoftDNS \_ AType**](microsoftdns-atype.md)         | 位址對應記錄的名稱                               |
| [**MicrosoftDNS \_ AAAAType**](microsoftdns-aaaatype.md)   | 主機至 Ipv6 地址記錄                                  |
| [**MicrosoftDNS \_ AFSDBType**](microsoftdns-afsdbtype.md) | Andrew 檔案系統資料庫伺服器記錄                    |
| [**MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype.md)   | ATM 位址對名稱記錄                                   |
| [**MicrosoftDNS \_ CNAMEType**](microsoftdns-cnametype.md) | 正式 [*名稱*](c-gly.md)記錄 |
| [**MicrosoftDNS \_ HINFOType**](microsoftdns-hinfotype.md) | 主機資訊記錄                                      |
| [**MicrosoftDNS \_ ISDNType**](microsoftdns-isdntype.md)   | 整合式服務數位網路記錄                   |
| [**MicrosoftDNS \_ KEYType**](microsoftdns-keytype.md)     | 索引鍵記錄。 請參閱 RFC 2535                                     |
| [**MicrosoftDNS \_ MBType**](microsoftdns-mbtype.md)       | 信箱記錄                                               |
| [**MicrosoftDNS \_ MDType**](microsoftdns-mdtype.md)       | 網域記錄的郵件代理程式                             |
| [**MicrosoftDNS \_ MFType**](microsoftdns-mftype.md)       | 網域記錄的郵件轉送代理程式                  |
| [**MicrosoftDNS \_ MGType**](microsoftdns-mgtype.md)       | 郵件群組記錄                                            |
| [**MicrosoftDNS \_ MINFOType**](microsoftdns-minfotype.md) | 郵件資訊記錄                                      |
| [**MicrosoftDNS \_ MRType**](microsoftdns-mrtype.md)       | 信箱重新命名記錄                                        |
| [**MicrosoftDNS \_ MXType**](microsoftdns-mxtype.md)       | 郵件交換記錄                                        |
| [**MicrosoftDNS \_ NSType**](microsoftdns-nstype.md)       | 名稱伺服器記錄                                           |
| [**MicrosoftDNS \_ NXTType**](microsoftdns-nxttype.md)     | 下一筆記錄                                                  |
| [**MicrosoftDNS \_ PTRType**](microsoftdns-ptrtype.md)     | 名稱對應記錄的位址                               |
| [**MicrosoftDNS \_ RPType**](microsoftdns-rptype.md)       | 負責任人員記錄                                    |
| [**MicrosoftDNS \_ RTType**](microsoftdns-rttype.md)       | 路由傳送記錄                                         |
| [**MicrosoftDNS \_ SIGType**](microsoftdns-sigtype.md)     | 簽章記錄                                             |
| [**MicrosoftDNS \_ SOAType**](microsoftdns-soatype.md)     | 開始授權                                           |
| [**MicrosoftDNS \_ SRVType**](microsoftdns-srvtype.md)     | 服務記錄                                               |
| [**MicrosoftDNS \_ TXTType**](microsoftdns-txttype.md)     | 文字記錄                                                  |
| [**MicrosoftDNS \_ WINSType**](microsoftdns-winstype.md)   | WINS 伺服器記錄                                           |
| [**MicrosoftDNS \_ WINSRType**](microsoftdns-winsrtype.md) | WINS 反向查閱記錄                                   |
| [**MicrosoftDNS \_ WKSType**](microsoftdns-wkstype.md)     | 知名的服務記錄                                   |
| [**MicrosoftDNS \_ X25Type**](microsoftdns-x25type.md)     | X.x.x.x 位址對名稱的對應記錄                         |



 

## <a name="administration-steps"></a>管理步驟

DNS WMI 提供者可讓您從伺服器本身或從遠端主機管理 Rr。 使用 DNS WMI 提供者管理 Rr 所需的一般步驟如下：

-   連接到 DNS WMI 提供者
-   取得資源記錄實例
-   列出或修改資源記錄屬性或使用方法

下列工作會連結到其相關聯的腳本範例。

-   [列出資源類型](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [新增資源記錄](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [刪除資源記錄](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [修改資源記錄](dns-wmi-provider-samples-managing-dns-resource-records.md)

 

 




