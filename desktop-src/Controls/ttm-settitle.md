---
title: 'TTM_SETTITLE 訊息 (Commctrl .h) '
description: 將標準圖示和標題字串新增至工具提示。
ms.assetid: e745a592-eef7-4e0d-8939-a48b52c4ab9f
keywords:
- TTM_SETTITLE message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_SETTITLE
- TTM_SETTITLEA
- TTM_SETTITLEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7972a9d40347995e9d641e7fc8706f9ad4c58bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844259"
---
# <a name="ttm_settitle-message"></a>TTM \_ SETTITLE 訊息

將標準圖示和標題字串新增至工具提示。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

將 *wParam* 設定為下列其中一個值，以指定要顯示的圖示。 從 Windows XP SP2 和更新版本，此參數也可以包含 **HICON** 值。 任何大於 TTI 誤差的值 \_ 都假設為 **HICON**。



| 值                                                                                                                                                                      | 意義                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="TTI_NONE"></span><span id="tti_none"></span><dl> <dt>**TTI \_ 無**</dt> </dl>                             | 無圖示。<br/>         |
| <span id="TTI_INFO"></span><span id="tti_info"></span><dl> <dt>**TTI \_ 資訊**</dt> </dl>                             | 資訊圖示。<br/>       |
| <span id="TTI_WARNING"></span><span id="tti_warning"></span><dl> <dt>**TTI \_ 警告**</dt> </dl>                    | 警告圖示<br/>     |
| <span id="TTI_ERROR"></span><span id="tti_error"></span><dl> <dt>**TTI \_ 錯誤**</dt> </dl>                          | 錯誤圖示<br/>       |
| <span id="TTI_INFO_LARGE"></span><span id="tti_info_large"></span><dl> <dt>**TTI \_ 資訊 \_ 很大**</dt> </dl>          | 大型錯誤圖示<br/> |
| <span id="TTI_WARNING_LARGE"></span><span id="tti_warning_large"></span><dl> <dt>**TTI \_ 警告 \_ 很大**</dt> </dl> | 大型錯誤圖示<br/> |
| <span id="TTI_ERROR_LARGE"></span><span id="tti_error_large"></span><dl> <dt>**TTI \_ 錯誤 \_ 大**</dt> </dl>       | 大型錯誤圖示<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

標題字串的指標。 您必須將值指派給 *lParam*。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

工具提示的標題會出現在文字上方的不同字型中。 沒有標題就夠了。工具提示也必須有文字，否則就不會顯示。

當 *wParam* 包含 **HICON** 時，[工具提示] 視窗會建立圖示的複本。

呼叫 **TTM \_ SETTITLE** 時， *lParam* 所指向的字串不得超過 100 **TCHARs** 的長度，包括終止的 **Null**。

## <a name="examples"></a>範例

下列範例顯示如何將標題和系統圖示新增至工具提示。


```C++
// hwndTip is the handle of the tooltip window.
HICON hIcon = LoadIcon(NULL, IDI_INFORMATION);
SendMessage(hwndTip, TTM_SETTITLE, (WPARAM)hIcon, L"Title text");
DestroyIcon(hIcon);
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TTM \_SETTITLEW** (Unicode) 和 **TTM \_ SETTITLEA** (ANSI) <br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[關於工具提示控制項](tooltip-controls.md)
</dt> </dl>

 

 





