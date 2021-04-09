---
title: 'TDM_UPDATE_ICON 訊息 (Commctrl .h) '
description: 重新整理工作對話方塊的圖示。
ms.assetid: 1094d9ca-90b4-4ba6-a14b-0d4e96243a34
keywords:
- TDM_UPDATE_ICON message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_UPDATE_ICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2da73ebb3bf0355f50bc08a08f0b35de97576b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935092"
---
# <a name="tdm_update_icon-message"></a>TDM \_ 更新 \_ 圖示訊息

重新整理工作對話方塊的圖示。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

表示要更新的圖示元素。 此參數必須是下列其中一個值：



| 值                                                                                                                                                                   | 意義                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="TDIE_ICON_MAIN"></span><span id="tdie_icon_main"></span><dl> <dt>**TDIE \_ 圖示 \_ MAIN**</dt> </dl>       | 主要圖示。<br/>   |
| <span id="TDIE_ICON_FOOTER"></span><span id="tdie_icon_footer"></span><dl> <dt>**TDIE \_ 圖示 \_ 頁尾**</dt> </dl> | 頁尾圖示。<br/> |



 

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

字串的指標， (PCWSTR) 或 (HICON) 顯示的圖示控制碼。 如果 *lParam* 為 **Null**，則不論 *wParam* 的值為何，都不會顯示任何圖示。

如果 *wParam* 的值為 TDIE \_ 圖示 \_ main，且 .tdf \_ USE \_ HICON \_ main 旗標是在用來建立工作對話方塊的 [**dwFlags**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)結構的 **TASKDIALOGCONFIG** 成員上設定，則 *lParam* 必須包含圖示的控制碼 (HICON) 才能顯示。

如果 *wParam* 的值是 TDIE \_ 圖示頁尾 \_ ，且 .tdf \_ USE HICON 頁尾旗標 \_ \_ 是在用來建立工作對話方塊的 [**dwFlags**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)結構的 **TASKDIALOGCONFIG** 成員上設定，則 *lParam* 必須包含圖示的控制碼 (HICON) 才能顯示。

如果 .TDF \_ use \_ HICON \_ MAIN 或 .tdf \_ use HICON 頁尾 \_ \_ 旗標 **未** 在 **dwFlags** 成員上設定，則 *lParam* 必須指向以 Null 終止的 Unicode 字串 (PCWSTR) ，其中包含透過 [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) 宏傳遞的有效資源識別碼。 圖示會根據 *wParam* 的值顯示：如果值為 TDIE \_ 圖示 \_ MAIN，圖示就會顯示在標頭中; 如果值為 TDIE \_ 圖示頁尾 \_ ，圖示就會顯示在頁尾中。 資源必須是來自應用程式的資源模組 (在 [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)) 結構的 **hInstance** 成員中指定，或如果 **hInstance** 為 **Null**，則會從系統的資源模組 (imageres.dll) 。 若要識別系統資源，請使用透過 **MAKEINTRESOURCE** 宏傳遞的有效系統識別碼，或 commctrl 中的下列其中一個預先定義值：



| 值                                                                                                                                                                            | 意義                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="TD_ERROR_ICON"></span><span id="td_error_icon"></span><dl> <dt>**TD \_ 錯誤 \_ 圖示**</dt> </dl>                   | 停止符號圖示。<br/>                        |
| <span id="TD_WARNING_ICON"></span><span id="td_warning_icon"></span><dl> <dt>**TD \_ 警告 \_ 圖示**</dt> </dl>             | 驚嘆號圖示。<br/>               |
| <span id="TD_INFORMATION_ICON"></span><span id="td_information_icon"></span><dl> <dt>**TD \_ 資訊 \_ 圖示**</dt> </dl> | 圓圈圖示中的小寫字母 "i"。<br/> |
| <span id="TD_SHIELD_ICON"></span><span id="td_shield_icon"></span><dl> <dt>**TD \_ 防護 \_ 圖示**</dt> </dl>                | 安全性保護盾圖示。<br/>                  |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="remarks"></a>備註

具有圖示的工作對話方塊配置可能會失敗，而且不會反映在傳回值中。 \_[確定] 的傳回值只會反映工作對話方塊收到的訊息，並嘗試進行處理。 如果工作對話方塊的配置失敗，對話方塊將會關閉，並且會在註冊的回呼函式傳回 **HRESULT** 程式碼。 如需回呼函數語法的詳細資訊，請參閱 [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback)。

如果在沒有頁尾的情況下建立工作對話方塊 (也就是，用來建立工作對話方塊的 [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) 結構的適當頁尾成員是 **Null**) 而且會傳送此訊息，不會將頁尾動態新增至工作對話方塊。 當您在沒有標頭的情況下建立工作對話方塊時，傳送此訊息來更新標頭圖示也是如此。 若要在執行時間加入頁首或頁尾，請使用 [**TDM \_ 導覽 \_ 頁面**](tdm-navigate-page.md) 功能。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

