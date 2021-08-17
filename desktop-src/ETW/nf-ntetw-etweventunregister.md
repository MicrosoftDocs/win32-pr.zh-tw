---
UID: NF:ntw.EtwEventUnregister
title: EtwEventUnregister 函式
description: 取消註冊事件。
old-location: ''
ms.assetid: na
ms.date: 02/20/2018
ms.keywords: EtwEventUnregister
ms.topic: reference
req.header: ntetw.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 10, version 1803 [desktop apps \| UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- ntetw.h
api_name:
- EtwEventUnregister
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: f2918aa3eb5ca3440496aa1f6ef51363045d5b8704b8b6fca059e68ba19a112d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070098"
---
# <a name="etweventunregister-function"></a>EtwEventUnregister 函式


## <a name="description"></a>描述


<b>EtwEventUnregister</b>會取消註冊事件。
            

提供者只能從其 <a href="/windows/desktop/ETW/controlcallback">ControlCallback</a> 函式呼叫這個函數。


## <a name="parameters"></a>參數




### <a name="reghandle-in"></a>RegHandle [in]

事件的控制代碼。


## <a name="returns"></a>傳回



傳回 HRESULT。





## <a name="remarks"></a>備註



## <a name="see-also"></a>另請參閱