---
description: 轉送是指連至不同目的地位址的連入會話的偏離。
ms.assetid: c70bf596-b2a4-46ec-9b1a-c9d948768b51
title: 轉寄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddddd21a945c3ca63a5c9040b8eabe0d1056b74b2f819f3fb62dbd8b760aaca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660848"
---
# <a name="forward"></a>轉寄

轉送是指連至不同目的地位址的連入會話的偏離。 TAPI 可讓應用程式指定位址的轉送條件清單。 轉送條件可以精確為每個呼叫端位址的不同目的地和 [**轉送模式**](./lineforwardmode--constants.md) 。

轉送作業也可以用來執行選擇性的不幹擾功能，方法是將一些來電者轉寄給語音信箱，讓其他人嘗試完成。

轉送作業也可以取消目前作用中的任何轉送。

某些服務提供者要求應用程式在轉送作業之前建立諮詢通話。 轉送作業接著會傳遞給諮詢通話的指標。

並非所有服務提供者都支援使用這項作業。

**TAPI 2.x：** 若要將 [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward) 設定為取得 [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus)，請使用 LINEADDRESSSTATE 轉寄來變更 [**行 \_ ADDRESSSTATE**](./line-addressstate.md) 通知訊息 \_ 。

**TAPI 3.x：** 請參閱 [**ITAddress：： Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward)、 [**ITAddress：： get \_ CurrentForwardInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo)、change notification： [**ITADDRESSEVENT：： get \_ Event**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) with AE \_ Forward。

> [!Note]  
> 服務提供者可能無法隨時知道轉送對位址有何作用。 轉送可以取消或變更，而不會產生通知給服務提供者。

 

 

 
