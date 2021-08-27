---
description: ProductVersion 屬性的值是字串格式的產品版本。
ms.assetid: 551fca7e-a827-482d-bc56-ff2fe5a17025
title: ProductVersion 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e09d2fb436dffba5ae2fa98144d39e5824d09796472297db116a2a4543d55168
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074638"
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
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[修補和升級](patching-and-upgrades.md)
</dt> <dt>

[small update](small-updates.md)
</dt> </dl>

 

 




