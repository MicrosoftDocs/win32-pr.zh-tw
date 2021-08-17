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
ms.openlocfilehash: 136bc160ea81367f8f55ad81cfc06f5e2e272cafae9d7b8f444a65d34e85d52b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328368"
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
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IFeatureInfo 定義為 000C109F-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Windows安裝程式腳本範例](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




