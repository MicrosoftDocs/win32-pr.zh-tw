---
description: 指定由檔案管理員呼叫的應用程式定義回呼函式，以與檔案管理員延伸模組進行通訊。
title: 'FMExtensionProc 回呼函數 (Wfext) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMExtensionProc
- FMExtensionProcW
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 6e02d655-f7d8-460a-97d2-5b369493e941
ms.openlocfilehash: 7cd13fe534f3bb121a4056f67ceff47ddfa71fa5506c2020a243ab340768ce35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032656"
---
# <a name="fmextensionproc-callback-function"></a>FMExtensionProc 回呼函式

指定由檔案管理員呼叫的應用程式定義回呼函式，以與檔案管理員延伸模組進行通訊。

## <a name="syntax"></a>語法


```C++
LONG CALLBACK FMExtensionProc(
   HWND hwnd,
   WORD wMsg,
   LONG lParam
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* 
</dt> <dd>

類型： **HWND**

檔案管理員的視窗控制碼。 延伸模組會使用此控制碼來指定它必須顯示之任何對話方塊或訊息方塊的父視窗，以及將查詢訊息傳送至 [檔案管理員]。

</dd> <dt>

*wMsg* 
</dt> <dd>

類型： **WORD**

下列其中一個檔案管理員訊息。

<dt>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>**1至99**


</dt> <dd>

使用者從擴充功能提供的功能表中選取專案。 值是選取之功能表項目的識別碼。

</dd> <dt>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT \_ HELPMENUITEM**


</dt> <dd>

在選取擴充功能功能表或工具列命令專案時，使用者按下 F1。 指出延伸模組應針對命令專案適當地呼叫 **WinHelp** 。

</dd> <dt>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT \_ HELPSTRING**


</dt> <dd>

使用者選取了延伸功能表或工具列命令專案。 指出延伸模組應提供說明字串。

</dd> <dt>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT \_ INITMENU**


</dt> <dd>

使用者選取了擴充功能的功能表。 擴充功能應該將功能表中的專案初始化。

</dd> <dt>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**FMEVENT \_ 載入**


</dt> <dd>

檔案管理員正在載入延伸模組 DLL，並提示 DLL 提供 DLL 提供之功能表的相關資訊。

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT \_ SELCHANGE**


</dt> <dd>

[ **檔案管理員** 目錄] 視窗或 [ **搜尋結果** ] 視窗中的選取專案已變更。

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT \_ TOOLBARLOAD**


</dt> <dd>

[檔案管理員] 正在建立工具列，並提示副檔名 DLL 提供 DLL 加入工具列之任何按鈕的相關資訊。

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**FMEVENT \_ UNLOAD**


</dt> <dd>

檔案管理員正在卸載擴充 DLL。

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**FMEVENT \_ 使用者重新整理 \_**


</dt> <dd>

使用者已從 **[** **視窗]** 功能表中選取 [重新整理] 命令。 必要時，擴充功能應該更新功能表中的專案。

</dd> </dl> </dd> <dt>

*lParam* 
</dt> <dd>

類型： **LONG**

訊息特定的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **LONG**

傳回相依于 *wMsg* 參數訊息的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wfext。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **FMExtensionProcW** (Unicode) <br/>                                          |



 

 




