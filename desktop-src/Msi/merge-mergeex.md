---
description: Merge 物件的 MergeEx 方法相當於 Merge 函式，但它會接受額外的引數。
ms.assetid: 83b6d62b-d176-42ac-b513-d1c2e562965c
title: 'MergeEx 方法 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.MergeEx
- IMsmMerge.MergeEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 7e683597d78e568e6bfec9b59241fe45f922c5346ef83f427598ad0a7c59dcac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926528"
---
# <a name="mergemergeex-method"></a>Merge. MergeEx 方法

[**Merge**](merge-object.md)物件的 **MergeEx** 方法相當於 [**merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge)函式，但它會接受額外的引數。 *PConfiguration* 引數是用戶端所執行的介面。 引數可以是 null。 此引數的存在表示用戶端能夠支援設定功能，但不會商都必須用戶端來提供任何特定可設定專案的設定資料。

[**Merge**](merge-merge.md)方法會執行目前資料庫和目前模組的合併。 合併會將模組中的元件附加至 *功能* 所識別的功能。 模組目錄樹狀結構的根會重新導向至 *RedirectDir* 所指定的位置。

## <a name="syntax"></a>語法


```JScript
Merge.MergeEx(
  Feature,
  RedirectDir,
  pConfiguration
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

</dd> <dt>

*pConfiguration* 
</dt> <dd>

*PConfiguration* 引數是用戶端所執行的介面。 引數可以是 null。 此引數的存在表示用戶端能夠支援設定功能，但不會商都必須用戶端來提供任何特定可設定專案的設定資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

完成合併之後，模組中的元件會附加至 *功能* 所識別的功能。 這項功能不會建立，且必須是現有的功能。 您可以使用 [**連線**](merge-connect.md)方法，將模組附加至其他功能。

只有在呼叫 [**CloseDatabase**](merge-closedatabase.md) 方法並將 *BCommit* 設為 **TRUE** 時，才會儲存對資料庫所做的變更。

如果發生任何合併衝突（包括排除），則會將它們放在錯誤列舉值中供稍後抓取，但不會導致合併失敗。 錯誤可能會透過 [ [**錯誤**](merge-errors.md) ] 屬性來抓取。 錯誤和參考用訊息會張貼至目前的記錄檔。

當合併因為模組設定不正確而失敗時， [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) 函數會傳回 E \_ FAIL。 這包括下列 msmErrorType 錯誤： **msmErrorBadNullSubstitution**、 **msmErrorBadSubstitutionType**、 **msmErrorBadNullResponse**、 **msmErrorMissingConfigItem** 和 **msmErrorDataRequestFailed**。 這些錯誤會導致合併在遇到錯誤時立即停止。 當 **MergeEx** 傳回 E 失敗時，錯誤物件仍會加入至列舉值 \_ 。 如需有關 msmErrorType 錯誤的詳細資訊，請參閱 [**取得 \_ 型別函數 (Error 物件)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type)。 所有其他錯誤都會導致 **MergeEx** 傳回 \_ FALSE，並導致合併繼續。

### <a name="c"></a>C++

請參閱 [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) 函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | Mergemod.dll 2.0 或更新版本<br/>                                                    |
| 標頭<br/>  | <dl> <dt>Mergemod。h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
