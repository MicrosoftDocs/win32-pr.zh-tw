---
description: 裝置網址類別型描述位址上允許的定址形式，例如電話號碼或 IP 位址。
ms.assetid: b474dfca-c4a6-4aab-a4dd-5aec7be3e02a
title: 地址類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9438c200c9b09dd4f78342ea18d412eaaf23b646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998129"
---
# <a name="address-type"></a><span data-ttu-id="dd014-103">地址類型</span><span class="sxs-lookup"><span data-stu-id="dd014-103">Address Type</span></span>

<span data-ttu-id="dd014-104">裝置網址類別型描述位址上允許的定址形式，例如電話號碼或 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="dd014-104">The device address type describes the forms of addressing permissible on an address, such as a phone number or an IP address.</span></span> <span data-ttu-id="dd014-105">指定的裝置將會瞭解一或多個網址類別型。</span><span class="sxs-lookup"><span data-stu-id="dd014-105">A given device will understand one or more address types.</span></span> <span data-ttu-id="dd014-106">如需 TAPI 所支援之網址類別型的清單，請參閱 [LINEADDRESSTYPE \_ 常數](lineaddresstype--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="dd014-106">For a list of address types supported by TAPI, see [LINEADDRESSTYPE\_ Constants](lineaddresstype--constants.md).</span></span> <span data-ttu-id="dd014-107">[位址轉譯](initiate-a-session-ovr.md) 可以用來將位址從某個類型轉換成另一種類型。</span><span class="sxs-lookup"><span data-stu-id="dd014-107">[Address translation](initiate-a-session-ovr.md) may be used to convert an address from one type to another.</span></span>

<span data-ttu-id="dd014-108">如需有關位址的一般資訊，請參閱[裝置類別](device-categories.md)下的[位址](address-ovr.md)。</span><span class="sxs-lookup"><span data-stu-id="dd014-108">For general information on addresses, see [Address](address-ovr.md) under [Device Categories](device-categories.md).</span></span>

<span data-ttu-id="dd014-109">[會話的網址類別型](address-type-for-a-session-ovr.md)會是裝置網址類別型的子集。</span><span class="sxs-lookup"><span data-stu-id="dd014-109">The [address type for a session](address-type-for-a-session-ovr.md) will be a subset of the device address types.</span></span>

<span data-ttu-id="dd014-110">**TAPI 2.x：** 請參閱 [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)和 [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps)的 **dwAddressType** 成員。</span><span class="sxs-lookup"><span data-stu-id="dd014-110">**TAPI 2.x:** See [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) and the **dwAddressType** member of [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps).</span></span>

<span data-ttu-id="dd014-111">**TAPI 3.x：** 請 [**參閱 ITAddressCapabilities：： \_ get AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability)，將 *AddressCap* 設定為 [**ADDRESS \_ 功能**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)的 **AC \_ ADDRESSTYPES** 成員。</span><span class="sxs-lookup"><span data-stu-id="dd014-111">**TAPI 3.x:** See [**ITAddressCapabilities::get\_AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability), with *AddressCap* set to the **AC\_ADDRESSTYPES** member of [**ADDRESS\_CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability).</span></span>

 

 
