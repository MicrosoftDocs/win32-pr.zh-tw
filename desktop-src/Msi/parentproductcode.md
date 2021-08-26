---
description: 在並行安裝期間，安裝程式會將並行安裝會話中的 ParentProductCode 屬性設定為與父安裝會話中的 [ProductCode] 屬性相同的值。
ms.assetid: 7bf2b9b1-9efd-4d47-9fa3-253421f1ba4f
title: ParentProductCode 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a56e7a120455723eb95f2bd7f5ea08c59894d3a1951aeb042afb30e3b0e2fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042448"
---
# <a name="parentproductcode-property"></a>ParentProductCode 屬性

在並行安裝期間，安裝程式會將並行安裝會話中的 **ParentProductCode** 屬性設定為與父安裝會話中的 [ [**ProductCode**](productcode.md) ] 屬性相同的值。 父安裝會執行並行安裝動作來執行並行安裝。 安裝套件可以藉由檢查這個屬性的值，判斷是否由並行安裝動作安裝。

> [!Note]  
> 不建議將並行安裝用於安裝應用程式，以供公開發行。 如需並行安裝的詳細資訊，請參閱 [並行安裝](concurrent-installations.md)。

 

> [!Note]  
> 如果 [RemoveExistingProducts](removeexistingproducts-action.md) 動作正在執行並行安裝，就不會設定這個屬性。

 

## <a name="remarks"></a>備註

若要防止封裝安裝為並行安裝，請將下列其中一個條件陳述式加入至 [LaunchCondition](launchcondition-table.md) 資料表。 這可防止另一個安裝執行的並行安裝動作來安裝套件。 這不會防止 [RemoveExistingProducts](removeexistingproducts-action.md) 動作安裝套件。

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[**ParentOriginalDatabase**](parentoriginaldatabase.md)
</dt> </dl>

 

 




