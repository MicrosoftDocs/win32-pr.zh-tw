---
title: 'EM_GETFILELINECOUNT 訊息 (CommCtrl .h) '
description: 取得多行編輯控制項中的行數，與螢幕上的線條顯示方式無關。
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- EM_GETFILELINECOUNT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETFILELINECOUNT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: bf48b3abeb10b98bf0c22a7dd2ef93c73a2a59c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104832"
---
# <a name="em_getfilelinecount-message-commctrlh"></a>EM_GETFILELINECOUNT 訊息 (CommCtrl .h) 

取得多行編輯控制項中的行數，與螢幕上的線條顯示方式無關。

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

傳回值是一個整數，它會指定多行編輯控制項中的文字行總數，而不會與螢幕上顯示的行數分開。 如果控制項沒有任何文字，則傳回值為1。 傳回值永遠不會小於1。

## <a name="remarks"></a>備註

**EM \_ GETFILELINECOUNT** 訊息會抓取文字行總數，與螢幕上顯示的行數無關，而不只是目前可見的行數。

自動換行並不會變更此訊息傳回的行數，因為此訊息與螢幕上的行顯示方式無關。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限 1809 desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2019 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>CommCtrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ GETFILELINE**](em-getfileline.md)
</dt> <dt>

[**EM \_ FILELINELENGTH**](em-filelinelength.md)
</dt> <dt>

[**編輯 \_ GetFileLineCount**](/windows/win32/api/commctrl/nf-commctrl-edit_getfilelinecount)
</dt> </dl>

 

 





