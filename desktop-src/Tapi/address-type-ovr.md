---
description: 裝置網址類別型描述位址上允許的定址形式，例如電話號碼或 IP 位址。
ms.assetid: b474dfca-c4a6-4aab-a4dd-5aec7be3e02a
title: 地址類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1015c9ce501c6f82406fe80d8070a436887c86bbf7e7b59aac84daca3414760e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949164"
---
# <a name="address-type"></a>地址類型

裝置網址類別型描述位址上允許的定址形式，例如電話號碼或 IP 位址。 指定的裝置將會瞭解一或多個網址類別型。 如需 TAPI 所支援之網址類別型的清單，請參閱 [LINEADDRESSTYPE \_ 常數](lineaddresstype--constants.md)。 [位址轉譯](initiate-a-session-ovr.md) 可以用來將位址從某個類型轉換成另一種類型。

如需有關位址的一般資訊，請參閱[裝置類別](device-categories.md)下的[位址](address-ovr.md)。

[會話的網址類別型](address-type-for-a-session-ovr.md)會是裝置網址類別型的子集。

**TAPI 2.x：** 請參閱 [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)和 [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps)的 **dwAddressType** 成員。

**TAPI 3.x：** 請 [**參閱 ITAddressCapabilities：： \_ get AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability)，將 *AddressCap* 設定為 [**ADDRESS \_ 功能**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)的 **AC \_ ADDRESSTYPES** 成員。

 

 
