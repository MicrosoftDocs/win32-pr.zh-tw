---
description: Session 物件的 EvaluateCondition 方法會評估包含符號和值的邏輯運算式。 這個方法會使用 MsiEvaluateCondition 函數。
ms.assetid: 629f7efd-80fe-4a0e-95cc-b62d6258ae0a
title: EvaluateCondition 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.EvaluateCondition
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6eb207d826b641e9295e4a3fa4fcda16e0b2769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987164"
---
# <a name="sessionevaluatecondition-method"></a>EvaluateCondition 方法

[**Session**](session-object.md)物件的 **EvaluateCondition** 方法會評估包含符號和值的邏輯運算式。 這個方法會使用 [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) 函數。

## <a name="syntax"></a>語法


```JScript
Session.EvaluateCondition(
  condition
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*條件* 
</dt> <dd>

包含邏輯運算式的必要字串。 如需詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回整數，指出條件的評估。



| 常數                  | 值 | 描述                               |
|---------------------------|-------|-------------------------------------------|
| msiEvaluateConditionFalse | 0     | 條件會評估為 false。         |
| msiEvaluateConditionTrue  | 1     | 條件評估為 true。          |
| msiEvaluateConditionNone  | 2     | 未提供條件運算式。 |
| msiEvaluateConditionError | 3     | 條件包含語法錯誤。    |



 

## <a name="remarks"></a>備註

條件運算式可以用來比較功能和元件狀態。 下表顯示 EvaluateCondition 方法所使用的功能和元件狀態。



| 狀態                 | 值 | 描述                                              |
|-----------------------|-------|----------------------------------------------------------|
| Null                  | Null  | 未對功能或元件採取任何動作。                 |
| msiInstallStateAbsent | 2     | 功能或元件不存在。                     |
| msiInstallStateLocal  | 3     | 功能或元件安裝在本機電腦上。 |
| msiInstallStateSource | 4     | 已安裝功能或元件以從來源執行。    |



 

> [!Note]  
> 在呼叫 [**SetInstallLevel**](session-setinstalllevel.md) 方法之前（不論是直接或透過 [CostFinalize 動作](costfinalize-action.md)），都不會設定狀態。 因此，狀態檢查只適用于動作順序資料表中的條件運算式。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[條件陳述式語法](conditional-statement-syntax.md)
</dt> </dl>

 

 




