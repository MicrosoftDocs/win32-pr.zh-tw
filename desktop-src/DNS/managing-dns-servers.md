---
title: 管理 DNS 伺服器
description: 瞭解如何管理 DNS 伺服器。 DNS 伺服器是在 DNS 中完成名稱解析程式的電腦。
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccce0b6c4a292e2fe46ec8584a601deee9267d2c5f1bfdeebaefa05db630f437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433378"
---
# <a name="managing-dns-servers"></a>管理 DNS 伺服器

DNS 伺服器是在 DNS 中完成名稱解析程式的電腦。 DNS 伺服器包含稱為 *區域* 檔案的檔案，可讓他們解析 IP 位址的名稱 (或反之亦然) 。 在查詢時，DNS 伺服器會以下列三種方式之一回應：

-   伺服器會傳回要求的名稱解析或 IP 解析資訊。
-   伺服器會將指標傳回給另一部可服務要求的 DNS 伺服器。
-   伺服器表示它沒有所要求的資訊。

DNS 伺服器可能會在準備傳回所要求的解析資訊時，查詢其他 DNS 伺服器。 但除此之外，DNS 伺服器不會執行上述清單中所述的任何作業。

有三種主要的 DNS 伺服器：主伺服器、次要伺服器和快取伺服器。 如需這些 DNS 伺服器的詳細資訊，請參閱 [Dns 伺服器](dns-servers.md) 。

## <a name="administration-steps"></a>管理步驟

DNS WMI 提供者可讓您從伺服器本身或從遠端主機管理 DNS 伺服器。 使用 DNS WMI 提供者管理 DNS 伺服器所需的一般步驟如下：

-   連接到 DNS WMI 提供者
-   取得伺服器實例
-   列出或修改伺服器屬性，或使用方法

為了說明如何實行這些管理步驟，我們提供了範例。 下列工作會連結到其相關聯的腳本範例。

-   [停止 DNS 伺服器](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [啟動 DNS 伺服器](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [重新開機 DNS 伺服器](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [新增 IP 位址](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [移除 IP 位址](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [列出 DNS 伺服器屬性](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [顯示 DNS 伺服器屬性類型](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [修改 DNS 伺服器屬性](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




