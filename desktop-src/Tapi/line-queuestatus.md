---
description: '\_當應用程式目前有開啟行的代理程式處理常式上的 ACD 佇列狀態變更時，就會傳送 LINE system.printing.printqueue.queuestatus 訊息。 此訊息是使用 lineProxyMessage 函式所產生。'
ms.assetid: 9baacfc5-f26c-41c7-a1f8-f48ec8aa844c
title: 'LINE_QUEUESTATUS 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a89785b92009a7531ae693545febaf153cf19bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983067"
---
# <a name="line_queuestatus-message"></a>行 \_ system.printing.printqueue.queuestatus 訊息

當應用程式目前有開啟行的代理程式處理常式上的 ACD 佇列狀態變更時，就會傳送 **LINE \_ system.printing.printqueue.queuestatus** 訊息。 此訊息是使用 [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) 函式所產生。


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

其狀態已變更之佇列的識別碼。

</dd> <dt>

*dwParam2* 
</dt> <dd>

指定已變更的佇列狀態。 可以是一或多個 [**LINEQUEUESTATUS \_ 常數**](linequeuestatus--constants.md)。

</dd> <dt>

*dwParam3* 
</dt> <dd>

保留的。 設定為零。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2。2<br/>                                                      |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




