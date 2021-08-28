---
title: /backward_compat 參數
description: /Backward \_ 相容性參數會指示 MIDL 編譯器在產生 RPC/COM 存根時關閉一些 advanced 功能。
ms.assetid: eec0ade7-30a0-44e4-92e9-fb03ff657723
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd412bdabe4255a9a4538503b29ddf5681265ce5e16c81d3d5fc2484eb6c9675
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086388"
---
# <a name="backward_compat-switch"></a>/backward \_ 相容性參數

/Backward \_ 相容性參數會指示 MIDL 編譯器在產生 RPC/COM 存根時關閉一些 advanced 功能。

``` syntax
midl /backward_compat { maybenull_sizeis | zeroout_alignmentgap | 
     BSTR_byvalue_escaping | string_defaultvalue | signed_wchar_t }
```

## <a name="switch-options"></a>切換選項

*maybenull \_ sizeis*<dl> 將[ \[ 停用 \_ 一致性 \_ 檢查 \] ](disable-consistence-check.md)屬性套用至整個 MIDL 編譯。  
</dl>

*zeroout \_ alignmentgap*<dl> 關閉已封送處理之緩衝區中的清空間距。  
</dl>

*BSTR \_ byvalue \_ 轉義*<dl> 指示 MIDL 編譯器接受 escape 序列，例如 \\ bstr 中的̃ nâ€™或̃ \\ tâ€™。  
</dl>

*字串 \_ defaultvalue*<dl> 強制 MIDL 編譯器將 [**\[ defaultvalue \]**](defaultvalue.md)屬性中的字串強制轉換成 VARIANT。VT \_ I4 型別，請先將值強制轉換成正確的型別。  
</dl>

*簽署的 \_ wchar \_ t*<dl> 指示 MIDL 將 wchar \_ t 類型視為已簽署，以提供 Visual Basic 的相容性。  
</dl>

## <a name="remarks"></a>備註

-   *maybenull \_ sizeis*：請參閱 \[ 停用 \_ 一致性 \_ 檢查 \] 。
-   *zeroout \_ alignmentgap*：當 idl 是以「目標 NT60」或更高版本編譯時，MIDL 將會建立存根，使其在連線緩衝區內的成員或結構之間有任何對齊間距。 命令列參數 */backward \_ 相容性 zeroout \_ alignmentgap* 指示 MIDL 停用此功能。

    在下列範例結構中，網路緩衝區包含7個位元組對齊間距，以將超成員對齊 char 成員之後的8個。 使用「目標 NT60 或更高版本時，MIDL 將會零出該間距，除非使用參數。

    IDL 檔案：

    ``` syntax
    typedef struct _structwithgaps{
        char c;
        // 7 byte gap to align the following hyper to 8 
        hyper h;
    } structwithgap;
    ```

    此參數可讓洩漏的風險大幅增加，進而大幅改善效能。

-   *BSTR \_ byvalue \_* escape：根據預設，MIDL 編譯器不會 \\ \\ 在將字串常數轉換成類型 vt \_ TÂ或 vt LPSTR 時，處理 OLE Automation 的字串常數中的 escape 序列，例如̃ nâ€™或€̃ LPWSTR €™ \_ 。 使用這個回溯相容性切換選項，就會評估 escape 序列。
-   *字串 \_ defaultvalue*：強制 MIDL 編譯器將 [**\[ \] defaultvalue**](defaultvalue.md)屬性中的數值字串強制轉換成 VARIANT。VT \_ I4 型別，請先將值強制轉換成正確的型別。 這可能會導致在某些情況下遺失精確度，因此不建議使用此切換選項。
-   *帶正負號的 \_ wchar \_ t*：指示 MIDL 將 wchar \_ t 類型視為已簽署，以提供 Visual Basic 的相容性。

 

 




