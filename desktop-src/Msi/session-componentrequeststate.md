---
description: Session 物件的 ComponentRequestState 屬性會取得或要求元件資料表中資料列的動作狀態變更。
ms.assetid: d0b50c25-dca6-4bdf-8ee9-490e436fcc5b
title: ComponentRequestState 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 17ec77c5498a808e0d7ac0f2881057979d7db0c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983073"
---
# <a name="sessioncomponentrequeststate-property"></a>ComponentRequestState 屬性

[**Session**](session-object.md)物件的 **ComponentRequestState** 屬性會取得或要求 [元件資料表](component-table.md)中資料列的動作狀態變更。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Session.ComponentRequestState
```



## <a name="property-value"></a>屬性值

元件專案的必要字串名稱、元件資料表的主要索引鍵。

## <a name="remarks"></a>備註



| 選取狀態        | 值 | 描述                                                    |
|------------------------|-------|----------------------------------------------------------------|
| Null                   | Null  | 要求不對此專案採取任何動作。                |
| msiInstallStateAbsent  | 2     | 要移除的專案。                                         |
| msiInstallStateLocal   | 3     | 專案要安裝在本機。                               |
| msiInstallStateSource  | 4     | 專案會從來源媒體安裝和執行。         |
| msiInstallStateDefault | 5     | 如果已安裝，則會以相同的狀態重新安裝專案。 |



 

如果屬性失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




