---
title: 'TVM_MAPHTREEITEMTOACCID 訊息 (Commctrl .h) '
description: 將 HTREEITEM 對應至存取範圍識別碼。
ms.assetid: 87ef0785-88c1-49f4-8a05-872577e16fe4
keywords:
- TVM_MAPHTREEITEMTOACCID message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_MAPHTREEITEMTOACCID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6267c2040583917283fc444db74ddacbdabd69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103721"
---
# <a name="tvm_maphtreeitemtoaccid-message"></a>TVM \_ MAPHTREEITEMTOACCID 訊息

將 **HTREEITEM** 對應至存取範圍識別碼。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>對應至存取範圍識別碼的 **HTREEITEM** 。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回存取範圍識別碼。

## <a name="remarks"></a>備註

當您將專案加入至樹狀檢視控制項時，會傳回可唯一識別該專案的 **HTREEITEM** 控制碼。

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

[**TreeView \_ MapHTREEITEMtoAccID**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_maphtreeitemtoaccid)
</dt> </dl>

 

 





