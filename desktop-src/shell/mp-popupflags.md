---
description: 表示顯示快顯功能表時可用的選項。
title: 'MP_POPUPFLAGS 常數 (Shobjidl.h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cc1d9ff0-a03b-4bd3-b481-9b78d20eb771
api_name:
- MPPF_SETFOCUS
- MPPF_INITIALSELECT
- MPPF_NOANIMATE
- MPPF_KEYBOARD
- MPPF_REPOSITION
- MPPF_FORCEZORDER
- MPPF_FINALSELECT
- MPPF_ALIGN_LEFT
- MPPF_ALIGN_RIGHT
- MPPF_TOP
- MPPF_LEFT
- MPPF_RIGHT
- MPPF_BOTTOM
- MPPF_POS_MASK
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d49f848df7749a732e9f0b849d44a9be56a5c3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113968"
---
# <a name="mp_popupflags-constants"></a>MP \_ POPUPFLAGS 常數

表示顯示快顯功能表時可用的選項。



| 常數/值                                                                                                                                                                                                                               | Description                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPPF_SETFOCUS"></span><span id="mppf_setfocus"></span><dl> <dt>**MPPF \_SETFOCUS**</dt> <dt>0x00000001</dt> </dl>                | 提供快顯功能表焦點。<br/>                                                                                                                                                                                                                               |
| <span id="MPPF_INITIALSELECT"></span><span id="mppf_initialselect"></span><dl> <dt>**MPPF \_INITIALSELECT**</dt> <dt>0x00000002</dt> </dl> | 選取快顯功能表中的第一個專案。<br/>                                                                                                                                                                                                                     |
| <span id="MPPF_NOANIMATE"></span><span id="mppf_noanimate"></span><dl> <dt>**MPPF \_NOANIMATE**</dt> <dt>0x00000004</dt> </dl>             | 在顯示功能表時，請勿使用預設的系統動畫，例如淡入。<br/>                                                                                                                                                                     |
| <span id="MPPF_KEYBOARD"></span><span id="mppf_keyboard"></span><dl> <dt>**MPPF \_鍵盤**</dt> <dt>0x00000010</dt> </dl>                | 依鍵盤快速鍵啟動功能表。<br/>                                                                                                                                                                                                                     |
| <span id="MPPF_REPOSITION"></span><span id="mppf_reposition"></span><dl> <dt>**MPPF \_重新置放**</dt> <dt>0x00000020</dt> </dl>          | 根據功能表的變更，將列顯示在不同的位置。<br/>                                                                                                                                                                                        |
| <span id="MPPF_FORCEZORDER"></span><span id="mppf_forcezorder"></span><dl> <dt>**MPPF \_FORCEZORDER**</dt> <dt>0x00000040</dt> </dl>       | 保留的。 請勿使用。<br/>                                                                                                                                                                                                                                         |
| <span id="MPPF_FINALSELECT"></span><span id="mppf_finalselect"></span><dl> <dt>**MPPF \_FINALSELECT**</dt> <dt>0x00000080</dt> </dl>       | 選取功能表中的最後一個專案。<br/>                                                                                                                                                                                                                             |
| <span id="MPPF_ALIGN_LEFT"></span><span id="mppf_align_left"></span><dl> <dt>**MPPF \_靠 \_ 左對齊**</dt> <dt>0x02000000</dt> </dl>         | **Windows Vista 或更新版本**：在 [**ITrackShellMenu：:P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)或 [**IMenuPopup：:P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)的 *prcExclude* 參數中指定的區域左邊對齊快顯功能表。 這是預設的對齊方式。<br/> |
| <span id="MPPF_ALIGN_RIGHT"></span><span id="mppf_align_right"></span><dl> <dt>**MPPF \_靠 \_ 右對齊**</dt> <dt>0x04000000</dt> </dl>      | **Windows Vista 或更新版本**：在 [**ITrackShellMenu：:P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)或 [**IMenuPopup：:P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)的 *prcExclude* 參數中指定的區域右邊對齊快顯功能表。<br/>                               |
| <span id="MPPF_TOP"></span><span id="mppf_top"></span><dl> <dt>**MPPF \_TOP**</dt> <dt>0x20000000</dt> </dl>                               | 將快顯功能表放在 [**ITrackShellMenu：:P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)或 [**IMenuPopup：:P**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)之 *ppt* 參數所指定的初始點上方。<br/>                                                                |
| <span id="MPPF_LEFT"></span><span id="mppf_left"></span><dl> <dt>**MPPF \_左方**</dt> <dt>0x40000000</dt> </dl>                            | 將快顯功能表放在初始點的左邊。<br/>                                                                                                                                                                                                    |
| <span id="MPPF_RIGHT"></span><span id="mppf_right"></span><dl> <dt>**MPPF \_RIGHT**</dt> <dt>0x60000000</dt> </dl>                         | 將快顯功能表放在初始點的右邊。<br/>                                                                                                                                                                                                   |
| <span id="MPPF_BOTTOM"></span><span id="mppf_bottom"></span><dl> <dt>**MPPF \_底部**</dt> <dt> (int) 0x80000000</dt> </dl>                 | 將快顯功能表放在初始點下方。<br/>                                                                                                                                                                                                             |
| <span id="MPPF_POS_MASK"></span><span id="mppf_pos_mask"></span><dl> <dt>**MPPF \_POS \_ 遮罩**</dt> <dt> (int) 0xE0000000</dt> </dl>          | 功能表位置遮罩。<br/>                                                                                                                                                                                                                                       |



## <a name="remarks"></a>備註

這些常數定義于從 Windows XP Service Pack 1 (SP1) 和 Windows Server 2003 開始的 Shobjidl.h .h 檔案

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP1） \[ 桌面應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Shobjidl.h。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.h .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMenuPopup：:P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)
</dt> <dt>

[**ITrackShellMenu：:P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)
</dt> </dl>

 

 




