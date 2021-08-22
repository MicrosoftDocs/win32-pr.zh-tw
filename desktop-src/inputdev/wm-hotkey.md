---
title: 'WM_HOTKEY 訊息 (Winuser .h) '
description: 當使用者按下 RegisterHotKey 函式所註冊的快速鍵時張貼。 訊息會放在與註冊快速鍵之執行緒相關聯的訊息佇列頂端。
ms.assetid: 28d87c2f-b2bb-4176-910b-0addea6beb93
keywords:
- WM_HOTKEY 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_HOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51dbd37b61fea12e559323a73cbf6b4a5cb54704a74663f865d9aa89636d3c46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119557138"
---
# <a name="wm_hotkey-message"></a>WM \_ 熱鍵訊息

當使用者按下 [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) 函式所註冊的快速鍵時張貼。 訊息會放在與註冊快速鍵之執行緒相關聯的訊息佇列頂端。


```C++
#define WM_HOTKEY                       0x0312
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

產生訊息之快速鍵的識別碼。 如果訊息是由系統定義的熱鍵產生，此參數將會是下列其中一個值。



| 值                                                                                                                                                                                                                             | 意義                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="IDHOT_SNAPDESKTOP"></span><span id="idhot_snapdesktop"></span><dl> <dt>**IDHOT \_SNAPDESKTOP**</dt> <dt>-2</dt> </dl> | 已按下 [貼齊桌面] 快速鍵。<br/> |
| <span id="IDHOT_SNAPWINDOW"></span><span id="idhot_snapwindow"></span><dl> <dt>**IDHOT \_SNAPWINDOW**</dt> <dt>-1</dt> </dl>    | 已按下 [貼齊視窗] 快速鍵。<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

低序位單字可指定要與高序位字組指定的按鍵組合使用的索引鍵，以產生 **WM 的 \_ 熱鍵** 訊息。 這個單字可以是下列一或多個值。 高序位字組指定熱鍵的虛擬按鍵碼。



| 值                                                                                                                                                                                                               | 意義                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MOD_ALT"></span><span id="mod_alt"></span><dl> <dt>**MOD \_ALT**</dt> <dt>0x0001</dt> </dl>             | 任一個 ALT 鍵已關閉。<br/>                                                                                                                                      |
| <span id="MOD_CONTROL"></span><span id="mod_control"></span><dl> <dt>**MOD \_控制項**</dt> <dt>0x0002</dt> </dl> | 其中一個 CTRL 鍵已關閉。<br/>                                                                                                                                     |
| <span id="MOD_SHIFT"></span><span id="mod_shift"></span><dl> <dt>**MOD \_SHIFT**</dt> <dt>0x0004</dt> </dl>       | 任一個 SHIFT 鍵已關閉。<br/>                                                                                                                                    |
| <span id="MOD_WIN"></span><span id="mod_win"></span><dl> <dt>**MOD \_WIN**</dt> <dt>0x0008</dt> </dl>             | 其中一個 WINDOWS 機碼已關閉。 這些金鑰會以 Windows 標誌標記。 牽涉到 Windows 金鑰的快速鍵會保留給作業系統使用。<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

**WM \_熱鍵** 與 [**wm \_ GETHOTKEY**](wm-gethotkey.md) 和 [**wm \_ SETHOTKEY**](wm-sethotkey.md) 快速鍵無關。 當 **wm \_ SETHOTKEY** 和 **wm \_ GETHOTKEY** 訊息與視窗啟用熱鍵相關時，會傳送給一般快速鍵的 **wm \_** 快速鍵訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**WM \_ GETHOTKEY**](wm-gethotkey.md)
</dt> <dt>

[**WM \_ SETHOTKEY**](wm-sethotkey.md)
</dt> <dt>

**概念**
</dt> <dt>

[鍵盤輸入](keyboard-input.md)
</dt> </dl>

 

