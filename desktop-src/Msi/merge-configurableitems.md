---
description: Merge 物件的唯讀 ConfigurableItems 屬性會傳回集合 ConfigurableItem 物件，每個物件都代表 ModuleConfiguration 資料表中的單一資料列。
ms.assetid: 4d1a64f7-fbd0-4358-8911-112e43f1be4a
title: 'Merge.ConfigurableItems 屬性 (Mergemod) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ConfigurableItems
- IMsmMerge.get_ConfigurableItems
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 179594ba7fe7691edb9abe1f72d104742fe9bc9e3a4a23b728ad8607b94c444a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013036"
---
# <a name="mergeconfigurableitems-property"></a>Merge.ConfigurableItems 屬性

[**Merge**](merge-object.md)物件的唯讀 **ConfigurableItems** 屬性會傳回集合 [**ConfigurableItem**](configurableitem-object.md)物件，每個物件都代表 [ModuleConfiguration 資料表](moduleconfiguration-table.md)中的單一資料列。 就語義而言，列舉值中的每個介面都代表一個可由模組取用者設定的專案。 集合是唯讀的集合，並會執行專案 () 、計數 () 和 NewEnum () 的標準唯讀集合介面 \_ 。 **IEnumMsmConfigItems** 列舉值會使用標準語義來執行下一個 () 、略過 () 、重設 () 和複製 () 。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Merge.ConfigurableItems
```



## <a name="property-value"></a>屬性值

## <a name="c"></a>C++

請參閱 [**get \_ ConfigurableItems**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) 函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 2.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




