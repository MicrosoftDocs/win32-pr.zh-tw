---
title: 'STM_SETIMAGE 訊息 (Winuser .h) '
description: 應用程式會傳送 STM \_ SETIMAGE 訊息，以將新的映射與靜態控制項產生關聯。
ms.assetid: d3e7c5d4-f621-40f6-9558-7fb699e8b489
keywords:
- STM_SETIMAGE message Windows 控制項
topic_type:
- apiref
api_name:
- STM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27c4f9c216d2e987727a1e2fa9bc6de12a823d52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934045"
---
# <a name="stm_setimage-message"></a>STM \_ SETIMAGE 訊息

應用程式會傳送 **STM \_ SETIMAGE** 訊息，以將新的映射與靜態控制項產生關聯。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定要與靜態控制項相關聯的影像類型。 這個參數可以是下列其中一個值：



| 值                                                                                                                                                                     | 意義                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**影像 \_ 點陣圖**</dt> </dl>                | 點陣圖。<br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <dt>**影像 \_ 游標**</dt> </dl>                | 游標。<br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <dt>**影像 \_ ENHMETAFILE**</dt> </dl> | 增強的中繼檔。<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**影像 \_ 圖示**</dt> </dl>                      | 圖示。<br/>              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

要與靜態控制項相關聯之影像的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是先前與靜態控制項相關聯之影像的控制碼（如果有的話）。否則，它會是 **Null**。

## <a name="remarks"></a>備註

若要將影像與靜態控制項產生關聯，控制項必須具有適當的樣式。 下表顯示每個影像類型所需的樣式。



| 映像類型         | 靜態控制項樣式 |
|--------------------|----------------------|
| 影像 \_ 點陣圖      | SS \_ 點陣圖           |
| 影像 \_ 游標      | SS \_ 圖示             |
| 影像 \_ ENHMETAFILE | SS \_ ENHMETAFILE      |
| 影像 \_ 圖示        | SS \_ 圖示             |



 

> [!IMPORTANT]
>
> 在 Microsoft Win32 控制項的第6版中，使用 **.Stm \_ SETIMAGE** 訊息傳遞至靜態控制項的點陣圖，是由後續的 **STM \_ SETIMAGE** 訊息所傳回的相同點陣圖。 用戶端負責刪除傳送至靜態控制項的任何點陣圖。
>
> 在 Windows XP 中，如果在 **.Stm \_ SETIMAGE** 訊息中傳遞的點陣圖包含非零 Alpha 的圖元，則靜態控制項會取得點陣圖的複本。 下一個 **STM \_ SETIMAGE** 訊息會傳回這個複製的點陣圖。 用戶端程式代碼可能會獨立追蹤傳遞給靜態控制項的點陣圖，但如果它沒有檢查並釋出從 **STM \_ SETIMAGE** 訊息傳回的點陣圖，則會遺漏點陣圖。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**STM \_ GETIMAGE**](stm-getimage.md)
</dt> </dl>

 

 





