---
description: 只有在每部電腦或目前使用者安裝產品時，才會設定已安裝的屬性。
ms.assetid: 139a6324-58fb-485e-8b3e-c5cf2881d5d1
title: 已安裝屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae5126107fff51f3790fb3ab9a9209490b9627a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979451"
---
# <a name="installed-property"></a>已安裝屬性

只有在每部電腦或目前使用者安裝產品時，才會設定 **已安裝** 的屬性。 如果已針對不同的使用者安裝產品，則不會設定此屬性。

[ **已安裝** ] 屬性可用於條件運算式中，以判斷是否已針對每部電腦或目前使用者安裝產品。 例如，您可以在順序資料表的條件式資料行中使用屬性，或區別第一個安裝和維護安裝。

若要判斷是否已針對不同的使用者安裝產品，請檢查 [**ProductState**](productstate.md) 屬性。

[**ProductVersion**](productversion.md)屬性的值是字串格式的產品版本。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




