---
title: 'TVM_MAPACCIDTOHTREEITEM 訊息 (Commctrl .h) '
description: 地圖 HTREEITEM 的存取範圍識別碼。
ms.assetid: f4feb7cb-2138-4930-b8ee-b9e2d4b19001
keywords:
- TVM_MAPACCIDTOHTREEITEM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_MAPACCIDTOHTREEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6481d8db806156d10536ac0ec7c66fdeb4693a1133365767b4c3dc37ad8420f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045798"
---
# <a name="tvm_mapaccidtohtreeitem-message"></a>TVM \_ MAPACCIDTOHTREEITEM 訊息

地圖 **HTREEITEM** 的存取範圍識別碼。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>包含要對應至 **HTREEITEM** 之存取範圍識別碼的 **UINT** 。 </dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回指定的協助工具識別碼所對應的 **HTREEITEM** 。

## <a name="remarks"></a>備註

當您將專案加入至樹狀檢視控制項時， **HTREEITEM** 會傳回可唯一識別該專案的。

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TreeView \_ MapAccIDToHTREEITEM**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
</dt> </dl>

 

 





