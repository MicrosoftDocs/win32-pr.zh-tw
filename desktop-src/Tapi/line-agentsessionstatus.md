---
description: '\_當應用程式目前有開啟行的代理程式處理常式上的 ACD 代理程式會話狀態有所變更時，就會傳送 LINE AGENTSESSIONSTATUS 訊息。 此訊息是使用 lineProxyMessage 函式所產生。'
ms.assetid: bb9d2292-8c41-4557-989e-6c5eb785313f
title: 'LINE_AGENTSESSIONSTATUS 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d53c14290dfb6bda3889e7d2b87d8d3ca5e651c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993590"
---
# <a name="line_agentsessionstatus-message"></a>行 \_ AGENTSESSIONSTATUS 訊息

當應用程式目前有開啟行的代理程式處理常式上的 ACD 代理程式會話狀態有所變更時，就會傳送 **LINE \_ AGENTSESSIONSTATUS** 訊息。 此訊息是使用 [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) 函式所產生。


```C++
        
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwDevice* 
</dt> <dd>

應用程式的控制碼，指向代理程式會話狀態已變更的線路裝置。

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

開啟行時所提供的回呼實例。

</dd> <dt>

*dwParam1* 
</dt> <dd>

已變更其狀態的代理程式會話控制碼。

</dd> <dt>

*dwParam2* 
</dt> <dd>

指定已變更的代理程式會話狀態。 可以是一或多 **行 \_ AGENTSESSIONSTATUS**。

</dd> <dt>

*dwParam3* 
</dt> <dd>

如果 *dwParam2* 包含 LINEAGENTSTATUSEX \_ 狀態位， *dwParam3* 就會指出代理程式狀態的新值，也就是其中一個 [**LINEAGENTSTATEEX \_ 常數**](lineagentstateex--constants.md)。

否則， *dwParam3* 會設為零。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2。2<br/>                                                      |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**lineGetAgentSessionInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo)
</dt> <dt>

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




