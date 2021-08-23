---
description: Session 物件的 FeatureInfo 方法會傳回 FeatureInfo 物件，其中包含指定功能的描述性資訊。
ms.assetid: f5391fd4-984e-44cc-8b6c-fd97834e0674
title: FeatureInfo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b4d6e44a16305d4a46525cfed631068ff0137c642b09b8dc6a9eca169a104548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625196"
---
# <a name="sessionfeatureinfo-method"></a>FeatureInfo 方法

[**Session**](session-object.md)物件的 **FeatureInfo** 方法會傳回 **FeatureInfo** 物件，其中包含指定功能的描述性資訊。

## <a name="syntax"></a>語法


```JScript
Session.FeatureInfo(
  Feature
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*功能* 
</dt> <dd>

識別感興趣的功能。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
</dt> </dl>

 

 




