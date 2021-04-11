---
title: 'LVM_INSERTGROUPSORTED 訊息 (Commctrl .h) '
description: 將群組插入排序的群組清單中。
ms.assetid: 8ad1660b-8b64-4f02-ac1b-b7edeeea38ab
keywords:
- LVM_INSERTGROUPSORTED message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_INSERTGROUPSORTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 485941f803fd5af565d8b40524a9e15968e387cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844083"
---
# <a name="lvm_insertgroupsorted-message"></a>LVM \_ INSERTGROUPSORTED 訊息

將群組插入排序的群組清單中。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd><a href="/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted">LVINSERTGROUPSORTED</a>結構的指標，其中包含要插入的群組。</dd> <dt>

*lParam* 
</dt> <dd>必須是 **Null**。</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="remarks"></a>備註

清單的順序是根據群組的識別碼。 順序是由應用程式定義的順序函式 [**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)所定義，該函式是由 *WParam* 參數在 [**LVINSERTGROUPSORTED**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted)結構中傳遞。

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> <dt>

[**LVINSERTGROUPSORTED**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted)
</dt> </dl>

 

