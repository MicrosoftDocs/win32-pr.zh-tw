---
description: Ndis 裝置類別包含可與網路驅動程式介面規格相關聯的裝置 (NDIS) 媒體存取控制 (MAC) 驅動程式，以支援網路通訊。 您可以使用函數來存取這些裝置。
ms.assetid: 98cdd929-0bd7-4509-b2f5-4edd8d6a8080
title: Ndis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0be1a69f98f9a4ff8cdc2f8ea173b208c0011d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998257"
---
# <a name="ndis"></a>Ndis

Ndis 裝置類別包含可與網路驅動程式介面規格相關聯的裝置 (NDIS) 媒體存取控制 (MAC) 驅動程式，以支援網路通訊。 您可以使用函數來存取這些裝置。

[**LineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)和 [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)函式會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構、將 **dwStringFormat** 成員設定為 STRINGFORMAT \_ 二進位值，並附加這些額外的成員：

``` syntax
HANDLE  hDevice;          // NDIS connection identifier
CHAR    szDeviceType[1];  // name of device 
```

**HDevice** 成員是要傳遞至 MAC 的識別碼（例如撥號網路的非同步 MAC），以將網路連線與通話/數據機連線建立關聯。 **SzDeviceType** 成員是以 null 終止的字串，指定與識別碼相關聯之裝置的名稱。

 

 



