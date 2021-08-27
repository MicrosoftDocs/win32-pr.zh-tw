---
title: 'EM_GETFIRSTVISIBLELINE 訊息 (Winuser .h) '
description: 取得多行編輯控制項中最上層可見行的索引（以零為基底）。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 022838d2-7948-4c5a-92ca-655822c4f672
keywords:
- EM_GETFIRSTVISIBLELINE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETFIRSTVISIBLELINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11eb93c1c7dcce7f502945df4e063b22c29514bc79fe7310875e9de055e1d745
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049208"
---
# <a name="em_getfirstvisibleline-message"></a>EM \_ GETFIRSTVISIBLELINE 訊息

取得多行編輯控制項中最上層可見行的索引（以零為基底）。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是多行編輯控制項中最上層可見行的索引（以零為基底）。

**編輯控制項：** 針對單行編輯控制項，傳回值是第一個可見字元的以零為基底的索引。

**Rich edit 控制項：** 針對單行 rich edit 控制項，傳回值為零。

## <a name="remarks"></a>備註

編輯控制項中的行數和線條長度，取決於控制項的寬度和目前的 Wordwrap 設定。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



 

 





