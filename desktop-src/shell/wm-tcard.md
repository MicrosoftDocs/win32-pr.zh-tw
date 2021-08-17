---
description: 傳送至已使用 Windows 說明起始定型卡的應用程式。
title: 'WM_TCARD 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: fdde7603-9913-4e80-9502-2142ef8a511c
api_name:
- WM_TCARD
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 85435c5674ad6a2ac4e05edaa5d450dc61de9eac6dae05d3b19662aec91a61f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856983"
---
# <a name="wm_tcard-message"></a>WM \_ TCARD 訊息

傳送至已使用 Windows 說明起始定型卡的應用程式。 當使用者按一下 [authorable] 按鈕時，訊息會通知應用程式。 應用程式會在對 WinHelp 函式的 \_ 呼叫中指定 HELP TCARD 命令，以[](/windows/desktop/api/Winuser/nf-winuser-winhelpa)起始定型卡。

## <a name="parameters"></a>參數

<dl> <dt>

*idAction* 
</dt> <dd>

值，指出使用者已採取的動作。 這可以是下列其中一個值。

<dt>

<span id="IDABORT"></span><span id="idabort"></span>

<span id="IDABORT"></span><span id="idabort"></span>**IDABORT**


</dt> <dd>

使用者按一下 [authorable **中止** ] 按鈕。

</dd> <dt>

<span id="IDCANCEL"></span><span id="idcancel"></span>

<span id="IDCANCEL"></span><span id="idcancel"></span>**IDCANCEL**


</dt> <dd>

使用者按一下 [authorable **取消** ] 按鈕。

</dd> <dt>

<span id="IDCLOSE"></span><span id="idclose"></span>

<span id="IDCLOSE"></span><span id="idclose"></span>**IDCLOSE**


</dt> <dd>

使用者已關閉訓練卡。

</dd> <dt>

<span id="IDHELP"></span><span id="idhelp"></span>

<span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**


</dt> <dd>

使用者按一下 **authorable Windows [** 說明] 按鈕。

</dd> <dt>

<span id="IDIGNORE"></span><span id="idignore"></span>

<span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**


</dt> <dd>

使用者按一下 authorable [ **略** 過] 按鈕。

</dd> <dt>

<span id="IDOK"></span><span id="idok"></span>

<span id="IDOK"></span><span id="idok"></span>**IDOK**


</dt> <dd>

使用者按一下 [authorable **確定]** 按鈕。

</dd> <dt>

<span id="IDNO"></span><span id="idno"></span>

<span id="IDNO"></span><span id="idno"></span>**IDNO**


</dt> <dd>

使用者按一下 authorable **No** button。

</dd> <dt>

<span id="IDRETRY"></span><span id="idretry"></span>

<span id="IDRETRY"></span><span id="idretry"></span>**IDRETRY**


</dt> <dd>

使用者按一下 authorable **重試** 按鈕。

</dd> <dt>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**協助 \_ TCARD \_ 資料**


</dt> <dd>

使用者按一下 [authorable] 按鈕。 *DwActionData* 參數包含由說明作者指定的長整數。

</dd> <dt>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**協助 \_ TCARD \_ 其他 \_ 呼叫者**


</dt> <dd>

另一個應用程式已要求定型卡。

</dd> <dt>

<span id="IDYES"></span><span id="idyes"></span>

<span id="IDYES"></span><span id="idyes"></span>**IDYES**


</dt> <dd>

使用者按一下 [authorable **是]** 按鈕。

</dd> </dl> </dd> <dt>

*dwActionData* 
</dt> <dd>

如果 *idAction* 指定 help \_ TCARD \_ 資料，則此參數是由說明作者指定的 **長整數** 。 否則，此參數為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略;使用零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Winuser。h</dt> </dl> |



 

 




