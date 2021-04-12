---
title: 'EM_GETHANDLE 訊息 (Winuser .h) '
description: 取得目前配置給多行編輯控制項文字的記憶體控制碼。
ms.assetid: 74271812-9715-4a46-96b3-0788134f8143
keywords:
- EM_GETHANDLE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88a466394b48d2d726621e50a7e2c5df2f747f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508923"
---
# <a name="em_gethandle-message"></a>EM \_ GETHANDLE 訊息

取得目前配置給多行編輯控制項文字的記憶體控制碼。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是識別保存編輯控制項內容之緩衝區的記憶體控制碼。 如果發生錯誤（例如將訊息傳送到單行編輯控制項），則傳回值為零。

## <a name="remarks"></a>備註

如果函式成功，應用程式可以藉由將傳回值轉換成 [**HLOCAL**](/windows/desktop/WinProg/windows-data-types) 並將它傳遞給 [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock)，來存取編輯控制項的內容。 **LocalLock** 會根據 ANSI 或 Unicode 函數是否建立控制項，傳回以 null 結束的 **CHAR** s 或 **WCHAR** s 陣列的緩衝區指標。 例如，如果使用 [**CreateWindowExA**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ，則緩衝區是 **CHAR** s 的陣列，但如果使用 **CreateWindowExW** ，則緩衝區是 **WCHAR** 的陣列。 應用程式可能不會變更緩衝區的內容。 若要解除鎖定緩衝區，應用程式會先呼叫 [**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) ，然後再允許編輯控制項接收新訊息。

> [!Note]  
> 針對 Comctl32.dll 第6版，無論 ANSI 或 Unicode 函數是否建立了編輯控制項，緩衝區一律會包含 **WCHAR** 的陣列。 如需 DLL 版本的詳細資訊，請參閱 [通用控制項版本](common-control-versions.md)。

 

如果您的應用程式無法遵守 **EM \_ GETHANDLE** 所加諸的限制，請使用 [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) 和 [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) 函數將編輯控制項的內容複寫到應用程式提供的緩衝區。

**Rich Edit：** 不支援 **EM \_ GETHANDLE** 訊息。 Rich edit 控制項不會將文字儲存為簡單字元陣列。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ SETHANDLE**](em-sethandle.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock)
</dt> <dt>

[**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock)
</dt> </dl>

 

