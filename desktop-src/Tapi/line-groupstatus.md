---
description: '\_當應用程式目前有開啟行的代理程式處理常式上發生 ACD 群組的狀態變更時，就會傳送 LINE GROUPSTATUS 訊息。 此訊息是使用 lineProxyMessage 函式所產生。'
ms.assetid: 1f3210fe-a7c8-4cfa-8e36-3a88e93d68bb
title: 'LINE_GROUPSTATUS 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22fec7c4701ee7140c02cede1901ef7998e5b60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992897"
---
# <a name="line_groupstatus-message"></a>行 \_ GROUPSTATUS 訊息

當應用程式目前有開啟行的代理程式處理常式上發生 ACD 群組的狀態變更時，就會傳送 **LINE \_ GROUPSTATUS** 訊息。 此訊息是使用 [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) 函式所產生。


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

保留的。 設定為零。

</dd> <dt>

*dwParam2* 
</dt> <dd>

指定已變更的群組狀態。 應用程式可以叫用 [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) 來判斷可用群組中的變更。 *DwParam2* 參數是一或多個 [**LINEGROUPSTATUS \_ 常數**](linegroupstatus--constants.md)。

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

[**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista)
</dt> </dl>

 

 




