---
description: 由媒體資料流程啟動或停止 thinning 資料流程時引發。 如需 thinning 的詳細資訊，請參閱關於速率控制。
ms.assetid: 7de8cb64-122a-475f-990c-c19590a9d9d8
title: 'MEStreamThinMode 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 371c628498356f64918d42ffe6af94aef95af34005250ba3a4a891b6b76f6dc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013558"
---
# <a name="mestreamthinmode-event"></a>MEStreamThinMode 事件

由媒體資料流程啟動或停止 thinning 資料流程時引發。 如需 *thinning* 的詳細資訊，請參閱 [關於速率控制](about-rate-control.md)。

您可以傳送此事件以回應 [**IMFRateControl：： SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) 方法或 [**IMFQualityAdvise：： SetDropMode**](/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode) 方法。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>VARTYPE</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>VT_BOOL<br/></td>
<td>指出 thinning 是否已啟動或停止。<br/>
<ul>
<li>VARIANT_TRUE： thinned 此事件之後傳遞的範例。</li>
<li>VARIANT_FALSE：未 thinned 此事件之後傳遞的範例。</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




