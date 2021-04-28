---
title: 'TDM_UPDATE_ELEMENT_TEXT 訊息 (Commctrl .h) '
description: TDM_UPDATE_ELEMENT_TEXT 訊息-更新工作對話方塊中的文字專案。
ms.assetid: 2df446c8-db87-42b5-b5bd-40fadbf9d45b
keywords:
- TDM_UPDATE_ELEMENT_TEXT message Windows 控制項
topic_type:
- apiref
api_name:
- TDM_UPDATE_ELEMENT_TEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c155b426b92645c0b9cdbabe00c44ffa722b89f3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085806"
---
# <a name="tdm_update_element_text-message"></a>TDM \_ UPDATE \_ 元素 \_ 文字訊息

更新工作對話方塊中的文字專案。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

表示要更新的元素。  (如需元素的圖例，請參閱 [關於工作對話方塊](task-dialogs-overview.md)。 ) 此參數必須是下列其中一個值：



| 值                                                                                                                                                                                           | 意義                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="TDE_CONTENT"></span><span id="tde_content"></span><dl> <dt>**TDE \_ 內容**</dt> </dl>                                         | 內容。<br/>              |
| <span id="TDE_EXPANDED_INFORMATION"></span><span id="tde_expanded_information"></span><dl> <dt>**TDE \_ 展開的 \_ 資訊**</dt> </dl> | 展開的資訊。<br/> |
| <span id="TDE_FOOTER"></span><span id="tde_footer"></span><dl> <dt>**TDE \_ 頁尾**</dt> </dl>                                            | 頁尾文字。<br/>          |
| <span id="TDE_MAIN_INSTRUCTION"></span><span id="tde_main_instruction"></span><dl> <dt>**TDE \_ 主要 \_ 指示**</dt> </dl>             | Main 指令。<br/>     |



 

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

包含新文字的 Unicode 字串指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="remarks"></a>備註

若要避免裁剪，新的文字必須不超過現有文字。 將文字設定為較短的字串並不會讓對話方塊調整大小。

如果用來建立工作對話方塊的 [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)結構的 **PszExpandedInformation** 成員為 **Null**，而且您傳送了具有 TDE 擴充資訊的 **TDM \_ UPDATE \_ 元素 \_ 文字** 訊息 \_ ，則 \_ 不會發生任何事。

上述也適用于頁尾和 TDE 頁尾 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TDM \_ 設定 \_ 元素 \_ 文字**](tdm-set-element-text.md)
</dt> </dl>

 

 





