---
description: Merge 物件的 CreateSourceImage 方法可讓用戶端在合併後將模組中的檔案解壓縮到磁片上的來源影像，並將變更模組設定期間可能進行的模組變更納入考慮。
ms.assetid: c3e3465a-d5a7-4fcc-b26a-5a8c763c23d9
title: 'CreateSourceImage 方法 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CreateSourceImage
- IMsmMerge.CreateSourceImage
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: e8d9365a69ff6f33c2989e9102bac7c9c22166aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990205"
---
# <a name="mergecreatesourceimage-method"></a>Merge. CreateSourceImage 方法

[**Merge**](merge-object.md)物件的 **CreateSourceImage** 方法可讓用戶端在合併後將模組中的檔案解壓縮到磁片上的來源影像，並將變更模組設定期間可能進行的模組變更納入考慮。 合併處理期間，會從模組的檔案資料表中取出要解壓縮的檔案清單。 檔案清單是由從模組的檔案資料表成功複製到目標資料庫的每個檔案所組成。 由於主鍵與資料庫中現有的資料列衝突，所以未複製的檔案資料表專案不是此清單的一部分。 在建立映射時，這些檔案的每個目錄都是來自開啟的 (後置合併) 資料庫。 *Path* 參數中指定的路徑是安裝來源映射的根目錄。 *fLongFileNames* 會判斷路徑區段和最終檔案名是否使用長檔名。 如果沒有開啟任何資料庫、未開啟任何模組，或尚未執行任何合併，則函數會失敗。

## <a name="syntax"></a>語法


```JScript
Merge.CreateSourceImage(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*路徑* 
</dt> <dd>

要安裝之來源映射的根目錄路徑。

</dd> <dt>

*fLongFileNames* 
</dt> <dd>

*fLongFileNames* 會判斷路徑區段和最終檔案名是否使用長檔名。

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

請參閱 [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage) 函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 2.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




