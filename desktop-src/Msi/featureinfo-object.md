---
description: FeatureInfo 物件包含有關目標功能的資訊，並使用 FeatureInfo 方法從會話物件建立。
ms.assetid: c9c96799-22c7-4e74-947b-3b8d31ebc1f1
title: FeatureInfo 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1db1bab5b1e55f027bb01eb9eff22484a4e39170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975731"
---
# <a name="featureinfo-object"></a>FeatureInfo 物件

**FeatureInfo** 物件包含有關目標功能的資訊，並使用 [**FeatureInfo**](session-featureinfo.md)方法從 [**會話**](session-object.md)物件建立。

## <a name="members"></a>成員

**FeatureInfo** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**FeatureInfo** 物件具有這些屬性。



| 屬性                                                  | 存取類型           | Description                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**屬性**](featureinfo-attributes.md)<br/>   | 讀取/寫入<br/> | 在功能資料表的 [屬性] 資料行中，傳回功能的值。<br/> |
| [**描述**](featureinfo-description.md)<br/> |                       | 傳回功能的描述。<br/>                                          |
| [**標題**](featureinfo-title.md)<br/>             | 唯讀<br/>  | 傳回功能的標題。<br/>                                                |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IFeatureInfo 定義為 000C109F-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Windows Installer 腳本範例](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




