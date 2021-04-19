---
description: 資料流程控制項啟動命令已生效。
ms.assetid: e2f8d9a2-c96c-457c-8a88-7c86d4405928
title: 'EC_STREAM_CONTROL_STARTED (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 984562fde9001de14067e5865d5583636b264852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990558"
---
# <a name="ec_stream_control_started"></a>\_已開始使用 EC 資料流程 \_ 控制項 \_

資料流程控制項啟動命令已生效。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*
</dt> <dd>

 (**IUnknown** \*) 指標指向啟動資料流程的 pin [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)介面。

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*
</dt> <dd>

 (**DWORD**) 使用者定義值。

</dd> </dl>

## <a name="default-action"></a>預設動作

無。

## <a name="remarks"></a>備註

篩選準則會傳送此事件以回應 [**IAMStreamControl：： StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) 方法。 這個方法會指定 pin 開始串流的參考時間。 串流處理開始時，篩選準則會傳送此事件。

*PSender* 參數會指定執行 start 命令的 pin。 根據執行方式而定，它可能不是收到 [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) 呼叫的 pin。

*DwCookie* 參數是由應用程式在 [**StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat)方法中指定。 此參數可讓應用程式追蹤對方法的多個呼叫。

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

 

 




