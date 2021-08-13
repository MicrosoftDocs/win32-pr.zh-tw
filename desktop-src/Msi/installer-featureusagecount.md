---
description: FeatureUsageCount 屬性是唯讀屬性，會傳回功能已使用的次數。
ms.assetid: 70171e22-d73a-4718-a360-df9d1722761b
title: FeatureUsageCount 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageCount
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8f0f8444909d07655949cd35d060eb455e5a153fc2b897e757c2fdde2d1d731d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631197"
---
# <a name="installerfeatureusagecount-property"></a>FeatureUsageCount 屬性

**FeatureUsageCount** 屬性是唯讀屬性，會傳回功能已使用的次數。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.FeatureUsageCount
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

使用 [**UseFeature**](installer-usefeature.md)、 [**ProvideComponent**](installer-providecomponent.md) 或 [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) 方法或其在指定功能上的 API 對等專案，會遞增這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




