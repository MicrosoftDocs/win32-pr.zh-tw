---
description: 許可權指的是應用程式擁有或正在監視會話。
ms.assetid: 0c02a88a-370f-4eb9-ba64-07a382bd2e87
title: Privilege
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2f773edb05afc029a8f9fb6b014cd8a737eef0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971523"
---
# <a name="privilege"></a>Privilege

許可權指的是應用程式擁有或正在監視會話。 如果應用程式擁有會話，就可以執行各種會話作業。 如果應用程式只是監視，它就會接收狀態訊息，而且它可以存取會話資訊，但任何嘗試執行大部分的作業都會導致錯誤。

在初始化期間，應用程式會告知 TAPI 所需的許可權層級在哪個位址上。 TAPI 僅針對已註冊擁有者或擁有者和監視許可權的應用程式，提供連入會話。

應用程式在其建立的會話上的許可權一律為擁有者。

**TAPI 2.x：** 請參閱 [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus)、 **DwCallPrivilege** member of [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus)、 [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege)。

**TAPI 3.x：** 請參閱 [**ITCallInfo：： get \_ 許可權**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege)、 [**ITCallInfo：： \_ get CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)（以 **CIL \_ NUMBEROFOWNERS** 或 [**NUMBEROFMONITORS \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)的 **cil \_ CALLINFO** 成員呼叫）。

 

 
