---
description: 圖形正在開啟檔案，或已完成檔案的開啟。
ms.assetid: 352867e1-025f-4adb-be32-f7941c0ec8cf
title: 'EC_OPENING_FILE (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 436a48a90640577504871dfe835d6c81c398680ae070065189cb4031493e7fc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079118"
---
# <a name="ec_opening_file"></a>EC \_ 開啟 \_ 檔案

圖形正在開啟檔案，或已完成檔案的開啟。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

如果圖形正在開始開啟檔案，則 **為 TRUE** ; 如果圖形不再開啟檔案，則為 **FALSE** 。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="default-action"></a>預設動作

無。

## <a name="remarks"></a>備註

如果篩選準則花了很長的時間來開啟檔案，則篩選準則可以傳送此事件。  (例如，檔案可能位於網路上。 ) 應用程式可以使用此事件來調整其使用者介面。

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

 

 




