---
description: 設定此屬性就像設定 TransformsAtSource 原則原則一樣，不同之處在于範圍不同。
ms.assetid: b78c3757-d969-4684-84b9-b2acfd9f5c82
title: TRANSFORMSATSOURCE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b0acf2e64976d66f04fbd16ec67a5bb38b7fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996487"
---
# <a name="transformsatsource-property"></a>TRANSFORMSATSOURCE 屬性

設定此屬性就像設定 [TransformsAtSource 原則](transformsatsource-policy.md) 原則一樣，不同之處在于範圍不同。 設定 TransformsAtSource 原則會套用至指定使用者所安裝的所有套件。 無論使用者是哪一種，設定 **TRANSFORMSATSOURCE** 屬性都會套用至套件。

## <a name="remarks"></a>備註

Windows Installer 會以 [**TRANSFORMSSECURE**](transformssecure.md)屬性的形式來解讀 **TRANSFORMSATSOURCE** 屬性。 如果在 [**轉換**](transforms.md) 屬性中傳遞 @ 旗標，Windows Installer 會將清單中的轉換視為 [安全來源轉換](secure-at-source-transforms.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




