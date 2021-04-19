---
description: 在成功驗證之後，ProductID 屬性會設定為完整 ProductID。UI 會顯示這個值，並由 RegisterProduct 動作使用。成功驗證之後，此屬性是由 ValidateProductID 動作或 ValidateProductID ControlEvent 所設定。請注意，SDK 隨附的特定範例使用者介面 Uisample.msi 需要 ProductID 的值。 如果您使用此 UI，但不想使用 ProductID 來驗證產品識別碼，請在屬性工作表中將 [ProductID] 屬性設定為 &\# 0034; none&\# 0034;。
ms.assetid: 6af23f2d-b22a-470d-b979-da32776e0007
title: ProductID 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf616e2bc34ce70deb5f6b63dba7287002d4fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998656"
---
# <a name="productid-property"></a>ProductID 屬性

在成功驗證之後， **productid** 屬性會設定為完整 **productid** 。

UI 會顯示這個值，並由 [RegisterProduct 動作](registerproduct-action.md)使用。

成功驗證之後，此屬性是由 [ValidateProductID 動作](validateproductid-action.md) 或 [ValidateProductID ControlEvent](validateproductid-controlevent.md)設定。

請注意，SDK 隨附的特定範例使用者介面 Uisample.msi 需要 **ProductID** 的值。 如果您使用此 UI，但不想使用 **ProductID** 來驗證產品識別碼，請在 [屬性工作表](property-table.md)中將 [ **productid** ] 屬性設定為 [無]。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




