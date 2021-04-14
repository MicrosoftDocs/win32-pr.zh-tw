---
title: 'ACM_OPEN 訊息 (Commctrl .h) '
description: 開啟 AVI 剪輯，並在動畫控制項中顯示其第一個畫面格。 您可以明確地傳送此訊息，或使用動畫 \_ 開啟或 \_ OpenEx 宏的動畫。 我們建議使用此訊息的 Unicode 版本 \_ OPENW。
ms.assetid: 87f476ce-bb27-4b5f-bfdf-dff84bd7e4f4
keywords:
- ACM_OPEN message Windows 控制項
topic_type:
- apiref
api_name:
- ACM_OPEN
- ACM_OPENA
- ACM_OPENW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0588c0e321efe5cace63baf4016dbaa97f735252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384130"
---
# <a name="acm_open-message"></a>\_未結的開啟訊息

開啟 AVI 剪輯，並在動畫控制項中顯示其第一個畫面格。 您可以明確地傳送此訊息，或使用 [**動畫 \_ 開啟**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) 或 [**\_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) 宏的動畫。 我們建議使用此訊息的 Unicode 版本 \_ OPENW。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[4.71 版](common-control-versions.md) 和更新版本。 應從中載入資源之模組的實例控制碼。 將此值設定為 **Null** ，讓控制項使用用來建立視窗的 HINSTANCE 值。 請注意，如果視窗是由 DLL 所建立，則 *wParam* 的預設值為 DLL 的 HINSTANCE 值，而不是呼叫 dll 的應用程式。

</dd> <dt>

*lParam* 
</dt> <dd>

緩衝區的指標，其中包含 AVI 檔案的路徑或 AVI 資源的名稱。 或者，此參數可以包含 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 中的 AVI 資源識別碼，以及 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))中的零。 若要建立這個值，請使用 [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) 宏。 控制項會從傳遞給 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 函式的實例控制碼所指定的模組、建立動畫的宏或 [**建立 \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) 控制項的對話方塊建立函數載入 AVI 資源。 在 [4.71 版](common-control-versions.md) 和更新版本中，資源是從 *wParam* 所指定的模組載入。 AVI 資源必須有 "AVI" 類型。 如果這個參數為 **Null**，系統會關閉先前針對指定動畫控制項開啟的 AVI 檔案（如果有的話）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="remarks"></a>備註

*LpszName* 所指定的 AVI 檔案或資源不得包含音訊。

我們建議使用此訊息的 Unicode 版本 \_ OPENW。

您只能開啟無訊息的 AVI 剪輯。 \_如果 *lParam* 指定包含音效的 AVI 剪輯，則開啟的 [開啟] 和 [建立 [**動畫動畫 \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) ] 會失敗。

您可以使用 [**「 \_ 左右動畫**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) 」來關閉先前針對指定動畫控制項開啟的 AVI 檔案或 avi 資源。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | 進行中 **\_OPENW** (Unicode) 和 **\_ OPENA** (ANSI) <br/>                         |



 

