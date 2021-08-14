---
title: /char 參數
description: /Char 參數有助於確保 MIDL 編譯器和 C 編譯器都能正確地針對所有 char 和 small 類型運作。
ms.assetid: 83f204cf-9cd0-42f3-bce7-b8f582e50e67
keywords:
- /char 參數 MIDL
topic_type:
- apiref
api_name:
- /char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb459f7c2d6ff98a35e139cf07d9d95c4bed575e52b3d20258f570f07297943
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963188"
---
# <a name="char-switch"></a>/char 參數

**/Char** 參數有助於確保 MIDL 編譯器和 C 編譯器都能正確地針對所有 [**char**](char-idl.md)和 [**small**](small.md)類型運作。

``` syntax
midl /char { signed | unsigned | ascii7 }
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="signed"></span><span id="SIGNED"></span>

<span id="signed"></span><span id="SIGNED"></span>已簽署 * * * *


</dt> <dd>

指定 [**char**](char-idl.md) 的預設 C 編譯器類型已簽署。 不帶正負號規格的所有 **字元** 都是以不帶正負號的字元產生。

</dd> <dt>

<span id="unsigned"></span><span id="UNSIGNED"></span>

<span id="unsigned"></span><span id="UNSIGNED"></span>未簽署 * * * *


</dt> <dd>

指定 [**char**](char-idl.md) 的預設 C 編譯器類型不帶正負號。 所有不帶正負號規格的使用都會產生為帶正負 [**號的小型**](small.md) 。

</dd> <dt>

<span id="ascii7"></span><span id="ASCII7"></span>

<span id="ascii7"></span><span id="ASCII7"></span>ascii7****


</dt> <dd>

指定所有 [**char**](char-idl.md) 值都必須傳遞至產生的檔案，但不含特定的 sign 關鍵字。 所有 [**不帶**](small.md) 正負號規格的使用都是以 **較小** 的方式產生。

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>備註

根據定義，MIDL [**char**](char-idl.md) 不帶正負號。 "Small" 是以 **char** 定義 \# ， (定義 Small char) ，而且 MIDL [**small**](small.md) 會經過簽署。

當 C 編譯器簽署宣告與該型別的 MIDL 預設衝突時， **/char** 參數會指示 MIDL 編譯器在產生的檔案中指定明確 [**帶**](signed.md) 正負號或不 [**帶正負**](unsigned.md) 號聲明。

請記住，MIDL 編譯器會以 C 原始程式碼形式產生存根，您必須將它編譯為用戶端和伺服器程式的一部分。 某些編譯器會在原始程式碼中指定 [**字元**](char-idl.md)資料的任何地方使用 **帶正負** 號的字元。 MIDL 編譯器產生的存根原始程式碼會將所有 **char** 資料視為不 **帶正負** 號的 char。 如果 MIDL 編譯器只是將 IDL 檔案中的所有 **char** 資料產生為存根中的 **char** 資料，則使用 **帶正負** 號 char **資料的** 編譯器會在存根原始程式碼中造成衝突。

**/Char** 命令列參數的目的是要解決這些潛在衝突。 它會將 IDL 檔案中指定為 [**char**](char-idl.md) 的所有資料保留為存根原始程式碼中的不 **帶正負號字元** 。 它也會將 [**小型**](small.md) 資料維護為已簽署。

下表摘要說明產生的類型。



| midl/char 選項       | 產生的 char 類型 | 產生的小型類型 |
|-------------------------|---------------------|----------------------|
| **midl/char 已簽署**   | **unsigned char**   | **small**            |
| **midl/char 未簽署** | **char**            | **帶正負號**     |
| **midl/char ascii7**   | **char**            | **small**            |



 

**/Char** 帶正負號選項表示 C 編譯器字元和小型類型已簽署。 若要比對 **char** 的 midl 預設值，MIDL 編譯器必須將未伴隨正負號規格之 **char** 的所有用法轉換成不帶正負號的 **char**。 因為這個 C 編譯器預設值符合 **small** 的 MIDL 預設值，所以不會修改 [**small**](small.md)型別。

**/Char** 未簽署選項表示 C 編譯器 [**char**](char-idl.md)類型未簽署。 MIDL 編譯器會將 [**small**](small.md) 未伴隨正負號規格的所有用法轉換成 **帶正負** 號的 **小**。

Ascii7 選項表示不會將明確的正負號規格新增至 [**char**](char-idl.md) 類型。 [**Small**](small.md)類型會產生為 **small**。

為了避免混淆，您應該盡可能在 IDL 檔案中使用 [**char**](char-idl.md) 和 small 類型的明確簽署規格。 請注意，DCE IDL 不支援在 IDL 檔案中使用明確簽署的 **char** 類型。 因此，當您使用 MIDL [**/osf**](-osf.md) 參數進行編譯時，就無法使用這項功能。

如需 **/char** 的相關資訊，請參閱 [**small**](small.md)。

## <a name="examples"></a>範例

**midl/char 簽署的檔案名 .idl**

**midl/char 不帶正負號的檔案名 .idl**

**midl/char ascii7 filename .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**char**](char-idl.md)
</dt> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**小**](small.md)
</dt> </dl>

 

 




