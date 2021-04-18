---
description: '\_當應用程式目前有開啟行的代理程式處理常式上的 ACD 代理程式狀態變更時，就會傳送 LINE AGENTSTATUSEX 訊息。 此訊息是使用 lineProxyMessage 函式產生的。'
ms.assetid: a0709367-9105-43af-9772-0161d94c098a
title: 'LINE_AGENTSTATUSEX 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c9ff1a39fd6aacf69922693a54198426d267720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976187"
---
# <a name="line_agentstatusex-message"></a>行 \_ AGENTSTATUSEX 訊息

當應用程式目前有開啟行的代理程式處理常式上的 ACD 代理程式狀態變更時，就會傳送 **LINE \_ AGENTSTATUSEX** 訊息。 此訊息是使用 [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) 函式產生的。


```C++
        
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwDevice* 
</dt> <dd>

應用程式線路裝置的控制碼。 這與代理程式處理常式相關。

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

開啟行時所提供的回呼實例。

</dd> <dt>

*dwParam1* 
</dt> <dd>

狀態已變更之代理程式的控制碼。

</dd> <dt>

*dwParam2* 
</dt> <dd>

指定已變更的佇列狀態。 可以是一或多個 [**LINEQUEUESTATUS \_ 常數**](linequeuestatus--constants.md)。

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

[**lineGetAgentInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo)
</dt> <dt>

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




