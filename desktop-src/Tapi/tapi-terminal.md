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
# <a name="tapiterminal"></a><span data-ttu-id="340b1-104">tapi/終端機</span><span class="sxs-lookup"><span data-stu-id="340b1-104">tapi/terminal</span></span>

<span data-ttu-id="340b1-105">Tapi/終端機裝置類別包含與線路上的每個終端機相關聯的電話裝置，或與手機裝置相關聯之每一行上的終端機。</span><span class="sxs-lookup"><span data-stu-id="340b1-105">The tapi/terminal device class consists of the phone devices associated with each terminal on a line or the terminal on each line associated with a phone device.</span></span> <span data-ttu-id="340b1-106">您可以使用 TAPI [線路裝置](line-device-functions.md) 或 [電話裝置功能](phone-device-functions.md)來存取這些裝置。</span><span class="sxs-lookup"><span data-stu-id="340b1-106">You access these devices by using the TAPI [line device](line-device-functions.md) or [phone device functions](phone-device-functions.md).</span></span>

<span data-ttu-id="340b1-107">[**LineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)函式會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構，將 **dwStringFormat** 成員設定為 STRINGFORMAT \_ 二進位值，並附加這個額外的成員：</span><span class="sxs-lookup"><span data-stu-id="340b1-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD adwDeviceId[];  // array of phone device identifiers
```

<span data-ttu-id="340b1-108">**AdwDeviceId** 成員是電話裝置識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="340b1-108">The **adwDeviceId** member is an array of phone device identifiers.</span></span> <span data-ttu-id="340b1-109">針對指定的線路裝置， [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)結構中的 **dwNumTerminals** 成員所指定的每個終端機都有一個陣列元素。</span><span class="sxs-lookup"><span data-stu-id="340b1-109">There is one array element for each terminal specified by the **dwNumTerminals** member in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the given line device.</span></span> <span data-ttu-id="340b1-110">每個元素都會指定與該行上相對應終端機相關聯的電話裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="340b1-110">Each element specifies the identifier of the phone device associated with the corresponding terminal on the line.</span></span> <span data-ttu-id="340b1-111">如果沒有與終端機相關聯的電話裝置，元素會設定為– 1 (0xFFFFFFFF) 。</span><span class="sxs-lookup"><span data-stu-id="340b1-111">If there is no phone device associated with a terminal, the element is set to –1 (0xFFFFFFFF).</span></span>

<span data-ttu-id="340b1-112">[**PhoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)函式會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構，將 **dwStringFormat** 成員設定為 STRINGFORMAT \_ 二進位值，並附加這個額外的成員：</span><span class="sxs-lookup"><span data-stu-id="340b1-112">The [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD adwTerminalID[];  // array of terminal identifiers
```

<span data-ttu-id="340b1-113">**AdwTerminalID** 成員是終端機識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="340b1-113">The **adwTerminalID** member is an array of terminal identifiers.</span></span> <span data-ttu-id="340b1-114">[**LineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)或 [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)函數所指定的每個線路裝置識別碼都有一個陣列元素。</span><span class="sxs-lookup"><span data-stu-id="340b1-114">There is one array element for each line device identifier specified by the [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) or [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) function.</span></span> <span data-ttu-id="340b1-115">每個陣列元素都包含與指定線路裝置的電話裝置相關聯的終端機識別碼。</span><span class="sxs-lookup"><span data-stu-id="340b1-115">Each array element contains the terminal identifier associated with the phone device for the given line device.</span></span> <span data-ttu-id="340b1-116">如果沒有電話裝置，元素會設定為– 1 (0xFFFFFFFF) 。</span><span class="sxs-lookup"><span data-stu-id="340b1-116">If there is no phone device, the element is set to –1 (0xFFFFFFFF).</span></span> <span data-ttu-id="340b1-117">終端機識別碼的值範圍從0到1，小於 [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)結構中 **dwNumTerminals** 成員所指定的數位。</span><span class="sxs-lookup"><span data-stu-id="340b1-117">The terminal identifiers range in value from zero to one less than the number specified by the **dwNumTerminals** member in the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure.</span></span>

 

 



