---
title: importlib 屬性
description: '\ Importlib \ 指示詞會讓已編譯成另一個類型程式庫的類型可用於建立的類型程式庫。'
ms.assetid: d5f15a77-c6b1-4918-be86-07d2995ca2d4
keywords:
- importlib 屬性 MIDL
topic_type:
- apiref
api_name:
- importlib
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c83d5c4b19800f92e3080d3fb435ddd20d62e4b6fe76986869a0f4da86deabcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895068"
---
# <a name="importlib-attribute"></a>importlib 屬性

**\[ Importlib \]** 指示詞會讓已編譯成另一個類型程式庫的類型，可供建立的類型程式庫使用。

``` syntax
[
    library-attributes
]
library (library-name)
{
    importlib(file-to-import); 
    ... 
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*程式庫-屬性* 
</dt> <dd>

將套用至程式庫的零或多個屬性。

</dd> <dt>

*程式庫名稱* 
</dt> <dd>

軟體元件將用來表示此連結 [**庫**](library.md)的識別碼。

</dd> <dt>

*匯入檔案* 
</dt> <dd>

在 MIDL 編譯時期匯入之檔案的名稱和位置。

</dd> </dl>

## <a name="remarks"></a>備註

所有的 **\[ importlib \]** 指示詞都必須在程式庫中的其他類型描述之前。 請注意，匯入的程式庫以及產生的程式庫都必須與應用程式一起散發，才能在執行時間使用。

在大部分情況下，您應該使用 MIDL 匯入指示詞 **\[** [](import.md) **\]** 來參考另一個的定義。中的 IDL 檔。IDL 檔案。 這個方法會提供您的型別程式庫與原始檔案中的所有資訊，而 **\[ importlib \]** 只會帶入類型程式庫的內容。

> [!Note]  
> **\[ Importlib \]** 指示詞會讓所匯入的程式庫中定義的任何類型都可從正在編譯的程式庫中存取。 為了避免在有重複的參考時不清楚，我們建議您使用適當的程式庫名稱來限定每個這類參考，如下所示：

 

``` syntax
library_name.type
```

在沒有這類限定性的情況下，MIDL 會解析重複的參考，如下所示：

-   自3.1 版起，MIDL 會使用它所找到的第一個參考。
-   MIDL 的3.0 版（midl 的第一個版本，可以產生類型程式庫）會使用所找到的最後一個參考。

## <a name="examples"></a>範例

``` syntax
library BrowseHelper 
{ 
    importlib("stdole32.tlb"); 
    importlib("mydisp.tlb"); 
    //Remainder of library definition 
};
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**圖書館**](library.md)
</dt> <dt>

[**進口**](import.md)
</dt> <dt>

[匯入系統標頭檔](importing-system-header-files.md)
</dt> <dt>

[匯入檔案和型別程式庫](importing-files-and-type-libraries.md)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 