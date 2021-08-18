---
description: Session 物件的 FeatureCurrentState 屬性是唯讀屬性，會傳回指定功能目前已安裝的狀態。 如需狀態值的詳細資料，請參閱 FeatureRequestState 屬性。
ms.assetid: c4c325dc-6e7e-4009-8707-952c04574170
title: FeatureCurrentState 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3738a33d2c7a855abe6cc60139286b3e9c4d586bc6c2d9d436390fc5e52f4fd1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629228"
---
# <a name="sessionfeaturecurrentstate-property"></a>FeatureCurrentState 屬性

[**Session**](session-object.md)物件的 **FeatureCurrentState** 屬性是唯讀屬性，會傳回指定功能目前已安裝的狀態。 如需狀態值的詳細資料，請參閱 [**FeatureRequestState**](session-featurerequeststate.md) 屬性。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Session.FeatureCurrentState
```



## <a name="property-value"></a>屬性值

要求的功能所需的字串名稱，以及 [功能資料表](feature-table.md)中的主鍵。

## <a name="remarks"></a>備註

如果屬性失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**會話**](session-object.md)
</dt> <dt>

[**FeatureRequestState 屬性**](session-featurerequeststate.md)
</dt> </dl>

 

 




