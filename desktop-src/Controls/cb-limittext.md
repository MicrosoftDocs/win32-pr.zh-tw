---
title: 'CB_LIMITTEXT 訊息 (Winuser .h) '
description: 限制使用者可在下拉式方塊的編輯控制項中輸入的文字長度。
ms.assetid: 95b7d07a-594b-4096-afbb-4dab77bdc41d
keywords:
- CB_LIMITTEXT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- CB_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e94cdb1bedfb1c0aa3efb401649524782183ced7728304951596c9383efaa0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089078"
---
# <a name="cb_limittext-message"></a>CB \_ LIMITTEXT 訊息

限制使用者可在下拉式方塊的編輯控制項中輸入的文字長度。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

使用者可以輸入的最大 **TCHARs** 數目，不包括終止的 null 字元。 如果此參數為零，則文字長度限制為0x7FFFFFFE 字元。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值一律為 **TRUE**。

## <a name="remarks"></a>備註

如果下拉式方塊沒有 [**CBS \_ AUTOHSCROLL**](combo-box-styles.md) 樣式，將文字限制設定為大於編輯控制項的大小不會有任何作用。

**CB \_ LIMITTEXT** 郵件只會限制使用者可以輸入的文字。 當傳送訊息時，它不會影響任何已在編輯控制項中的文字，也不會影響選取清單方塊中的字串時，複製到編輯控制項的文字長度。

使用者可以在編輯控制項中輸入的文字預設限制為 30000 **TCHARs**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



 

 





