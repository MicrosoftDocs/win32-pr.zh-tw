---
description: MSINEWINSTANCE 屬性工作表示安裝具有實例轉換之產品的新實例。
ms.assetid: 35d41fa9-79d3-4baa-b177-5a32239b5051
title: MSINEWINSTANCE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b26831f1171813d9df9e2c4124a4d6c24ea7efbf707fc5c15eefc9d6a8b1046
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082848"
---
# <a name="msinewinstance-property"></a>MSINEWINSTANCE 屬性

**MSINEWINSTANCE** 屬性工作表示安裝具有實例轉換之產品的新實例。 這個屬性會透過產品程式碼來支援多個實例–變更轉換。 這個屬性的值為1。 在命令列上存在此屬性時，必須同時存在 [**轉換**](transforms.md) 屬性。 **轉換** 中所列的第一個轉換必須是實例轉換。 如需詳細資訊，請參閱 [安裝產品和修補程式的多個實例](installing-multiple-instances-of-products-and-patches.md)

在 Windows Server 2003 或 Windows XP 中執行系統的安裝程式可以使用此屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




