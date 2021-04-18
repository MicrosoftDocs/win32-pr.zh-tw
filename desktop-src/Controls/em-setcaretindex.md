---
title: 'EM_SETCARETINDEX 訊息 (CommCtrl .h) '
description: 設定在編輯控制項中插入號的位置之以零為基底的索引值。
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- EM_SETCARETINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETCARETINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: ea0c49ebad91532e82dc7e96facb62f38b2abfa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466549"
---
# <a name="em_setcaretindex-message"></a>EM \_ SETCARETINDEX 訊息

設定在編輯控制項中插入號的位置之以零為基底的索引值。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

插入號之位置的新索引值（以零為基底）。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

如果索引超出編輯控制項中的文字範圍，則會調整索引以容納在文字範圍內。

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

[**EM \_ GETCARETINDEX**](em-getcaretindex.md)
</dt> </dl>

 

 





