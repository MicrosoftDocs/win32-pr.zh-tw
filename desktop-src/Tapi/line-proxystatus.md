---
description: '\_當應用程式目前開啟的那一行上的可用 proxy 變更時，就會傳送 line PROXYSTATUS 訊息。'
ms.assetid: e20d4b48-a72a-4a83-ae04-a608791a1a3a
title: 'LINE_PROXYSTATUS 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 585feda6194a13ecfbe17292aadb9036784d244c9ee5b7df4361981ab7401f65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682348"
---
# <a name="line_proxystatus-message"></a>行 \_ PROXYSTATUS 訊息

當應用程式目前開啟的那一行上的可用 proxy 變更時，就會傳送 **line \_ PROXYSTATUS** 訊息。

TAPISRV 會在使用 LINEPROXYSTATUS OPEN 和 LINEPROXYSTATUS ALLOPENFORACD 的 [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)函式中 \_ ， \_ 或 [](/windows/desktop/api/Tapi/nf-tapi-lineclose)使用 lineClose \_ CLOSE (所有 [**LINEPROXYSTATUS \_ 常數**](lineproxystatus--constants.md)) 來產生此訊息。


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

指定已變更的佇列狀態。 可以是一或多個 [**LINEPROXYSTATUS \_ 常數**](lineproxystatus--constants.md)。

</dd> <dt>

*dwParam2* 
</dt> <dd>

如果 *dwParam1* 設為 LINEPROXYSTATUS \_ OPEN 或 LINEPROXYSTATUS \_ CLOSE， *dwParam2* 會指出相關的 proxy 要求類型，也就是下列其中一項：

-   LINEPROXYREQUEST \_ SETAGENTGROUP
-   LINEPROXYREQUEST \_ SETAGENTSTATE
-   LINEPROXYREQUEST \_ SETAGENTACTIVITY
-   LINEPROXYREQUEST \_ GETAGENTCAPS
-   LINEPROXYREQUEST \_ GETAGENTSTATUS
-   LINEPROXYREQUEST \_ AGENTSPECIFIC
-   LINEPROXYREQUEST \_ GETAGENTACTIVITYLIST
-   LINEPROXYREQUEST \_ GETAGENTGROUPLIST
-   LINEPROXYREQUEST \_ CREATEAGENT
-   LINEPROXYREQUEST \_ SETAGENTMEASUREMENTPERIOD
-   LINEPROXYREQUEST \_ GETAGENTINFO
-   LINEPROXYREQUEST \_ CREATEAGENTSESSION
-   LINEPROXYREQUEST \_ GETAGENTSESSIONLIST
-   LINEPROXYREQUEST \_ SETAGENTSESSIONSTATE
-   LINEPROXYREQUEST \_ GETAGENTSESSIONINFO
-   LINEPROXYREQUEST \_ GETQUEUELIST
-   LINEPROXYREQUEST \_ SETQUEUEMEASUREMENTPERIOD
-   LINEPROXYREQUEST \_ GETQUEUEINFO
-   LINEPROXYREQUEST \_ GETGROUPLIST
-   LINEPROXYREQUEST \_ SETAGENTSTATEEX

否則， *dwParam2* 會設為零。

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

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**行 \_ PROXYREQUEST**](line-proxyrequest.md)
</dt> <dt>

[**LINEPROXYREQUEST \_ 常數**](lineproxyrequest--constants.md)
</dt> </dl>

 

 




