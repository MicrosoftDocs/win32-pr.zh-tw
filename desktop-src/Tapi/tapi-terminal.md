---
description: Tapi/終端機裝置類別包含與線路上的每個終端機相關聯的電話裝置，或與手機裝置相關聯之每一行上的終端機。 您可以使用 TAPI 線路裝置或電話裝置功能來存取這些裝置。
ms.assetid: 466ed2cd-f737-4df4-8633-4fb5c95b4b6c
title: tapi/終端機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce64da984f766e8ca3c0c47f1b60db6e9d7d8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997843"
---
# <a name="tapiterminal"></a>tapi/終端機

Tapi/終端機裝置類別包含與線路上的每個終端機相關聯的電話裝置，或與手機裝置相關聯之每一行上的終端機。 您可以使用 TAPI [線路裝置](line-device-functions.md) 或 [電話裝置功能](phone-device-functions.md)來存取這些裝置。

[**LineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)函式會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構，將 **dwStringFormat** 成員設定為 STRINGFORMAT \_ 二進位值，並附加這個額外的成員：

``` syntax
DWORD adwDeviceId[];  // array of phone device identifiers
```

**AdwDeviceId** 成員是電話裝置識別碼的陣列。 針對指定的線路裝置， [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)結構中的 **dwNumTerminals** 成員所指定的每個終端機都有一個陣列元素。 每個元素都會指定與該行上相對應終端機相關聯的電話裝置識別碼。 如果沒有與終端機相關聯的電話裝置，元素會設定為– 1 (0xFFFFFFFF) 。

[**PhoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)函式會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構，將 **dwStringFormat** 成員設定為 STRINGFORMAT \_ 二進位值，並附加這個額外的成員：

``` syntax
DWORD adwTerminalID[];  // array of terminal identifiers
```

**AdwTerminalID** 成員是終端機識別碼的陣列。 [**LineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)或 [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)函數所指定的每個線路裝置識別碼都有一個陣列元素。 每個陣列元素都包含與指定線路裝置的電話裝置相關聯的終端機識別碼。 如果沒有電話裝置，元素會設定為– 1 (0xFFFFFFFF) 。 終端機識別碼的值範圍從0到1，小於 [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)結構中 **dwNumTerminals** 成員所指定的數位。

 

 



