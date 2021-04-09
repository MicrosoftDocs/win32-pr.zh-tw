---
title: 'EM_GETCARETINDEX 訊息 (CommCtrl .h) '
description: 取得編輯控制項中插入號的位置之以零為基底的索引。
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- EM_GETCARETINDEX message Windows 控制項
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
ms.openlocfilehash: 6653e2ae0e2126941e3d8977a593300b86051800
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934490"
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
| 最低支援的伺服器<br/> | 僅限 Windows Server 2019 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>CommCtrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ SETCARETINDEX**](em-setcaretindex.md)
</dt> </dl>

 

 





