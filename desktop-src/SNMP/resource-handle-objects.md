---
title: 資源控制碼物件
description: 資源物件的結構受限於 Microsoft 的 WinSNMP 實行。 WinSNMP 應用程式可以存取具有控制碼的資源物件。
ms.assetid: c70a03b1-afac-4f1a-81e7-7f31430f5655
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1afe5e6488190f95961bff7ce37f7b719d076d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674907"
---
# <a name="resource-handle-objects"></a>資源控制碼物件

資源物件的結構受限於 Microsoft 的 WinSNMP 實行。 WinSNMP 應用程式可以存取具有控制碼的資源物件。

此實作為可為 WinSNMP 應用程式佈建下列其中一種資源控制碼類型。

| 控制碼類型        | Description                       |
|--------------------|-----------------------------------|
| **HSNMP \_ 會話** | 對 WinSNMP 會話的處理       |
| **HSNMP \_ 實體**  | SNMP 實體的控制碼          |
| **HSNMP \_ 內容** | 對 WinSNMP 內容的控制碼       |
| **HSNMP \_ PDU**     | 通訊協定資料單位的控制碼    |
| **HSNMP \_ VBL**     | 變數系結清單的控制碼 |



 

您可以使用 WinSNMP 應用程式要求執行建立或刪除資源控制碼，但此執行作業會執行此作業。 如需釋放個別資源的詳細資訊，請參閱 [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor)、 [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)、 [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)、 [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)和 [**SnmpFreeCoNtext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) 函數。

 

 




