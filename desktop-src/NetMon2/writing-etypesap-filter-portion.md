---
description: Capture 篩選器的 Etype/SAP 部分會通知網路監視器驅動程式，接受具有特定 Etypes 和服務存取點組合的框架)  (Sap。
ms.assetid: 57dcf1cd-f27f-4bd3-a5a8-9e978a2d213e
title: 撰寫 Etype/SAP 篩選部分
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b072d123ca18d3aa2b3f2c91db4a8461473a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944837"
---
# <a name="writing-etypesap-filter-portion"></a>撰寫 Etype/SAP 篩選部分

Capture 篩選器的 Etype/SAP 部分會通知網路監視器驅動程式，接受具有特定 Etypes 和 [*服務存取點*](s.md) 組合的框架)  (sap。 Etypes 和 Sap 是低層級的通訊協定（例如乙太網路、LLC 和貼齊）指出接下來的通訊協定。 具體來說：

-   Ethernet 指定 Etype
-   LLC 指定 SAP
-   貼齊會指定 Etype

## <a name="etypesap-capture-filter-flags"></a>Etype/SAP Capture 篩選旗標

您可以使用下列資訊，在 [**CAPTUREFILTER**](capturefilter.md)結構的 **FilterFlags** 成員中設定旗標。



| 旗標                                         | 意義                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAPTUREFILTER \_ 旗標 \_ 包括 \_ 所有 \_ SAP   | 傳遞所有 SAP 值，並通知驅動程式所有的 SAP 值都有效。 如果與 **lpSapTable** 成員中的任何值結合，此旗標會通知驅動程式，除了 **lpSapTable** 中的所有 SAP 值都有效。<br/>           |
| CAPTUREFILTER \_ 旗標 \_ 包含 \_ 所有 \_ ETYPES | 傳遞所有的 Etype 值，並通知驅動程式所有 Etype 值都有效。 如果與 **lpEtypeTable** 成員中的任何值結合，此旗標會通知驅動程式，除了 **lpEtypeTable** 中的所有 Etype 值都有效。<br/> |
| \_ \_ 僅限本機 CAPTUREFILTER 旗標 \_           | 設定此旗標不會將 NIC 設定為 P 模式。 您只會看到本機電腦上 (任何畫面格) 的本機流量。                                                                                                                                          |
| CAPTUREFILTER \_ 旗標 \_ 保持 \_ RAW             | 保留 SMT 和權杖環形 MAC 框架。                                                                                                                                                                                                                        |



 

## <a name="etypesap-capture-filter-settings"></a>Etype/SAP Capture 篩選器設定

您可以使用下列資訊來設定 [**CAPTUREFILTER**](capturefilter.md)結構的 **lpSapTable** 和 **lpEtypeTable** 成員。



| 設定          | 意義                                                                                                                                                                                                                                                              |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **lpSapTable**   | 列出您想要驅動程式傳遞的 SAP 值。 這份清單會告知網路監視器驅動程式驗證封裝含相符項的任何框架。 如果 \_ 已設定 CAPTUREFILTER 旗標 \_ 包括 \_ 所有 \_ sap，則會變成例外狀況清單 (如果找到的話，請不要傳遞) 。           |
| **lpEtypeTable** | 列出您想要網路監視器驅動程式傳遞的 Etype 值。 這份清單只會告知驅動程式驗證封裝含相符的任何框架。 如果 CAPTUREFILTER \_ 旗 \_ 標 \_ 包含 \_ 已設定的所有 ETYPES，這會變成例外狀況清單 (如果找到的話，請不要傳遞) 。 |



 

 

 




