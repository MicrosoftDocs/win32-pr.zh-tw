---
title: 'LVM_GETINSERTMARK 訊息 (Commctrl .h) '
description: 抓取插入點的位置。
ms.assetid: ad00df4c-4b4b-48f1-8821-7849a216df2e
keywords:
- LVM_GETINSERTMARK 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e64281ccc9d4638353ddbb6062ce5cf1c0a678e009639dcc43cd0d4cf52741
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002668"
---
# <a name="lvm_getinsertmark-message"></a>LVM \_ GETINSERTMARK 訊息

抓取插入點的位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd><a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a>結構的指標，此結構會接收插入點的位置。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。 如果 [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark)結構之 **cbSize** 成員中的大小不等於結構的實際大小，就會傳回 **FALSE** 。

## <a name="remarks"></a>備註

只有在清單視圖控制項處於圖示視圖、小型圖示視圖或磚視圖，而且不在群組視圖模式中時，才會出現插入點。

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





