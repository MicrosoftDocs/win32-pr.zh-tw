---
description: Session 物件的 Sequence 方法會在指定的資料表上開啟查詢，並依 [順序] 資料行中的數位排序動作。
ms.assetid: cde735b0-0b97-4c4f-adfc-f0321aafb012
title: Session. Sequence 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Sequence
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 18708b79bdce73b29f46b4d62a15ceb8003d9c9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976254"
---
# <a name="sessionsequence-method"></a>Session. Sequence 方法

[**Session**](session-object.md)物件的 **Sequence** 方法會在指定的資料表上開啟查詢，並依 [順序] 資料行中的數位排序動作。 針對每個提取的資料列，如果任何提供的條件運算式未評估為 False，則會呼叫 [**dataadapter.doaction**](session-doaction.md) 方法。 傳回列舉 msiDoActionStatusEnum，如 [**dataadapter.doaction**](session-doaction.md) 方法中所述。

## <a name="syntax"></a>語法


```JScript
Session.Sequence(
  table
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*table* 
</dt> <dd>

要用於排序的資料表所需的字串名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

通常會由最上層動作在內部呼叫這個方法。

藉由呼叫 **sequence** 方法，無法執行包含更新系統之動作的動作序列，例如 [InstallFiles](installfiles-action.md)和 [WriteRegistryValues](writeregistryvalues-action.md)動作。 這項規則的例外狀況是從 [InstallInitialize](installinitialize-action.md)和 [InstallFinalize 動作](installfinalize-action.md)之間的 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中排程的自訂動作呼叫 **順序** 方法。 您可以呼叫不會更新系統的動作，例如 [AppSearch](appsearch-action.md) 或 [CostInitialize](costinitialize-action.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




