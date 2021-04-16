---
description: 使用者使用者資訊是可從連接的一端傳輸到另一端的緩衝區。 這項資訊僅適用于 ISDN Q. 931 標準。 請參閱您的服務提供者檔，以說明這項資料的意義和使用。
ms.assetid: 7040ab51-184e-4ffc-9333-b82ae5a5a7f3
title: 使用者使用者資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4539db192b9c24b5d71dfb60a2129e66b6658b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513797"
---
# <a name="user-user-information"></a>使用者使用者資訊

使用者使用者資訊是可從連接的一端傳輸到另一端的緩衝區。 這項資訊僅適用于 ISDN Q. 931 標準。 請參閱您的服務提供者檔，以說明這項資料的意義和使用。

並非所有服務提供者都支援使用這項資訊。

* * TAPI 2.x： * *[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo)、 **dwCallDataSize** 和 **dwCallDataOffset** 成員 [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)， [**lineSendUserUserInfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)

* * TAPI 3.x： * *[**ITCallInfo：： GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer)，以 [**CALLINFO \_ BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)的 **CIB \_ USERUSERINFO** 成員呼叫 [**ITCallInfo：： ReleaseUserUserInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)

 

 
