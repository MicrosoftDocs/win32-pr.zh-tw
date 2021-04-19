---
description: '\_當指定之呼叫的相關呼叫資訊已變更時，就會傳送 TAPI 線路 CALLINFO 訊息。 應用程式可以叫用 lineGetCallInfo 來判斷目前的呼叫資訊。'
ms.assetid: eb882409-6842-434e-9f93-61cf0c11d1d0
title: 'LINE_CALLINFO 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6005ab5383816ead440f5a1a7d580bfaccb5c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995301"
---
# <a name="line_callinfo-message"></a>行 \_ CALLINFO 訊息

當指定之呼叫的相關呼叫資訊已變更時，就會傳送 TAPI **線路 \_ CALLINFO** 訊息。 應用程式可以叫用 [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) 來判斷目前的呼叫資訊。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

呼叫的控制碼。

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

開啟呼叫的行時所提供的回呼實例。

</dd> <dt>

*dwParam1* 
</dt> <dd>

已變更的呼叫資訊專案。 可以是一或多個 [**LINECALLINFOSTATE \_ 常數**](linecallinfostate--constants.md)。

</dd> <dt>

*dwParam2* 
</dt> <dd>

未使用的。

</dd> <dt>

*dwParam3* 
</dt> <dd>

未使用的。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

具有 *NumOwnersIncr*、 *NumOwnersDecr* 和/或 *NumMonitorsChanged* 指示的 **行 \_ CALLINFO** 訊息會傳送給已經有呼叫控制碼的應用程式。 這可能是因為另一個應用程式將擁有權或 monitorship 變更為使用 [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)、 [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)、 [**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)、 [**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)、 [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)和 [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)的呼叫所造成。

在 [**行 \_ CALLSTATE**](line-callstate.md)訊息中提供新呼叫的通知時，不會傳送這些 **行 \_ CALLINFO** 訊息，因為呼叫資訊已在 \_ 傳送 CALLSTATE 訊息行時反映正確的擁有者和監視器數目。 **行 \_** 透過 LINECALLSTATE 的未知機制，透過 TAPI 提供的呼叫來監視，也會抑制 CALLINFO 訊息 \_ 。

> [!Note]  
> 導致擁有者或監視器數目變更的應用程式 (例如，藉由叫用 [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) 或 [**LineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)) 不會收到訊息，指出已完成變更。

 

呼叫進入 *閒置* 狀態之後，就不會傳送呼叫的 **行 \_ CALLINFO** 訊息。 具體而言，擁有者和監視數目的變更並不會回報，因為應用程式會解除配置其閒置呼叫的控制碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls)
</dt> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineSetCallPrivilege**](/windows/desktop/api/Tapi/nf-tapi-linesetcallprivilege)
</dt> <dt>

[**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> </dl>

 

 




