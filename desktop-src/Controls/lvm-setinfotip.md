---
title: 'LVM_SETINFOTIP 訊息 (Commctrl .h) '
description: 針對 LVN GETINFOTIP 通知，設定延遲回應中的工具提示文字 \_ 。
ms.assetid: 3dbf6a9a-52ec-4619-9c70-041e75942e20
keywords:
- LVM_SETINFOTIP 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef739535e399550911adfbe86d7376d3efeb77cd797ba807b24ee682d1f3fe3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919898"
---
# <a name="lvm_setinfotip-message"></a>LVM \_ SETINFOTIP 訊息

針對 [LVN \_ GETINFOTIP](lvn-getinfotip.md) 通知，設定延遲回應中的工具提示文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd><a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">LVSETINFOTIP</a>結構的指標，其中包含要設定的資訊。</dd> </dl>

## <a name="return-value"></a>傳回值

如果工具提示文字設定成功，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

**LVM \_ SETINFOTIP** 訊息會透過執行下列步驟，讓應用程式在背景中計算提示：

1.  為了回應 [LVN \_ GETINFOTIP](lvn-getinfotip.md)通知，請將 [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa)結構的 **pszText** 成員設為空字串，並傳回0。
2.  在背景中，計算提示。
3.  計算資訊提示之後，傳送 **LVM \_ SETINFOTIP** 訊息，將 [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip)結構的 **pszText** 成員設定為資訊提示，並將 **iItem** 和 **iSubItem** 成員設定為資訊提示所套用的專案和子專案。

只有當 [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip)結構所描述的專案和子專案仍處於需要資訊提示的狀態時，才會顯示傳遞至 **LVM \_ SETINFOTIP** 訊息的文字

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





