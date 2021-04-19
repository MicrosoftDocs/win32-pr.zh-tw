---
description: Session 物件的 FeatureCost 屬性會傳回指定功能所需的磁碟空間總量 (（以512位元組為單位）) 所需的大小，以及 (到功能資料表) 的根目錄的父功能。
ms.assetid: 5df9912a-2722-41c8-991b-256a009e85df
title: FeatureCost 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCost
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 25c93ce0b3b4efa91a827217d221546e8bab5744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977759"
---
# <a name="sessionfeaturecost-property"></a>FeatureCost 屬性

[**Session**](session-object.md)物件的 **FeatureCost** 屬性會傳回指定功能所需的磁碟空間總量 (（以512位元組為單位）) 所需的大小，以及 (到功能資料表) 的根目錄的父功能。 針對每個功能，總成本是由連結至該功能之每個元件的磁片成本所組成。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Session.FeatureCost
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

如果屬性失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




