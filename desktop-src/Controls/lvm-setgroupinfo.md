---
title: 'LVM_SETGROUPINFO 訊息 (Commctrl .h) '
description: 設定群組資訊。
ms.assetid: f79bd235-e2de-4055-be3e-76eb2744e1ee
keywords:
- LVM_SETGROUPINFO 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553a81c3cfe962ae6daf5ae4c988964028554bc662cec08df40c16fd8b4eb43f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077268"
---
# <a name="lvm_setgroupinfo-message"></a>LVM \_ SETGROUPINFO 訊息

設定群組資訊。 明確地傳送此訊息，或使用 [**ListView \_ SetGroupInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>指定要設定其資訊之群組的識別碼。</dd> <dt>

*lParam* \[in、out\]
</dt> <dd>[**LVGROUP**](windows/win32/api/commctrl/ns-commctrl-lvgroup)結構的指標，其中包含要設定的資訊。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回群組的識別碼，否則為-1。

## <a name="remarks"></a>備註

若要變更現有群組的群組識別碼，請將 <b>LVGF_GROUPID</b> 新增至 <b>LVGROUP</b> ，並將 <b>LVGROUP IGROUPID</b> 設定為新的識別碼。 如果 <b>LVGROUP. iGroupId</b> 包含現有群組的識別碼，則呼叫會失敗。

若要更新現有群組的其他屬性 (例如，更新群組的頁首或頁尾文字對齊方式， <b>uAlign</b>) <b>LVGROUP。 mask</b> 不得包含 <b>LVGF_GROUPID</b>，否則更新將會失敗。

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





