---
title: 'LVM_GETINSERTMARKRECT 訊息 (Commctrl .h) '
description: 抓取插入點界限的矩形。
ms.assetid: 7b10229c-73ab-426c-8a8a-71258a33e248
keywords:
- LVM_GETINSERTMARKRECT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5832ce185a579432b341482847400e96d60869a64d3ff0a2cd599e2eecf6b20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062598"
---
# <a name="lvm_getinsertmarkrect-message"></a>LVM \_ GETINSERTMARKRECT 訊息

抓取插入點界限的矩形。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>未使用;必須為零。</dd> <dt>

*lParam* 
</dt> <dd><a href="/previous-versions//dd162897(v=vs.85)">**矩形結構的**</a>指標，其中包含包圍插入點之矩形的座標。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個值。



| 傳回碼                                                                      | 描述                          |
|----------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**0**</dt> </dl> | 找不到插入點。<br/> |
| <dl> <dt>**1**</dt> </dl> | 找到插入點。<br/>    |



 

## <a name="remarks"></a>備註

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

