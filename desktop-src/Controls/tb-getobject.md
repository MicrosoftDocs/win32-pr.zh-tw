---
title: 'TB_GETOBJECT 訊息 (Commctrl .h) '
description: 抓取工具列控制項的 IDropTarget。
ms.assetid: b26394ea-6f0f-4084-956d-f9166cc54b76
keywords:
- TB_GETOBJECT message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce923feaec893e6f4304eb0b993de33dc1fe2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105054"
---
# <a name="tb_getobject-message"></a>TB \_ GETOBJECT 訊息

抓取工具列控制項的 [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) 。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

所要求之介面的識別碼。 此值必須指向 **IID \_ IDropTarget**。

</dd> <dt>

*lParam* 
</dt> <dd>

接收介面指標的位址。 如果發生錯誤，則會在此位址中放置 **Null** 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值，指出作業成功或失敗。

## <a name="remarks"></a>備註

工具列的 [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) 會在將物件拖曳至其上方或卸載時，供工具列使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

