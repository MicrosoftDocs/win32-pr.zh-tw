---
description: 執行圖形的非同步命令失敗。
ms.assetid: 0bfcf4b4-b35a-4593-9956-8e1e8c9139cb
title: 'EC_ERROR_STILLPLAYING (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82383c541f2ba5294cf4d45844f096ff510f25444ce87a54b956d0a777a7fc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051778"
---
# <a name="ec_error_stillplaying"></a>EC \_ 錯誤 \_ STILLPLAYING

執行圖形的非同步命令失敗。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

 (**HRESULT**) 失敗之作業的失敗碼。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="default-action"></a>預設動作

無。

## <a name="remarks"></a>備註

如果篩選圖形管理員發出的非同步執行命令失敗，則會將此事件傳送至應用程式。 圖形仍處於執行中狀態。 基礎篩選準則的狀態不確定。 某些篩選器可能正在執行，其他篩選器可能不會執行。

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

 

 




