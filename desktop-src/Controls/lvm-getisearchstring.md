---
title: 'LVM_GETISEARCHSTRING 訊息 (Commctrl .h) '
description: 抓取清單視圖控制項的遞增搜尋字串。 您可以明確地傳送此訊息，或使用 ListView \_ GetISearchString 宏來傳送。
ms.assetid: e953c4a0-0556-4987-8abf-3276e787fe49
keywords:
- LVM_GETISEARCHSTRING message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETISEARCHSTRING
- LVM_GETISEARCHSTRINGA
- LVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9040cf96c5c483b29764b1ccfb67e0e4fff3f897
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466513"
---
# <a name="lvm_getisearchstring-message"></a>LVM \_ GETISEARCHSTRING 訊息

抓取清單視圖控制項的遞增搜尋字串。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

接收累加式搜尋字串的緩衝區指標。 若要只取出字串的長度，請將 *lParam* 設定為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回累加式搜尋字串中的字元數，不包括結束的 Null 字元，或如果清單視圖控制項不在累加式搜尋模式中，則為零。

## <a name="remarks"></a>備註

**安全性警告：** 不當使用此訊息可能會危及程式的安全性。 此訊息不會提供您知道緩衝區大小的方法。 如果您使用此訊息，請先呼叫在 *lParam* 中傳遞 **null** 的訊息，這會傳回字元數，但不包括需要的 **null** 。 然後第二次呼叫訊息以抓取字串。 您應該先複習 [安全性考慮： Microsoft Windows 控制項](sec-comctls.md) ，再繼續進行。

*增量搜尋字串* 是使用者輸入的字元序列，而清單視圖則具有輸入焦點。 每次使用者輸入一個字元時，系統會將字元附加到搜尋字串，然後搜尋相符的專案。 如果系統找到相符專案，則會選取專案，並視需要將它滾動至 view。

超時期間是與使用者輸入的每個字元相關聯。 如果在使用者鍵入另一個字元之前經過超時時間，則會重設增量搜尋字串。

請確定緩衝區夠大，足以容納字串和終止的 Null 字元。 如果太小，則會產生立即不正確分頁錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **LVM \_GETISEARCHSTRINGW** (Unicode) 和 **LVM \_ GETISEARCHSTRINGA** (ANSI) <br/> |



 

 





