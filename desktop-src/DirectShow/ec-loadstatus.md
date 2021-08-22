---
description: 開啟網路檔案時，通知應用程式的進度。
ms.assetid: 022b87e5-76af-4253-9485-97140f294938
title: 'EC_LOADSTATUS (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499f05a26f3fa1387347929f5c14a64b1f440a53ed9b5fd17830d582fb640c3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015936"
---
# <a name="ec_loadstatus"></a>EC \_ LOADSTATUS

開啟網路檔案時，通知應用程式的進度。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

狀態碼。 請參閱＜備註＞。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="default-action"></a>預設動作

無。

## <a name="remarks"></a>備註

[WM ASF 讀取](wm-asf-reader-filter.md)器篩選器和舊版[Windows 媒體來源](windows-media-source-filter.md)篩選器會傳送此事件。 第一個事件參數具有下列其中一個值。



| 值                        | 描述                                    |
|------------------------------|------------------------------------------------|
| \_LOADSTATUS \_ 已關閉       | 來源篩選器已關閉檔案。         |
| AM \_ LOADSTATUS \_ 連接   | 來源篩選器正在連接到伺服器。 |
| AM \_ LOADSTATUS \_ LOADINGDESCR | 未使用。                                      |
| AM \_ LOADSTATUS \_ LOADINGMCAST | 未使用                                       |
| AM \_ LOADSTATUS \_ 尋找     | 來源篩選器正在尋找要求的資料。  |
| \_LOADSTATUS \_ 開啟         | 來源篩選已開啟檔案。         |
| AM \_ LOADSTATUS \_ 開啟      | 來源篩選器正在開啟檔案。         |



 

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

 

 




