---
title: 'TTM_GETTITLE 訊息 (Commctrl .h) '
description: 取得工具提示控制項標題的相關資訊。
ms.assetid: d8992dd1-1610-44e8-8c0f-8ae1ac4b5898
keywords:
- TTM_GETTITLE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TTM_GETTITLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 242e20f3360caac03874524df38267fc0b103ec8f1c04d8d30df106fc9c65ac4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797438"
---
# <a name="ttm_gettitle-message"></a>TTM \_ GETTITLE 訊息

取得工具提示控制項標題的相關資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**TTGETTITLE**](/windows/desktop/api/Commctrl/ns-commctrl-ttgettitle)結構的指標，其中包含工具提示標題的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="remarks"></a>備註

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





