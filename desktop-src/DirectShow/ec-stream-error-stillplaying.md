---
description: 資料流程中發生錯誤，但是資料流程仍在播放中。
ms.assetid: ff155c01-22ba-46dd-85b8-05eabf956908
title: 'EC_STREAM_ERROR_STILLPLAYING (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db74a9f16a0ca01ce74e6d94df50cc402221aaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984026"
---
# <a name="ec_stream_error_stillplaying"></a>EC \_ 資料流程 \_ 錯誤 \_ STILLPLAYING

資料流程中發生錯誤，但是資料流程仍在播放中。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

 (**HRESULT**) 失敗之作業的失敗碼。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

 (**DWORD**) 次要錯誤碼。 此值通常是零。

</dd> </dl>

## <a name="default-action"></a>預設動作

無。 應用程式必須決定是否要停止圖形。

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

 

 




