---
description: 當使用者在 [檔案管理員目錄] 視窗或 [搜尋結果] 視窗中選取檔案名時，傳送至擴充 DLL。
title: 'FMEVENT_SELCHANGE 訊息 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_SELCHANGE
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0773aa74-adf2-4e90-aead-2a9a981be3cb
ms.openlocfilehash: 4b05bca54f75bd48b5e710e31c31e5f0f56a2597
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510787"
---
# <a name="fmevent_selchange-message"></a>FMEVENT \_ SELCHANGE 訊息

當使用者在 [檔案管理員目錄] 視窗或 [搜尋結果] 視窗中選取檔案名時，傳送至擴充 DLL。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果延伸模組 DLL 處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

目錄視窗的樹狀結構部分中的變更不會產生此訊息。

因為使用者可以多次變更選取專案，所以擴充 DLL 必須在處理此訊息之後立即傳回，以避免讓使用者的選取程式變慢。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wfext。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




