---
title: " (SNMP) 的物件識別碼"
description: SNMP 物件識別碼可唯一命名物件，並在管理資訊基底 (MIB) 樹狀結構中識別其位置。
ms.assetid: b4552185-ef37-4e04-9b19-a226165e0b32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b81d52e43cb3be89551dd597bc5084d533f3913264f8bcf5c0a2ef7dbb375bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009256"
---
# <a name="object-identifiers-snmp"></a> (SNMP) 的物件識別碼

SNMP 物件識別碼可唯一命名物件，並在管理資訊基底 (MIB) 樹狀結構中識別其位置。 物件識別碼是與應用程式無關的抽象語法標記法 (一)  (asn.1) 包含非負整數或 subidentifiers 序列的資料類型。 物件識別碼至少必須有兩個 subidentifiers，而且不能超過 128 subidentifiers。

WinSNMP 程式設計環境會使用 [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) 結構來管理物件識別碼。 在 **smiOID** 結構中，物件識別碼陣列的格式為每個陣列元素一次 subidentifier。

物件識別碼以點分隔的數值字串表示會以句號分隔其 subidentifiers。例如，"1.2.3.4.5.6"。

如需詳細資訊，請參閱 [SNMP 管理資訊基礎 (MIB) ](the-snmp-management-information-base-mib-.md) 和相關的 rfc。

 

 




