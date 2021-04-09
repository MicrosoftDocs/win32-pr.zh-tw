---
title: 'EM_LINELENGTH 訊息 (Winuser .h) '
description: 抓取編輯控制項中的行長度（以字元為單位）。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- EM_LINELENGTH message Windows 控制項
topic_type:
- apiref
api_name:
- EM_LINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3cbf59cbe31886e55c34bce9f7c2421e431012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844044"
---
# <a name="em_linelength-message"></a>EM \_ LINELENGTH 訊息

抓取編輯控制項中的行長度（以字元為單位）。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。

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

若為多行編輯控制項，傳回值是 *wParam* 參數所指定之行的長度（以 **TCHAR** s）。 若為 ANSI 文字，此為位元組數;若為 Unicode 文字，此為字元數。 它不會在行尾包含換行字元。

針對單行編輯控制項，傳回值是編輯控制項中文字的長度（以 **TCHAR** s）。

如果 *wParam* 大於控制項中的字元數，則傳回值為零。

## <a name="remarks"></a>備註

使用 [**EM \_ LINEINDEX**](em-lineindex.md) 訊息，在多行編輯控制項內取出指定行號的字元索引。

**Rich Edit：** Microsoft Rich Edit 1.0 和更新版本支援。 如需有關豐富編輯版本與各種系統版本之相容性的詳細資訊，請參閱 [關於 Rich Edit 控制項](about-rich-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ LINEINDEX**](em-lineindex.md)
</dt> </dl>

 

 





