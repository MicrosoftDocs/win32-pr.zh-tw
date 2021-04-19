---
description: 位址指派之後，TAPI 會將位址識別碼指派給位址。
ms.assetid: 19394db1-4408-4ba6-be48-b408c1fa0f30
title: 位址識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80ee463271a4d7fe9e4dcec086b08c37326551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973033"
---
# <a name="address-identifiers"></a><span data-ttu-id="64f65-103">位址識別碼</span><span class="sxs-lookup"><span data-stu-id="64f65-103">Address Identifiers</span></span>

<span data-ttu-id="64f65-104">位址指派之後，TAPI 會將位址識別碼指派給位址。</span><span class="sxs-lookup"><span data-stu-id="64f65-104">After address assignment, TAPI assigns address identifiers to the addresses.</span></span> <span data-ttu-id="64f65-105">*位址識別碼* 是介於0和行的位址數目減一的數位。</span><span class="sxs-lookup"><span data-stu-id="64f65-105">An *address identifier* is a number between 0 and the number of addresses on the line minus one.</span></span> <span data-ttu-id="64f65-106">位址識別碼是指派給指定裝置的永久數位，即使是在作業系統升級之間仍維持不變。</span><span class="sxs-lookup"><span data-stu-id="64f65-106">An address identifier is a permanent number assigned to a given device and remains constant even across operating system upgrades.</span></span> <span data-ttu-id="64f65-107">[裝置識別碼](device-identifier-ovr.md)和位址識別碼的組合可唯一識別指定的位址。</span><span class="sxs-lookup"><span data-stu-id="64f65-107">The combination of [device identifier](device-identifier-ovr.md) and address identifier uniquely identifies a given address.</span></span>

<span data-ttu-id="64f65-108">**TAPI 2.x：** 應用程式會在呼叫 [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) 或 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo)、 [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) 結構或呼叫 [**lineGetAddressID**](/windows/win32/api/tapi/nf-tapi-linegetaddressid)時，取得位址識別碼 (和裝置識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="64f65-108">**TAPI 2.x:** Applications obtain an address identifier (and device identifier) during a call to [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) or [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), in the [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) structure, or in a call to [**lineGetAddressID**](/windows/win32/api/tapi/nf-tapi-linegetaddressid).</span></span>

<span data-ttu-id="64f65-109">**TAPI 3.x：**[**ITAddressCapabilities：： get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability)稱為 *AddressCap* 設定為 [**ADDRESS \_ 功能**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)的 **AC \_ ADDRESSID** 成員將會傳回，並將 *plCapability* 參數設定為目前的位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="64f65-109">**TAPI 3.x:** The [**ITAddressCapabilities::get\_AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) called *AddressCap* set to the **AC\_ADDRESSID** member of [**ADDRESS\_CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) will return with the *plCapability* parameter set to the current address ID.</span></span>

 

 
