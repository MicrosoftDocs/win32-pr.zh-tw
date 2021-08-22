---
description: Merge 物件的 ExtractFiles 方法會從模組中解壓縮內嵌的 .cab 檔案，然後將這些檔案寫入目的地目錄。
ms.assetid: 846355d6-32f2-4b04-91dc-acd60445fbd9
title: 'ExtractFiles 方法 (Advpub .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFiles
- IMsmMerge.ExtractFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: e56d6572526e2aecfc12dc5b2bb9a365be6d3c53b6fb1707fe197c056d05c377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926558"
---
# <a name="mergeextractfiles-method"></a>Merge. ExtractFiles 方法

[**Merge**](merge-object.md)物件的 **ExtractFiles** 方法會從模組中解壓縮內嵌的 .cab 檔案，然後將這些檔案寫入目的地目錄。

## <a name="syntax"></a>語法


```JScript
Merge.ExtractFiles(
  Path
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*路徑* 
</dt> <dd>

完整的目的地目錄。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

目的地目錄中具有相同名稱的任何檔案都會遭到覆寫。 如果路徑不存在，則會建立路徑。

**ExtractFiles** 一律會使用路徑的簡短檔案名來解壓縮檔案。 若要針對路徑使用長檔名，請使用 [**ExtractFilesEx 方法**](merge-extractfilesex.md)。

### <a name="c"></a>C++

請參閱 [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) 函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 1.0 或更新版本<br/>                                                                     |
| 標頭<br/>  | <dl> <dt>Advpub (包含 Mergemod) </dt> </dl> |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl>                  |



 

 
