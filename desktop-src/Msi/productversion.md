---
description: ProductVersion 屬性的值是字串格式的產品版本。
ms.assetid: 551fca7e-a827-482d-bc56-ff2fe5a17025
title: ProductVersion 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01f82fcbd28c4a4132e4c3f76adfd68e33c43b36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996405"
---
# <a name="productversion-property"></a>ProductVersion 屬性

**ProductVersion** 屬性的值是字串格式的產品版本。 此為必要屬性。

字串的格式如下所示：

<dl> major.minor.build  
</dl>

第一個欄位是主要版本，最大值為255。 第二個欄位是次要版本，最大值為255。 第三個欄位稱為組建版本或更新版本，且最大值為65535。

## <a name="remarks"></a>備註

**ProductVersion** 的三個欄位中至少有一個必須變更，才能使用 [升級資料表](upgrade-table.md)進行升級。 只要變更封裝程式碼，但不變更 **ProductVersion** 和 [**ProductCode**](productcode.md) 的更新，就稱為 [小型更新](small-updates.md)。 提供的三個版本欄位主要是為了方便起見。 例如，如果您想要變更 **ProductVersion**，但不想變更主要或次要版本，您可以變更組建版本。

請注意，Windows Installer 只會使用產品版本的前三個欄位。 如果您在產品版本中包含第四個欄位，安裝程式會忽略第四個欄位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[修補和升級](patching-and-upgrades.md)
</dt> <dt>

[small update](small-updates.md)
</dt> </dl>

 

 




