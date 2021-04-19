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
# <a name="tapiline"></a><span data-ttu-id="337ae-104">tapi/行</span><span class="sxs-lookup"><span data-stu-id="337ae-104">tapi/line</span></span>

<span data-ttu-id="337ae-105">Tapi/線路裝置類別包含所有線路裝置。</span><span class="sxs-lookup"><span data-stu-id="337ae-105">The tapi/line device class consists of all line devices.</span></span> <span data-ttu-id="337ae-106">您可以使用 TAPI 線路功能來存取這些裝置。</span><span class="sxs-lookup"><span data-stu-id="337ae-106">You access these devices using the TAPI line functions.</span></span>

<span data-ttu-id="337ae-107">[**LineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)函式會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構，將 **dwStringFormat** 成員設定為 STRINGFORMAT \_ 二進位值，並附加這個額外的成員。</span><span class="sxs-lookup"><span data-stu-id="337ae-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member.</span></span>

``` syntax
DWORD dwDeviceI;  // line device identifier
```

<span data-ttu-id="337ae-108">**DwDeviceId** 成員是與 [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid)所指定之線條控制碼相關聯之線條裝置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="337ae-108">The **dwDeviceId** member is the identifier of the line device associated with the line handle given by [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid).</span></span>

<span data-ttu-id="337ae-109">[**PhoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid)函式也會填滿 [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring)結構，並將 **dwStringFormat** 設定為 STRINGFORMAT 二進位檔， \_ 並附加這個額外的成員：</span><span class="sxs-lookup"><span data-stu-id="337ae-109">The [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) function also fills a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting **dwStringFormat** to STRINGFORMAT\_BINARY and appending this additional member:</span></span>

``` syntax
DWORD adwDeviceIds[];  // array of line device identifiers
```

<span data-ttu-id="337ae-110">**AdwDeviceIds** 成員是一個陣列，其中包含與手機裝置相關聯的所有線路裝置的裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="337ae-110">The **adwDeviceIds** member is an array containing the device identifiers of all line devices that are associated with the phone device.</span></span> <span data-ttu-id="337ae-111">如果沒有相關聯的線路裝置， [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) 會傳回 PHONEERR \_ INVALDEVICECLASS 值。</span><span class="sxs-lookup"><span data-stu-id="337ae-111">If there are no associated line devices, [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) returns the PHONEERR\_INVALDEVICECLASS value.</span></span>

 

 



