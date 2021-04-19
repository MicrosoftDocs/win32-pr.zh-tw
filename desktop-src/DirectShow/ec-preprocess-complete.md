---
description: 當 WM ASF 寫入器篩選器完成 multipass 編碼的前置處理時傳送。
ms.assetid: 2029afc4-419c-494a-ae52-1f84b08bcb35
title: 'EC_PREPROCESS_COMPLETE (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba13938ac848ef37f1a2a2826372d97ff5a5d716
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000371"
---
# <a name="ec_preprocess_complete"></a>EC 前置處理 \_ \_ 完成

當 [WM ASF 寫入](wm-asf-writer-filter.md) 器篩選器完成 multipass 編碼的前置處理時傳送。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

零個。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

 (**IUnknown** \*) 指標指向篩選的 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)介面。

</dd> </dl>

## <a name="default-action"></a>預設動作

無。

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

 

 




