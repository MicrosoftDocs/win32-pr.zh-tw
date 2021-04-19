---
description: MSINEWINSTANCE 屬性工作表示安裝具有實例轉換之產品的新實例。
ms.assetid: 35d41fa9-79d3-4baa-b177-5a32239b5051
title: MSINEWINSTANCE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8b51ec02d7b30c42e6e400b6a6177d7ef47d88c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987856"
---
# <a name="msinewinstance-property"></a>MSINEWINSTANCE 屬性

**MSINEWINSTANCE** 屬性工作表示安裝具有實例轉換之產品的新實例。 這個屬性會透過產品程式碼來支援多個實例–變更轉換。 這個屬性的值為1。 在命令列上存在此屬性時，必須同時存在 [**轉換**](transforms.md) 屬性。 **轉換** 中所列的第一個轉換必須是實例轉換。 如需詳細資訊，請參閱 [安裝產品和修補程式的多個實例](installing-multiple-instances-of-products-and-patches.md)

在 Windows Server 2003 或 Windows XP 中執行系統的安裝程式可以使用此屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




