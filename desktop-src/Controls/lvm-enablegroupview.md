---
title: 'LVM_ENABLEGROUPVIEW 訊息 (Commctrl .h) '
description: 啟用或停用清單視圖控制項中的專案是否顯示為群組。
ms.assetid: 783a5e23-d1cb-4523-a6d2-b2cf93fa7f62
keywords:
- LVM_ENABLEGROUPVIEW message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_ENABLEGROUPVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d546e1236fa4f0800c0353810beb5b427ba4fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024600"
---
# <a name="lvm_enablegroupview-message"></a>LVM \_ ENABLEGROUPVIEW 訊息

啟用或停用清單視圖控制項中的專案是否顯示為群組。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>**布林** 值，指出是否要啟用清單視圖控制項來群組顯示的專案。 使用 **TRUE** 可啟用群組， **FALSE** 則會停用。 </dd> <dt>

*lParam* 
</dt> <dd>必須是 **Null**。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個值。



| 傳回碼                                                                       | Description                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>  | 將清單視圖專案顯示為群組的功能已啟用或停用。<br/> |
| <dl> <dt>**1**</dt> </dl>  | 已成功變更控制項的狀態。<br/>                                |
| <dl> <dt>**-1**</dt> </dl> | 作業失敗。<br/>                                                             |



 

## <a name="remarks"></a>備註

**LVM \_** [**Lvs) \_ OWNERDATA**](list-view-window-styles.md)樣式下不支援 ENABLEGROUPVIEW。

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





