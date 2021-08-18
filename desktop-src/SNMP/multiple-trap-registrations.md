---
title: 多重陷阱註冊
description: 當 WinSNMP 應用程式註冊用於陷阱或通知的 WinSNMP 會話時，有數個選項可供使用。
ms.assetid: 76a4095f-ab5c-4f7a-9b60-a383a632fd65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2149e4ac1e9880601ae64718cd78991718d54a6228488a03e593376d9a7937
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009325"
---
# <a name="multiple-trap-registrations"></a>多重陷阱註冊

當 WinSNMP 應用程式註冊用於陷阱或通知的 WinSNMP 會話時，有數個選項可供使用。 因此，應用程式可以多次呼叫 [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) 函式，實際上會定義接收陷阱和通知的自訂篩選準則。 例如，您可以註冊某一種陷阱或通知，或針對所有陷阱和通知，視 *通知* 參數的值而定。 此外，應用程式可以在 **SnmpRegister** 函式的其他參數中指定值，以進一步定義應到達應用程式的陷阱和通知。 如需詳細資訊，請參閱 [管理陷阱和通知](managing-traps-and-notifications.md)。

以下是多個 **SnmpRegister** 呼叫是多餘的實例。 在這些情況 \_ 下，如果函式順利完成，SNMPREGISTER 會傳回 SNMPAPI SUCCESS，但多餘的註冊會失效。

1.  呼叫 [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) 函式，在上一次呼叫 **SnmpRegister** 要求傳遞所有陷阱和通知 (未篩選的傳遞) 之後，要求將已篩選的陷阱和通知傳遞至會話。 此呼叫是重複的，因為會話已經接收所有陷阱和通知，包括篩選所定義的單一類型。
2.  對 **SnmpRegister** 的重複呼叫，或其中一個參數清單與先前呼叫中對該會話之 **SnmpRegister** 的參數清單相同。
3.  [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister)函式的呼叫會根據物件識別碼 (OID，要求篩選的陷阱和通知傳遞，) 其前置詞為先前對 **SnmpRegister** 的呼叫中指定的 oid。 例如，您可以在 *通知* 參數中指定 "1.3.6.1.4.1.311."，以接收來自任何 Microsoft SNMP 代理程式實體的通知。 如果您再次呼叫 **SnmpRegister** 並指定 "1.3.6.1.4.1.311.1"，則第二個呼叫是重複的，因為會話已經接收到所有包含 OID 首碼 "1.3.6.1.4.1.311." 的陷阱和通知。

若要取消註冊會話，您必須符合 [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) 函式的每個唯一註冊呼叫。 呼叫 **SnmpRegister** 以取消註冊會話，並確定 **SnmpRegister** 的前五個參數與初始註冊呼叫中的參數相同。 初始呼叫和取消註冊呼叫之間的唯一差異在於，當您註冊時，您必須 \_ 在 *status* 參數中指定 SNMPAPI 的值，而且當您呼叫函式以取消註冊時，您必須指定 SNMPAPI \_ OFF。 您不需要比對 **SnmpRegister** 函式的重複註冊呼叫。 您只需要符合第一個唯一的註冊電話。

若要變更篩選準則，應用程式可能需要先取消註冊並停用特定陷阱或通知的傳遞。 然後，應用程式可以藉由呼叫 [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister)並傳遞適當的值來建立新的篩選準則。

 

 




