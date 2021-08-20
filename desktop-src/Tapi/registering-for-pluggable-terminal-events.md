---
description: 當資料流程選取終端機時，就會發生事件註冊程式。
ms.assetid: 03854b38-4dba-480e-b931-34299d04c551
title: 註冊可插入的終端機事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c71993d597cbcba7c634068813eb14939539dc7e7d43cda0105e8cf9ee615a1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060456"
---
# <a name="registering-for-pluggable-terminal-events"></a>註冊可插入的終端機事件

當資料流程選取終端機時，就會發生事件註冊程式。 在終端機應用程式的 [**SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) 方法執行中，我們可以使用已附加至資料流程的終端機 [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) 介面，然後呼叫 **QueryInterface** 來尋找 [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration)。

``` syntax
HRESULT hr = E_FAIL;
ITPluggableTerminalEventSinkRegistration* pEventRegistration = NULL;
hr = pTerminal->QueryInterface( 
    IID_ITPluggableTerminalEventSinkRegistration,
    (void**)& pEventRegistration
);
```

如果 **QueryInterface** 呼叫成功，我們可以呼叫 [**RegisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-registersink) 方法。 基於這個目的，我們應該建立可執行 [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink) 介面的物件。 我們會將此介面傳遞為 **RegisterSink** 方法的參數。

``` syntax
ITPluggableTerminalEventSink*    pEventSink;

HRESULT hr = CreateEventSink( &pEventSink);
// If (hr != S_OK) process the error here. 

hr = pEventRegistration->RegisterSink( pEventSink );
// If (hr != S_OK) process the error here. 
```

執行 [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration) 呼叫的終端機將會儲存介面。 當終端機將會引發事件時，將會使用指標。

您可以使用 [**UnregisterSink**](/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink)取消註冊事件接收器。

``` syntax
hr = pEventRegistration->UnregisterSink();
// If (hr != S_OK) process the error here.
```

 

 
