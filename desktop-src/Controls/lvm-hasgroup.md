---
title: 'LVM_HASGROUP 訊息 (Commctrl .h) '
description: 判斷清單視圖控制項是否有指定的群組。
ms.assetid: 0b8a9208-5221-4f66-8b26-7de55afe485f
keywords:
- LVM_HASGROUP message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_HASGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb05fed8466188aa0025d2128ce64ad7f1512c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466497"
---
# <a name="lvm_hasgroup-message"></a>LVM \_ HASGROUP 訊息

判斷清單視圖控制項是否有指定的群組。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>群組的識別碼。</dd> <dt>

*lParam* 
</dt> <dd>必須是 **Null**。</dd> </dl>

## <a name="return-value"></a>傳回值

如果清單視圖控制項具有指定的群組，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





