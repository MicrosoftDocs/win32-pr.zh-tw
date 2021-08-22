---
title: 主機名稱和 IP 位址
description: TCP/IP 網路需要先將主機名稱解析為 IP 位址，才能使用位址資訊來建立連線。
ms.assetid: f077e7d0-2e2c-4a2b-b5cd-1c7f43f7743b
keywords:
- SNMP 的主機名稱和 IP 位址
- 主機名稱，解析 SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f884f8ed681a5fc4864665f4c2a97ef8ed9fc0d81756d51848428b76163f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009506"
---
# <a name="host-names-and-ip-addresses"></a>主機名稱和 IP 位址

TCP/IP 網路需要先將主機名稱解析為 IP 位址，才能使用位址資訊來建立連線。 在 Windows 作業系統上執行的電腦會使用主機檔案，基於此目的，會將主機名稱對應至 IP 位址。

主機檔案是一個文字檔，其中列出明確的主機名稱和 IP 位址。 主機檔案會在啟動時自動載入至記憶體，並在主機名稱需要解析時進行諮詢。 如果主機檔案未包含將特定主機名稱解析為其 IP 位址所需的對應資訊，則會對 DNS 伺服器進行解析查詢。

SNMP 使用 Windows 網際網路命名服務 (WINS) 進行主機名稱解析。 WINS 可以將 NetBIOS 名稱或電腦名稱稱對應至 TCP/IP 網路上的 IP 位址。 如果電腦無法存取 WINS 伺服器，SNMP 服務會使用主機檔案來將主機名稱解析為 IP 位址。

SNMP 服務支援使用主機名稱和 IP 位址。 但是，當您選擇使用主機名稱或 IP 位址來識別網路位置時，您的 SNMP 管理應用程式應該使用主機名稱。 如果您使用主機名稱，請將參與系統的所有主機名稱和 IP 位址對應新增至主機檔案。

 

 




