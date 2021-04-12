---
title: 'UDM_GETPOS32 訊息 (Commctrl .h) '
description: 傳回上下按鈕控制項的32位位置。
ms.assetid: 90feffbd-a472-446f-8a67-5da408cde002
keywords:
- UDM_GETPOS32 message Windows 控制項
topic_type:
- apiref
api_name:
- UDM_GETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15f316b6833c67cd01d4e01910399a8730691f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464648"
---
# <a name="udm_getpos32-message"></a>UDM \_ GETPOS32 訊息

傳回上下按鈕控制項的32位位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

如果已成功抓取值，則為 **布林** 值的指標，如果發生錯誤，則會設為非零。 如果此參數設定為 **Null**，則不會報告錯誤。

如果在跨進程的情況下使用 **UDM \_ GETPOS32** ，此參數必須是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回具有32位精確度的上下按鈕控制項的位置。 應用程式必須檢查 *lParam* 值，以判斷傳回值是否有效。

## <a name="remarks"></a>備註

當它處理此訊息時，上下按鈕控制項會根據好友視窗的標題來更新其目前位置。 如果沒有好友視窗，或標題指定無效或超出範圍的值，則會傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**UDM \_ GETPOS**](udm-getpos.md)
</dt> <dt>

[**UDM \_ SETPOS**](udm-setpos.md)
</dt> <dt>

[**UDM \_ SETPOS32**](udm-setpos32.md)
</dt> </dl>

 

 





