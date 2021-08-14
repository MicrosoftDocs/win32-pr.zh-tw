---
title: HelpModeOn 屬性
description: HelpModeOn 屬性
ms.assetid: 4a9b5fd3-12e2-489b-8ce0-9b66b01f517a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 489de1893e96bf2d4cc38ef9e788a726db8b9fd4dfbdc9ae3cd1b60f9bc02f91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962738"
---
# <a name="helpmodeon-property"></a>HelpModeOn 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定是否為字元的即時線上說明模式。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*agent. ***字元 ( "**_CharacterID_*_" ) 。HelpModeOn_ *  \[  =  *布林值*\]



| 部分      | 描述                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | 布林運算式，指定是否開啟即時線上說明模式。 **True** 說明模式為開啟。 <br/> **False** (預設) 說明模式為關閉。<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

當您將這個屬性設定為 **True** 時，滑鼠指標會在移至字元上方或移至字元的快顯功能表時，變更為內容相關的說明影像。 當使用者按一下或拖曳字元，或按一下字元快顯功能表中的專案時，伺服器會觸發 [**HelpComplete**](helpcomplete-event.md) 事件並離開說明模式。

在 [說明] 模式中，除非您將 [**AutoPopupMenu**](autopopupmenu-property.md)屬性設定為 **True**，否則伺服器不會傳送 [**Click**](click-event.md)、 [**DragStart**](dragstart-event.md)、 [**DragComplete**](dragcomplete-event.md)和 [**命令**](command-event.md)事件。 在這種情況下，伺服器會傳送 **Click** 事件 (不會離開說明模式) ，而只有滑鼠右鍵可讓您顯示快顯功能表。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

## <a name="see-also"></a>另請參閱

[**HelpComplete 事件**](helpcomplete-event.md)


 

 





