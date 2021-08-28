---
description: Session 物件的 ComponentCosts 屬性會傳回 RecordList 物件，以列舉安裝元件所需的每個磁片磁碟機的磁碟空間。
ms.assetid: 9b1355f1-cc99-49d9-8187-07fba4804d1f
title: ComponentCosts 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCosts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 643996bccd352695651fb55f2ddcb33c0888773f4d99283f646a7fcb498c4074
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629518"
---
# <a name="sessioncomponentcosts-property"></a>ComponentCosts 屬性

[**Session**](session-object.md)物件的 ComponentCosts 屬性會傳回 [**RecordList**](recordlist-object.md)物件，以列舉安裝元件所需的每個磁片磁碟機的磁碟空間。 使用者介面會使用這項資訊來顯示所有磁片磁碟機所需的磁碟空間。 傳回的磁碟空間成本是512個位元組的倍數。

ComponentCosts 屬性只應在安裝程式完成檔案 [成本](file-costing.md) 及 [CostFinalize 動作](costfinalize-action.md)之後使用。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Session.ComponentCosts
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

若要取得總成本，請新增所有元件的成本加上安裝程式引擎成本 (Component = "" ) 。

ComponentCosts 會傳回 [**RecordList 物件**](recordlist-object.md)。 傳回之 RecordList 物件中的每一筆記錄都有下欄欄位：



| 欄位 | 描述                                          |
|-------|------------------------------------------------------|
| 1     | 磁片區/磁片磁碟機名稱                                    |
| 2     | 最終磁碟空間的成本為512個位元組的倍數。     |
| 3     | 暫存磁碟空間的成本為512個位元組的倍數。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




