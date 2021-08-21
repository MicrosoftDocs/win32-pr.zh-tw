---
description: GetFiles 物件的 ModuleFiles 屬性會針對目前開啟的模組，傳回檔案資料表的所有主要索引鍵。
ms.assetid: e1c8049c-b271-4def-abde-89ea99393574
title: 'GetFiles. ModuleFiles 屬性 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles.ModuleFiles
- IMsmGetFiles.get_ModuleFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: b4b7d498979c94de048e72058df4c8bf87fb8607220efe808554d66deb5d89ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635938"
---
# <a name="getfilesmodulefiles-property"></a>GetFiles. ModuleFiles 屬性

[**GetFiles**](getfiles-object.md)物件的 **ModuleFiles** 屬性會針對目前開啟的模組，傳回檔案 [資料表](file-table.md)的所有主要索引鍵。 主要索引鍵會以字串集合的形式傳回。 在呼叫 **ModuleFiles** 之前，必須先呼叫 [Merge 物件](merge-object.md)的 [**OpenModule**](merge-openmodule.md)方法來開啟模組。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = GetFiles.ModuleFiles
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

請注意，集合中列出的檔案順序可能不會與 File 資料表中所列的順序相同。

如果模組沒有檔案資料表，或不包含特定語言的任何檔案，ModuleFiles 會傳回空的字串集合。

### <a name="c"></a>C++

請參閱 [**get \_ ModuleFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) 函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 1.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
