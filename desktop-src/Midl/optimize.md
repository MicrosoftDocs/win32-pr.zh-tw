---
title: optimize 屬性
description: '\ Optimize \ ACF 屬性是用來微調將資料封送處理的階層層級。'
ms.assetid: d636d940-0550-417f-a21a-065bdeaeb5d9
keywords:
- optimize 屬性 MIDL
topic_type:
- apiref
api_name:
- optimize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7703a3539ff16c7f2dc78d51c62cfe05612dcb6e935bb5c5701f9a7b59a9f1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869568"
---
# <a name="optimize-attribute"></a>optimize 屬性

**\[ Optimize \]** ACF 屬性是用來微調將資料封送處理的階層層級。

> [!Note]  
> 這個關鍵字是取代，不應該使用。 目前的 MIDL 編譯應該改用 [**/Oicf**](-oi.md)[**/robust**](-robust.md) 。

 

``` syntax
optimize ("optimization-options")
```

## <a name="parameters"></a>參數

<dl> <dt>

*優化-選項* 
</dt> <dd>

指定封送處理資料的方法。 請使用 "s" 進行混合模式封送處理，或使用 "i" 進行解讀封送處理。

</dd> </dl>

## <a name="remarks"></a>備註

此版本的 RPC 提供兩種方法來封送處理資料：混合模式 ( "s" ) 並 ( "i" ) 進行解讀。 這些方法會對應至 [**/os**](-os.md) 和 [**/Oi**](-oi.md) 命令列參數。 解讀的方法會完全離線地封送處理資料。 雖然這可以大幅減少存根的大小，但效能可能會受到影響。

如果要考慮效能，混合模式方法可以是最佳的方法。 混合模式可讓 MIDL 編譯器判斷哪些資料會以內嵌方式進行封送處理，以及透過呼叫離線動態連結程式庫的方式進行封送處理。 如果有許多程式使用相同的資料類型，就可以重複呼叫單一程式來封送處理資料。 如此一來，最適合內嵌封送處理的資料會以內嵌方式處理，而其他資料可以更有效率地在離線時進行封送處理。

請注意， **\[ optimize \]** 屬性可用來做為介面屬性或做為作業屬性。 如果用來作為介面屬性，它會設定整個介面的預設值，覆寫命令列參數。 但是，如果使用它做為作業屬性，它只會影響該作業，覆寫命令列參數和介面預設值。

## <a name="examples"></a>範例

``` syntax
optimize ("s") HRESULT FasterProcedure(...); 
optimize ("i") HRESULT SmallerProcedure(...);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**/Os**](-os.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> </dl>

 

 




