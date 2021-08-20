---
description: 相容性緩衝區是針對 ISDN 931 標準所特有。 請參閱您的服務提供者檔，以說明這項資料的意義和使用。
ms.assetid: c4c87ca8-fbae-4275-9b69-7b32daf4c18f
title: 相容性緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 739063a6570a93b1fb05442ebe3f6ec10a040626ba7a0fe4b9692d7e5636b5ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117946590"
---
# <a name="compatibility-buffer"></a>相容性緩衝區

相容性緩衝區是針對 ISDN 931 標準所特有。 請參閱您的服務提供者檔，以說明這項資料的意義和使用。

並非所有服務提供者都支援使用這項資訊。

**TAPI 2.x：** 請參閱 *dwLowLevelCompOffset*) 的 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwHighLevelCompSize**、 **dwHighLevelCompOffset**、 **dwLowLevelCompSize** 和 **lpCallInfo** 成員。

**TAPI 3.x：** 請參閱 [**CIB \_ 緩衝區**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)) 的 [**ITCallInfo：： get \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfobuffer) (**CIB \_ HIGHLEVELCOMPATIBILITYBUFFER** 和 **LOWLEVELCOMPATIBILITYBUFFER \_ CALLINFO** 成員。

 

 
