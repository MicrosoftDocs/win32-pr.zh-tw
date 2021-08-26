---
description: Session 物件的 ComponentCurrentState 屬性是唯讀屬性，它會傳回指定元件的目前已安裝狀態。 如需狀態值的詳細資料，請參閱 ComponentRequestState 屬性。
ms.assetid: c8343e90-8867-462d-9844-e547341a590c
title: ComponentCurrentState 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ce060c7eddb76491480f4a1de9f477629da489ae9d8412adc02da25b8d7a0a1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039854"
---
# <a name="sessioncomponentcurrentstate-property"></a>ComponentCurrentState 屬性

[**Session**](session-object.md)物件的 **ComponentCurrentState** 屬性是唯讀屬性，它會傳回指定元件的目前已安裝狀態。 如需狀態值的詳細資料，請參閱 [**ComponentRequestState**](session-componentrequeststate.md) 屬性。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Session.ComponentCurrentState
```



## <a name="property-value"></a>屬性值

所要求元件的必要字串名稱，以及元件資料表中的主要金鑰。

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

[**ComponentRequestState 屬性**](session-componentrequeststate.md)
</dt> </dl>

 

 




