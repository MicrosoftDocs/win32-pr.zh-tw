---
title: 'CBEM_DELETEITEM 訊息 (Commctrl .h) '
description: 從 ComboBoxEx 控制項中移除專案。
ms.assetid: 688cf388-54ba-4b45-88d7-628da49d8615
keywords:
- CBEM_DELETEITEM message Windows 控制項
topic_type:
- apiref
api_name:
- CBEM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa3034f79dffabcd7d7aa780582646e17d30b62f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106996587"
---
# <a name="cbem_deleteitem-message"></a>CBEM \_ DELETEITEM 訊息

從 ComboBoxEx 控制項中移除專案。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要移除之專案的以零為基底的索引。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 INT 值，表示控制項中剩餘的專案數目。 如果 *iIndex* 無效，訊息會傳回 CB \_ ERR。

## <a name="remarks"></a>備註

這則訊息會對應至下拉式方塊控制項訊息 [**CB \_ DELETESTRING**](cb-deletestring.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





