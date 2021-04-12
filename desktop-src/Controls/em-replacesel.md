---
title: 'EM_REPLACESEL 訊息 (Winuser .h) '
description: 以指定的文字取代編輯控制項中選取的文字或 rich edit 控制項。
ms.assetid: 525e6f5a-f52f-4bab-bc76-caa484729897
keywords:
- EM_REPLACESEL message Windows 控制項
topic_type:
- apiref
api_name:
- EM_REPLACESEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9745b870a310626a6cbbbddbef118a63c64479
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106271"
---
# <a name="em_replacesel-message"></a>EM \_ REPLACESEL 訊息

以指定的文字取代編輯控制項中選取的文字或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定取代作業是否可以復原。 若為 **TRUE**，則作業可以復原。 如果為 **FALSE** ，則作業無法復原。

</dd> <dt>

*lParam* 
</dt> <dd>

以 null 結束的字串指標，其中包含取代文字。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

使用 **EM \_ REPLACESEL** 訊息來取代編輯控制項中的部分文字。 若要取代所有文字，請使用 [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) 訊息。

如果沒有選取專案，則會在插入號插入取代文字。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

在 rich edit 控制項中，取代文字會採用插入號的字元格式，或是選取範圍中第一個字元的選項。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

