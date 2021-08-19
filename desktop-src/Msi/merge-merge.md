---
description: Merge 物件的 Merge 方法會執行目前資料庫和目前模組的合併。
ms.assetid: 4b580b1f-5071-42f1-8022-a152817f9fdc
title: 'Merge 方法 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Merge
- IMsmMerge.Merge
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 43644f8ef19b81331f9f2d88d4dac03d654379d51174a50e994d3642cb86eabc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804728"
---
# <a name="mergemerge-method"></a>Merge 方法

[**Merge**](merge-object.md)物件的 **merge** 方法會執行目前資料庫和目前模組的合併。 合併會將模組中的元件附加至 *功能* 所識別的功能。 模組目錄樹狀結構的根會重新導向至 *RedirectDir* 所指定的位置。

**合併** 方法只能呼叫一次，以合併 .msi 和 .msm 檔案的特定組合。

## <a name="syntax"></a>語法


```JScript
Merge.Merge(
  Feature,
  RedirectDir
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*功能* 
</dt> <dd>

資料庫中的功能名稱。

</dd> <dt>

*RedirectDir* 
</dt> <dd>

資料庫 [目錄資料表](directory-table.md) 中專案的索引鍵。 這個參數可以是 null 或空字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

完成合併之後，模組中的元件會附加至 *功能* 所識別的功能。 這項功能不會建立，且必須是現有的功能。 請注意， **Merge** 方法會取得模組中的所有功能參考，並針對模組資料庫中所有出現的 null GUID 取代功能參考。 如需詳細資訊，請參閱 [合併模組中的參考功能](referencing-features-in-merge-modules.md)。

您可以使用 [**連線**](merge-connect.md)方法，將模組附加至其他功能。 請注意，呼叫 **連線** 方法只會建立功能元件關聯。 它不會修改已合併至資料庫的資料列。

只有在呼叫 [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) 方法並將 *BCommit* 設為 **TRUE** 時，才會儲存對資料庫所做的變更。

如果發生任何合併衝突（包括排除），則會將它們放在錯誤列舉值中供稍後抓取，但不會導致合併失敗。 錯誤可能會透過 [ [**錯誤**](error-object.md) ] 屬性來抓取。 錯誤和參考用訊息會張貼至目前的記錄檔。

### <a name="c"></a>C++

請參閱 [**合併**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 1.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
