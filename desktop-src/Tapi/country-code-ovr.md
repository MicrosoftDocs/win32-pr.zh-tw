---
description: 只有當地址類型是 LINEADDRESSTYPE PHONENUMBER 時，國家或地區碼才會相關 \_ 。 它會識別全世界的領域。
ms.assetid: d838c2ac-4ee3-4314-8573-deed6c7430e3
title: 國家或地區碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5557e4d67b701fda2aa05ad81686ae474b172063
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848283"
---
# <a name="country-or-region-code"></a>國家或地區碼

只有當地址類型是 LINEADDRESSTYPE PHONENUMBER 時，國家或地區碼才會相關 \_ 。 它會識別全世界的領域。

所有支援使用電話號碼的服務提供者都必須支援此資訊的使用。

**TAPI 2.x：** 請參閱 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**DwCountryCode** 成員的 *lpCallInfo*) 。

**TAPI 3.x：** 請參閱 [**ITCallInfo：： get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) ([**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)) 的 **CIL \_ COUNTRYCODE** 成員。

 

 
