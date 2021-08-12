---
title: 'TB_GETBUTTONINFO 訊息 (Commctrl .h) '
description: 抓取工具列中按鈕的擴充資訊。
ms.assetid: 87430dd2-43d1-4e33-96ac-d33f89a654b6
keywords:
- TB_GETBUTTONINFO 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETBUTTONINFO
- TB_GETBUTTONINFOA
- TB_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 457b8ca82d570b9d6c55cf97392803fce9a81cbe1d5db8122fcdaa975dd99d5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669931"
---
# <a name="tb_getbuttoninfo-message"></a>TB \_ GETBUTTONINFO 訊息

抓取工具列中按鈕的擴充資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

按鈕的命令識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>

接收按鈕資訊之 [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) 結構的指標。 在傳送此訊息之前，必須先填入此結構的 **cbSize** 和 **dwMask** 成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回按鈕的以零為起始的索引; 如果發生錯誤，則為-1。

## <a name="remarks"></a>備註

當您使用 [**TB \_ ADDBUTTONS**](tb-addbuttons.md) 或 [**tb \_ INSERTBUTTON**](tb-insertbutton.md) 將按鈕放在工具列上時，按鈕文字通常是由其字串集區索引所指定。 **TB \_GETBUTTONINFO** 將不會取得此字串。 若要使用 **tb \_ GETBUTTONINFO** 來抓取按鈕文字，您必須先設定具有 [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md)的文字字串。 將按鈕文字設定為 [TB] **\_ SETBUTTONINFO** 之後，就無法再使用字串集區索引。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TB \_GETBUTTONINFOW** (Unicode) 和 **TB \_ GETBUTTONINFOA** (ANSI) <br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md)
</dt> <dt>

[**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)
</dt> </dl>

 

 





