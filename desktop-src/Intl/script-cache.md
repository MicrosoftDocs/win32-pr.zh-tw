---
description: 定義 Uniscribe 字型度量快取。
ms.assetid: 56a98529-6ae9-4b71-bd7d-cf056a1e3683
title: 'SCRIPT_CACHE (Usp10) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece29fe0ed610b4576263c36c50311ef57317579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988970"
---
# <a name="script_cache"></a>腳本 \_ 快取

定義 Uniscribe 字型度量快取。


```C++
typedef void* SCRIPT_CACHE;
```



## <a name="remarks"></a>備註

這是不透明的結構。 應用程式必須 \_ 針對所使用的每個字元樣式，配置和保留一個腳本快取變數。 變數必須初始化為 **Null**。

許多腳本函式都採用硬體裝置內容控制碼和腳本快取 \_ 變數的組合。 Uniscribe 會先嘗試使用腳本快取變數來存取字型資料 \_ 。 如果尚未快取所需的資料，它只會檢查硬體裝置內容。

硬體裝置內容控制碼可傳遞至 Uniscribe 作為 **Null**。 如果已快取 Uniscribe 所需的資料，則不會存取裝置內容，而且作業會繼續正常運作。

如果裝置內容傳遞為 **Null** ，而 Uniscribe 需要基於任何原因存取它，Uniscribe 會傳回錯誤碼 E E \_ 擱置。 這段程式碼會快速傳回，讓應用程式避免耗時的 [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject) 呼叫。

## <a name="examples"></a>範例

下列範例適用于所有採用腳本快取變數的函 \_ 式，以及選擇性的硬體裝置內容控制碼。


```C++
hr = ScriptShape(NULL, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
if (hr == E_PENDING)
{
    // ... select font into hdc ...
    hr = ScriptShape(hdc, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Usp10。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Uniscribe 結構](uniscribe-structures.md)
</dt> <dt>

[Caching](caching.md)
</dt> </dl>

 

 
