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
ms.openlocfilehash: 617d1695b8b472952f22737ba3f677d9320f9b4214afc3dea5a9cc5010e2b1a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629288"
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
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




