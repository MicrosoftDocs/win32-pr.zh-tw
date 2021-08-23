---
description: 連接的識別會識別實際連接的合作物件。 如果呼叫轉向，這可能與被呼叫的識別碼不同。
ms.assetid: 3f9ba728-8e78-4f1f-a0c1-76799fd62c9d
title: 連接的識別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df3052287658d06372f30c9d1fa5ae79c13ab0f7ff10dd9c134b7f730439cc6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118867755"
---
# <a name="connected-identification"></a>連接的識別

連接的識別會識別實際連接的合作物件。 如果呼叫轉向，這可能與被呼叫的識別碼不同。

並非所有服務提供者都支援使用這項資訊。

**TAPI 2.x：** 請參閱 *dwConnectedIDNameSize*) 的 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwConnectedIDFlags**、 **dwConnectedIDSize**、 **dwConnectedIDOffset**、 **dwConnectedIDNameOffset** 和 **lpCallInfo** 成員。

**TAPI 3.x：** 請參閱 [**ITCallInfo：： get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) ([**CALLINFO \_ STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)) 的 **CIL \_ CONNECTEDIDNAME** 成員。

 

 
