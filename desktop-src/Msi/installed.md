---
description: 只有在每部電腦或目前使用者安裝產品時，才會設定已安裝的屬性。
ms.assetid: 139a6324-58fb-485e-8b3e-c5cf2881d5d1
title: 已安裝屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5925f68595f6b0975e64281be0ba7326fa831d08f0298f9b84375df97e5196c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633521"
---
# <a name="installed-property"></a>已安裝屬性

只有在每部電腦或目前使用者安裝產品時，才會設定 **已安裝** 的屬性。 如果已針對不同的使用者安裝產品，則不會設定此屬性。

[ **已安裝** ] 屬性可用於條件運算式中，以判斷是否已針對每部電腦或目前使用者安裝產品。 例如，您可以在順序資料表的條件式資料行中使用屬性，或區別第一個安裝和維護安裝。

若要判斷是否已針對不同的使用者安裝產品，請檢查 [**ProductState**](productstate.md) 屬性。

[**ProductVersion**](productversion.md)屬性的值是字串格式的產品版本。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




