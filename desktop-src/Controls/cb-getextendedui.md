---
title: 'CB_GETEXTENDEDUI 訊息 (Winuser .h) '
description: 決定下拉式方塊是否有預設使用者介面或擴充的使用者介面。
ms.assetid: 4f5580e0-68b1-4584-bf79-561fb8222fe0
keywords:
- CB_GETEXTENDEDUI message Windows 控制項
topic_type:
- apiref
api_name:
- CB_GETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d90550bf341fc8586174c7ec57eb77fad08c59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465268"
---
# <a name="cb_getextendedui-message"></a>CB \_ GETEXTENDEDUI 訊息

決定下拉式方塊是否有預設使用者介面或擴充的使用者介面。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果下拉式方塊有擴充的使用者介面，則傳回值為 **TRUE**;否則為 **FALSE**。

## <a name="remarks"></a>備註

依預設，F4 鍵會開啟或關閉清單，而向下箭號會變更目前的選取範圍。 在具有擴充使用者介面的下拉式方塊中，會停用 F4 鍵，然後按向下鍵以開啟下拉式清單。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CB \_ SETEXTENDEDUI**](cb-setextendedui.md)
</dt> <dt>

**概念**
</dt> <dt>

[下拉式列示方塊功能](combo-box-features.md)
</dt> </dl>

 

 





