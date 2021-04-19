---
description: Tapi/線路裝置類別包含所有線路裝置。 您可以使用 TAPI 線路功能來存取這些裝置。
ms.assetid: 2215b10b-e410-462c-8cf9-42f3e688e82e
title: tapi/行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928cfa6144e9a701d6462519d2aa9d590a54a511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990365"
---
# <a name="tapiline"></a>tapi/行

Tapi/線路裝置類別包含所有線路裝置。 您可以使用 TAPI 線路功能來存取這些裝置。

[**LineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)函式會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構，將 **dwStringFormat** 成員設定為 STRINGFORMAT \_ 二進位值，並附加這個額外的成員。

``` syntax
DWORD dwDeviceI;  // line device identifier
```

**DwDeviceId** 成員是與 [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)所指定之線條控制碼相關聯之線條裝置的識別碼。

[**PhoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)函式也會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構，並將 **dwStringFormat** 設定為 STRINGFORMAT 二進位檔， \_ 並附加這個額外的成員：

``` syntax
DWORD adwDeviceIds[];  // array of line device identifiers
```

**AdwDeviceIds** 成員是一個陣列，其中包含與手機裝置相關聯的所有線路裝置的裝置識別碼。 如果沒有相關聯的線路裝置， [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) 會傳回 PHONEERR \_ INVALDEVICECLASS 值。

 

 



