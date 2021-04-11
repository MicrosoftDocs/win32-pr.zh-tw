---
description: Tapi/phone 裝置類別包含所有電話裝置。 您可以使用 TAPI 電話功能來存取這些裝置。
ms.assetid: c2e52fdf-e07a-4897-8af5-0a101d6c237a
title: tapi/電話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c704a6999982fb0c23a8b02439a3d0e61b3af8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944726"
---
# <a name="tapiphone"></a>tapi/電話

Tapi/phone 裝置類別包含所有電話裝置。 您可以使用 TAPI 電話功能來存取這些裝置。

[**PhoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)函式會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構，將 **dwStringFormat** 成員設定為 STRINGFORMAT \_ 二進位值，並附加這個額外的成員：

``` syntax
DWORD dwDeviceI;  // phone device identifier
```

**DwDeviceId** 成員是與 [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)所指定之電話控制碼相關聯之電話裝置的識別碼。

[**LineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)函式也會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構，並將 **dwStringFormat** 設定為 STRINGFORMAT 二進位檔， \_ 並附加這個額外的成員：

``` syntax
DWORD adwDeviceIds[];  // array of phone device identifiers
```

**AdwDeviceIds** 成員是一個陣列，其中包含與指定線路裝置相關聯之所有電話裝置的裝置識別碼。 如果沒有相關聯的電話裝置， [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) 會傳回 LINEERR \_ INVALDEVICECLASS 值。

 

 



