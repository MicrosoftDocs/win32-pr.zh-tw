---
description: 相依性物件的唯讀模組屬性會傳回目前字串（以 BSTR 形式）所需的模組 ModuleID。 ModuleID 是在 ModuleSignature 資料表中使用的相同形式。
ms.assetid: 22aae1b6-59b6-4842-9523-d1e064511380
title: '相依性。 Module 屬性 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dependency.Module
- IMsmDependency.get_Module
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 1cd5ce697057a04d611dcf7f2f0cd0757874a27f869b5b6aa450d9c6bcc85209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378878"
---
# <a name="dependencymodule-property"></a>相依性。 Module 屬性

相依性 [**物件**](dependency-object.md)的唯讀 **模組** 屬性會傳回目前字串（以 **BSTR** 形式）所需的模組 ModuleID。 ModuleID 是在 [ModuleSignature 資料表](modulesignature-table.md)中使用的相同形式。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Dependency.Module
```



## <a name="property-value"></a>屬性值

## <a name="c"></a>C++

請參閱 [**IMsmDependency \_ 取得 \_ 模組**](/windows/win32/api/mergemod/nf-mergemod-imsmdependency-get_module) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 1.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

