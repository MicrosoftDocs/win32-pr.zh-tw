---
description: Merge 物件的 ExtractFilesEx 方法會從模組中解壓縮內嵌的 .cab 檔案，然後將這些檔案寫入目的地目錄。
ms.assetid: 8b063052-4f92-466a-9c52-bda26ed13d5c
title: 'ExtractFilesEx 方法 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFilesEx
- IMsmMerge.ExtractFilesEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: be6aa1001be0d3ecd6cbb9c4cd1d8c04b4649f10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995492"
---
# <a name="mergeextractfilesex-method"></a>Merge. ExtractFilesEx 方法

[**Merge**](merge-object.md)物件的 **ExtractFilesEx** 方法會從模組中解壓縮內嵌的 .cab 檔案，然後將這些檔案寫入目的地目錄。

## <a name="syntax"></a>語法


```JScript
Merge.ExtractFilesEx(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*路徑* 
</dt> <dd>

完整的目的地目錄。

</dd> <dt>

*fLongFileNames* 
</dt> <dd>

設定為使用路徑區段和最終檔案名的完整檔案名來指定。

</dd> <dt>

*pFilePaths* 
</dt> <dd>

這是已成功解壓縮之檔案的完整路徑清單。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

目的地目錄中具有相同名稱的任何檔案都會遭到覆寫。 如果路徑不存在，則會建立路徑。

### <a name="c"></a>C++

請參閱 [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) 函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 2.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




