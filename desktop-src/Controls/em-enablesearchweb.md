---
title: 'EM_ENABLESEARCHWEB 訊息 (CommCtrl .h) '
description: 啟用或停用 [搜尋 web] 功能和內容功能表項目。
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- EM_ENABLESEARCHWEB message Windows 控制項
topic_type:
- apiref
api_name:
- EM_ENABLESEARCHWEB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdb2638476027f0a7fe2bb1a66a3a00a330e28c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934634"
---
# <a name="em_enablesearchweb-message"></a>EM \_ ENABLESEARCHWEB 訊息

啟用或停用 [搜尋 web] 功能和內容功能表項目。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**TRUE** 值表示已啟用「搜尋 web」功能，而值為 **FALSE** 表示已停用。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

如果您使用此訊息停用 [搜尋網路]， [**EM \_ SEARCHWEB**](em-searchweb.md) 訊息不會有任何作用。

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

[**EM \_ SEARCHWEB**](em-searchweb.md)
</dt> </dl>

 

 





