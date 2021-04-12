---
title: 'EM_FILELINELENGTH 訊息 (CommCtrl .h) '
description: 抓取編輯控制項中某一行的長度（以字元為單位），與螢幕上的線條顯示方式無關。
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- EM_FILELINELENGTH message Windows 控制項
topic_type:
- apiref
api_name:
- EM_FILELINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa50f4d9b49253a558095be78e0e781d7d4c7f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508712"
---
# <a name="em_filelinelength-message"></a>EM \_ FILELINELENGTH 訊息

抓取編輯控制項中某一行的長度（以字元為單位），與螢幕上的線條顯示方式無關。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要取出其長度的行字元字元索引。 如果此參數大於控制項中的字元數，則傳回值為零。

此參數可以是-1。 在此情況下，訊息會傳回包含所選字元的行上未選取的字元數。 例如，如果選取範圍是從下一行結尾的第四個字元到第四個字元，則傳回值會是第一行的 10 (三個字元，而在下一個) 則是七個字元。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

若為多行編輯控制項，傳回值是 *wParam* 參數所指定之線條的長度（以 **TCHAR** s），與螢幕上的線條顯示方式無關。 它不會在行尾包含回車或換行字元。

針對單行編輯控制項，傳回值是編輯控制項中文字的長度（以 **TCHAR** s）。

如果 *wParam* 大於控制項中的字元數，則傳回值為零。

## <a name="remarks"></a>備註

使用 [**EM \_ FILELINEINDEX**](em-lineindex.md) 訊息來抓取多行編輯控制項內指定行號的字元索引，與螢幕上的線條顯示方式無關。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限 1809 desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2019 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>CommCtrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ FILELINEINDEX**](em-filelineindex.md)
</dt> </dl>

 

 





