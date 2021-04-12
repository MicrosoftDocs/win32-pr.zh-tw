---
title: 'TDM_SET_ELEMENT_TEXT 訊息 (Commctrl .h) '
description: 更新工作對話方塊中的文字專案。
ms.assetid: e3f15805-5d48-4549-9959-69ec01345e57
keywords:
- TDM_SET_ELEMENT_TEXT message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_SET_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2229dc269f14c9a3b0765675dcc97dc9776b72c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025433"
---
# <a name="tdm_set_element_text-message"></a>TDM \_ 設定 \_ 元素 \_ 文字訊息

更新工作對話方塊中的文字專案。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

表示要更新的元素。  (圖的詳細資訊，請參閱 [關於工作對話方塊](task-dialogs-overview.md)。 ) 此參數必須是下列值之一。



| 值                                                                                                                                                                                           | 意義                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**TDE \_ 內容**</dt> </dl>                                         | 內容。<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**TDE \_ 展開的 \_ 資訊**</dt> </dl> | 展開的資訊。<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**TDE \_ 頁尾**</dt> </dl>                                            | 頁尾文字。<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**TDE \_ 主要 \_ 指示**</dt> </dl>             | Main 指令。<br/>     |



 

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

要使用的新文字。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="remarks"></a>備註

工作對話方塊的大小或配置可能會變更，以容納新的文字。

## <a name="examples"></a>範例

下列範例程式碼示範如何設定 *hwnd* 所代表之工作對話方塊中的頁尾文字。


```C++
SendMessage(hwnd, TDM_SET_ELEMENT_TEXT, (WPARAM)TDE_FOOTER, (LPARAM)L"New footer text.");
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TDM \_ UPDATE \_ 元素 \_ 文字**](tdm-update-element-text.md)
</dt> </dl>

 

 





