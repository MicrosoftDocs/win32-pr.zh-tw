---
description: 已取代。 PenInputPanel 已由文字輸入面板取代 (提示) 。在 PenInputPanel 物件于配置之間變更時發生。
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: 'PenInputPanel. PanelChanged 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6ff0f415e12131221a8dad1c0775a347ef96cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320124"
---
# <a name="peninputpanelpanelchanged-event"></a>PenInputPanel. PanelChanged 事件

已取代。 [**PenInputPanel**](peninputpanel-class.md)已由 [文字輸入面板取代 (提示)](text-input-panel-reference.md)。

在 [**PenInputPanel**](peninputpanel-class.md) 物件于配置之間變更時發生。

## <a name="syntax"></a>語法


```C++
HRESULT PanelChanged(
  [in] PanelType NewPanelType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NewPanelType* \[在\]
</dt> <dd>

在 **PanelChanged** 事件引發之後，用於 [**PenInputPanel**](peninputpanel-class.md)物件內輸入的新面板型別。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此事件成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

建立 [**PenInputPanel**](peninputpanel-class.md) 物件時， [**手寫**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) 是預設的 **PanelType**。 如果您在 [畫筆輸入面板] 第一次變成作用中之前設定 [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) 屬性來變更面板，則會發生 **PanelChanged** 事件。

當使用者線上條和手寫書寫板之間變更時，不會引發 **PanelChanged** 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PenInputPanel**](peninputpanel-class.md)
</dt> </dl>

 

 
