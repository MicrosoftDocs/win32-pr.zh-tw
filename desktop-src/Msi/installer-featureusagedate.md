---
description: FeatureUsageDate 屬性是唯讀屬性，會傳回上次使用指定功能的日期。
ms.assetid: 444e54b2-94e7-44ea-8d7b-eeac984e3715
title: FeatureUsageDate 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageDate
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b393f9a24b9d1ebeb82de86d26483f703d7854c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986172"
---
# <a name="installerfeatureusagedate-property"></a>FeatureUsageDate 屬性

**FeatureUsageDate** 屬性是唯讀屬性，會傳回上次使用指定功能的日期。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.FeatureUsageDate
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

使用 [**UseFeature**](installer-usefeature.md)、 [**ProvideComponent**](installer-providecomponent.md) 或 [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) 方法或其在指定功能上的 API 對等專案，會設定這個屬性。

日期會是 MS-DOS 日期格式，如下表所示。



| Bits | 目錄                                            |
|------|-----------------------------------------------------|
| 0-4  | 每月的日 (1-31)                              |
| 5-8  | 月 (1 = 一月、2 = 二月，依此類推)         |
| 9-15 | 從1980算起的年位移 (新增1980以取得實際年份)  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




