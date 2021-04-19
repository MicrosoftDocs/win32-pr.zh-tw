---
description: CoNtext 屬性會傳回此修補程式的內容。
ms.assetid: 09c92b0b-44f3-4355-8171-03da8ba32757
title: Patch。 CoNtext 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a6495b199046a361910741545a7178050621ccd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982511"
---
# <a name="patchcontext-property"></a>Patch。 CoNtext 屬性

**CoNtext** 屬性會傳回此修補程式的內容。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Patch.Context
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

這個屬性會傳回下列其中一個值。



| Context                        | 值 | 意義                        |
|--------------------------------|-------|--------------------------------|
| MSIINSTALLCONTEXT \_ USERMANAGED | 1     | 在受控內容下修補。   |
| MSIINSTALLCONTEXT \_ 使用者        | 2     | 在未受管理的內容下修補。 |
| MSIINSTALLCONTEXT \_ 機器     | 4     | 電腦內容下的修補程式。   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch 定義為000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Patch 物件**](patch-object.md)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




