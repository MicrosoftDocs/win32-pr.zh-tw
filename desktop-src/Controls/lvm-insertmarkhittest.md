---
title: 'LVM_INSERTMARKHITTEST 訊息 (Commctrl .h) '
description: 抓取最接近指定點的插入點。
ms.assetid: 901bb770-a36d-4d9f-a53b-d497b4df39e5
keywords:
- LVM_INSERTMARKHITTEST 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 250585fea10846e10238132c5150f5ace9f8e00c474e763023c36c8566fbc752
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919978"
---
# <a name="lvm_insertmarkhittest-message"></a>LVM \_ INSERTMARKHITTEST 訊息

抓取最接近指定點的插入點。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>指向包含點擊測試座標之 **點** 結構的指標。</dd> <dt>

*lParam* 
</dt> <dd><a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a>結構的指標，指定最接近 *wParam* 參數所定義之座標的插入點。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。 如果 [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark)結構之 **cbSize** 成員中的大小不等於結構的實際大小，或當插入點不適用於目前的視圖時，則會傳回 **FALSE** 。

## <a name="remarks"></a>備註

只有當清單視圖控制項處於圖示視圖、小型圖示視圖或磚視圖，而且不在群組視圖模式中時，才會出現插入點。

如果不適用此視圖的插入點， [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) 結構會在 **iItem** 成員中包含-1。

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





