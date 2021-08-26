---
title: 'LVM_DELETECOLUMN 訊息 (Commctrl .h) '
description: 從清單視圖控制項移除資料行。 您可以明確地傳送此訊息，或使用 ListView \_ DeleteColumn 宏來傳送。
ms.assetid: 1748a70b-9a13-4753-ac23-55b5652164c2
keywords:
- LVM_DELETECOLUMN 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_DELETECOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 039ab92028d23a75518237bc6e9723f051f2f6f2de8732e40f2086d027a61873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920318"
---
# <a name="lvm_deletecolumn-message"></a>LVM \_ DELETECOLUMN 訊息

從清單視圖控制項移除資料行。 您可以明確地傳送此訊息，或使用 [**ListView \_ DeleteColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要刪除之資料行的索引。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

只有 ComCtl32.dll 6 版和更新版本才支援刪除清單視圖控制項中的資料行零。 第5版也支援刪除資料行零，但只有在您使用 [**CCM \_ SETVERSION**](ccm-setversion.md) 將版本設定為5或更新版本之後。 在第5版之前的版本中，如果您必須刪除資料行零，請插入零長度的虛擬資料行零，並刪除一或多個資料行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





