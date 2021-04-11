---
title: 'RB_GETROWHEIGHT 訊息 (Commctrl .h) '
description: 抓取 Rebar 控制項中指定之資料列的高度。
ms.assetid: 1ff6a32e-b344-4dbc-b4a4-fb13f11a9d8c
keywords:
- RB_GETROWHEIGHT message Windows 控制項
topic_type:
- apiref
api_name:
- RB_GETROWHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce137eef6168d95abfe493a6f22ab66d58460b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843884"
---
# <a name="rb_getrowheight-message"></a>RB \_ GETROWHEIGHT 訊息

抓取 Rebar 控制項中指定之資料列的高度。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

以零為基底的帶索引。 將會取出包含指定之頻外的資料列高度。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回代表資料列高度的 **UINT** 值（以圖元為單位）。

## <a name="remarks"></a>備註

若要取出 Rebar 控制項中的資料列數目，請使用 [**RB \_ GETROWCOUNT**](rb-getrowcount.md) 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





