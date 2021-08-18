---
title: 'EM_GETCARETINDEX 訊息 (CommCtrl .h) '
description: 取得編輯控制項中插入號的位置之以零為基底的索引。
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- EM_GETCARETINDEX 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETCARETINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4080acdc7ee338b76f80b97c81a952188fc74774254476771f9ff47e87f3fdff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019836"
---
# <a name="em_getcaretindex-message"></a>EM \_ GETCARETINDEX 訊息

取得編輯控制項中插入號的位置之以零為基底的索引。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是以零為基底的索引值，即插入號的位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限 1809 desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2019 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>CommCtrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ SETCARETINDEX**](em-setcaretindex.md)
</dt> </dl>

 

 





