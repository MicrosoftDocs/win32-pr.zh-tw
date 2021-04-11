---
title: 'LVM_SETVIEW 訊息 (Commctrl .h) '
description: 設定清單視圖控制項的視圖。
ms.assetid: e6d3f16d-52ea-4863-a6c9-9a085d5f794a
keywords:
- LVM_SETVIEW message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a159710b3086bcba5298a5a88f9cab15f76e0d89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105462"
---
# <a name="lvm_setview-message"></a>LVM \_ SETVIEW 訊息

設定清單視圖控制項的視圖。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>指定視圖的 **DWORD** 。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回1，否則傳回-1。 例如，如果視圖無效，則會傳回-1。

## <a name="remarks"></a>備註

以下是 views 的值。

-   LV \_ 視圖 \_ 詳細資料
-   LV \_ 視圖 \_ 圖示
-   LV \_ 視圖 \_ 清單
-   LV \_ 視圖 \_ SMALLICON
-   LV \_ 視圖 \_ 磚

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comctl32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





