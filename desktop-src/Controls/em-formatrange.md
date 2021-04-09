---
title: 'EM_FORMATRANGE 訊息 (Richedit .h) '
description: 針對特定裝置格式化 rich edit 控制項中的文字範圍。
ms.assetid: 6d1e562b-d741-4d4a-a395-554083cb0dbb
keywords:
- EM_FORMATRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_FORMATRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8f235fb054643623510ea23e73001aaeb070be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843712"
---
# <a name="em_formatrange-message"></a>EM \_ FORMATRANGE 訊息

針對特定裝置格式化 rich edit 控制項中的文字範圍。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定是否呈現文字。 如果這個參數不是零，則會呈現文字。 否則，只會測量文字。

</dd> <dt>

*lParam* 
</dt> <dd>

[**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange)結構，其中包含輸出裝置的相關資訊，或 **Null** 表示控制項快取的可用資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息會傳回符合區域的最後一個字元的索引，加上1。

## <a name="remarks"></a>備註

此訊息通常是用來格式化輸出裝置（如印表機）之 rich edit 控制項的內容。

使用此訊息來格式化某範圍的文字之後，請務必再次傳送 **EM \_ FORMATRANGE** ，但是將 *lParam* 設為 **Null**，以釋放快取的資訊，否則會發生記憶體流失。 此外，在為一部裝置使用此訊息之後，您必須先釋放快取的資訊，再針對不同的裝置再次使用它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ DISPLAYBAND**](em-displayband.md)
</dt> <dt>

**概念**
</dt> <dt>

[列印 Rich Edit 控制項](printing-rich-edit-controls.md)
</dt> </dl>

 

 





