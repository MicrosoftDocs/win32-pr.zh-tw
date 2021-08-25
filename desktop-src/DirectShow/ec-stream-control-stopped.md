---
description: 資料流程控制停止命令已生效。
ms.assetid: a2f7a959-fafd-47ff-9b3d-1a898fdb1f81
title: 'EC_STREAM_CONTROL_STOPPED (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69884ecc573b2bb775092529cb81e1b33a1514d4799af9f55c7bcebb5ebd2b24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928418"
---
# <a name="ec_stream_control_stopped"></a>EC \_ 資料流程 \_ 控制 \_ 已停止

資料流程控制停止命令已生效。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*
</dt> <dd>

 (**IUnknown** \*) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)介面的指標，指向停止資料流程的 pin。

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*
</dt> <dd>

 (**DWORD**) 使用者定義值。

</dd> </dl>

## <a name="default-action"></a>預設動作

無。

## <a name="remarks"></a>備註

篩選準則會傳送此事件以回應 [**IAMStreamControl：： StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) 方法。 **StopAt** 方法會指定 pin 的參考時間以停止串流。 當串流處理中斷時，篩選會傳送此事件。

*PSender* 參數會指定執行 stop 命令的 pin。 根據執行方式而定，它可能不是收到 [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) 呼叫的 pin。

*DwCookie* 參數是由應用程式在 [**StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat)方法中指定。 此參數可讓應用程式追蹤對方法的多個呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dshow。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[事件通知碼](event-notification-codes.md)
</dt> <dt>

[DirectShow 中的事件通知](event-notification-in-directshow.md)
</dt> </dl>

 

 




