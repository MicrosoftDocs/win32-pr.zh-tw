---
description: 當應用程式使用 WM ASF 寫入器篩選器來編制 Windows Media 視訊檔案的索引時傳送。
ms.assetid: e5f69aa1-f9b0-4403-acab-25d1f971a876
title: 'EC_WMT_INDEX_EVENT (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28e10b1d0e4a559bb10fbc521e232d08e08b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977507"
---
# <a name="ec_wmt_index_event-dshowh"></a>EC_WMT_INDEX_EVENT (Dshow) 

當應用程式使用 [WM ASF 寫入](wm-asf-writer-filter.md) 器篩選器來編制 Windows Media 視訊檔案的索引時傳送。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

可以是下列其中一項 **WMT \_ 狀態** 消息。



| 值                | 描述              |
|----------------------|--------------------------|
| WMT \_ 已開始         | 索引已開始。      |
| WMT \_ 已關閉          | 索引已完成。  |
| WMT \_ 索引 \_ 進度 | 正在編制索引。 |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

如果 *lParam1* 是 WMT \_ CLOSED 或 WMT \_ 開始，則 *lParam2* 為零。 如果 *lParam1* 是 WMT \_ INDEX \_ 進度，則 *lParam2* 為 **DWORD** ，會以總下載大小的百分比指定目前的進度。

</dd> </dl>

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

 

 




