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
# <a name="tapiphone"></a><span data-ttu-id="434d2-104">tapi/電話</span><span class="sxs-lookup"><span data-stu-id="434d2-104">tapi/phone</span></span>

<span data-ttu-id="434d2-105">Tapi/phone 裝置類別包含所有電話裝置。</span><span class="sxs-lookup"><span data-stu-id="434d2-105">The tapi/phone device class consists of all phone devices.</span></span> <span data-ttu-id="434d2-106">您可以使用 TAPI 電話功能來存取這些裝置。</span><span class="sxs-lookup"><span data-stu-id="434d2-106">You access these devices by using the TAPI phone functions.</span></span>

<span data-ttu-id="434d2-107">[**PhoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)函式會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構，將 **dwStringFormat** 成員設定為 STRINGFORMAT \_ 二進位值，並附加這個額外的成員：</span><span class="sxs-lookup"><span data-stu-id="434d2-107">The [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD dwDeviceI;  // phone device identifier
```

<span data-ttu-id="434d2-108">**DwDeviceId** 成員是與 [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)所指定之電話控制碼相關聯之電話裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="434d2-108">The **dwDeviceId** member is the identifier of the phone device associated with the phone handle given by [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid).</span></span>

<span data-ttu-id="434d2-109">[**LineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)函式也會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構，並將 **dwStringFormat** 設定為 STRINGFORMAT 二進位檔， \_ 並附加這個額外的成員：</span><span class="sxs-lookup"><span data-stu-id="434d2-109">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function also fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to STRINGFORMAT\_BINARY and appending this additional member:</span></span>

``` syntax
DWORD adwDeviceIds[];  // array of phone device identifiers
```

<span data-ttu-id="434d2-110">**AdwDeviceIds** 成員是一個陣列，其中包含與指定線路裝置相關聯之所有電話裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="434d2-110">The **adwDeviceIds** member is an array containing the device identifiers of all phone devices that are associated with the given line device.</span></span> <span data-ttu-id="434d2-111">如果沒有相關聯的電話裝置， [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) 會傳回 LINEERR \_ INVALDEVICECLASS 值。</span><span class="sxs-lookup"><span data-stu-id="434d2-111">If there are no associated phone devices, [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) returns the LINEERR\_INVALDEVICECLASS value.</span></span>

 

 



