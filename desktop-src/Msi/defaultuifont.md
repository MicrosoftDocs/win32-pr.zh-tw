---
description: DefaultUIFont 屬性會設定用於控制項的預設字型樣式。 若要指定預設值，請將 DefaultUIFont 設定為屬性工作表中的樣式表單中的其中一個預先定義樣式。
ms.assetid: 594183ce-ef13-47f6-a4ae-37ba09c06cbd
title: DefaultUIFont 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3791219dcef84253280fec3c797f2035afd239f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979625"
---
# <a name="defaultuifont-property"></a>DefaultUIFont 屬性

**DefaultUIFont** 屬性會設定用於控制項的預設字型樣式。 若要指定預設值，請將 **DefaultUIFont** 設定為 [屬性工作表](property-table.md)中的樣式 [表單](textstyle-table.md)中的其中一個預先定義樣式。

## <a name="remarks"></a>備註

您應在 [屬性工作表](property-table.md)中，將每個安裝套件的 **DefaultUIFont** 屬性設定為 [[樣式](textstyle-table.md)表單] 中所列的其中一個預先定義樣式。 如果未指定這個屬性，安裝程式會使用系統字型。 當套件的字碼頁與使用者的預設 UI 字碼頁不同時，這可能會導致安裝程式不正確地顯示文字字串。

您可以如 [新增控制項和文字](adding-controls-and-text.md)中所述，設定控制項的文字與字型樣式。 如果 [控制資料表](control-table.md) 或 [BBControl 表](bbcontrol-table.md) 的 Text 資料行中所列的字元字串未指定字型樣式，控制項就會使用 **DefaultUIFont** 屬性的值做為字型樣式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




