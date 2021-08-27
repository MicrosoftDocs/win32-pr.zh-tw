---
description: 抓取 Windows 工作列的自動隱藏和 alwayson 狀態。
title: 'ABM_GETSTATE 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 18e16752-16be-492b-a4fa-c951e18dc86c
api_name:
- ABM_GETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1ced01e3f8186a82e99f408f91546ebcbb117ed9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466385"
---
# <a name="abm_getstate-message"></a>ABM \_ >getstate 訊息

抓取 Windows 工作列的自動隱藏和 alwayson 狀態。


```C++
uState = (UINT) SHAppBarMessage(ABM_GETSTATE, pabd);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pabd* 
</dt> <dd>

[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標。 傳送此訊息時，您必須指定 **cbSize** 成員;所有其他成員都會被忽略。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果工作列不是自動隱藏或不在最上層狀態，則傳回零。 否則，傳回值是下列其中一項或兩項：




| 傳回碼 | Description | 
|-------------|-------------|
| <dl><dt><strong>ABS_ALWAYSONTOP</strong></dt></dl> | 工作列處於 always on 最上層狀態。 <br /><blockquote>[!Note]<br />從 Windows 7，因為工作列一律處於該狀態，所以不會再傳回 ABS_ALWAYSONTOP。 您應該更新較舊的程式碼，以忽略此值不存在的情況下，不假設該傳回值表示工作列不是處於最新狀態。</blockquote><br /> | 
| <dl><dt><strong>ABS_AUTOHIDE</strong></dt></dl> | 工作列處於 [自動隱藏] 狀態。<br /> | 




 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Shellapi。h</dt> </dl> |



 

 




