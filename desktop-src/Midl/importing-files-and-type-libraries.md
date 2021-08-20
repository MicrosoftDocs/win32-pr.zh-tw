---
title: 匯入檔案和型別程式庫
description: MIDL 關鍵字包括、匯入和 importlib，可讓您藉由參考現有的標頭、IDL 和物件定義語言 (ODL) 檔和編譯的類型程式庫來重複使用程式碼。
ms.assetid: b4571c1d-4bd7-4ab1-9ef6-14356a6c4bb4
keywords:
- Microsoft 介面定義語言 MIDL、工作、匯入檔案和型別程式庫
- 匯入 MIDL
- 類型程式庫 MIDL，匯入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099ada5122ad024e342148bf3c453df0bd50872e6d59a2bbabd7d2892af5f93a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013736"
---
# <a name="importing-files-and-type-libraries"></a>匯入檔案和型別程式庫

MIDL 關鍵字 [**包括**](include.md)、匯 [**入**](import.md)和 [**importlib**](importlib.md) ，可讓您藉由參考現有的標頭、IDL 和物件定義語言 (ODL) 檔和編譯的類型程式庫來重複使用程式碼。

ACF [**include**](include.md) 指示詞可讓您在 ACF 檔中指定要包含在 MIDL 產生的存根程式碼中的一或多個 C 語言標頭檔。 產生的檔案會有一行包含 C 預處理器指示詞，其中 **\# 包含** 指定的標頭檔。 使用這個 **include** 指示詞來帶入特定作業環境專屬的標頭檔，而不包含用戶端與伺服器之間的介面所需的資訊。 針對包含您要提供給 IDL 檔案之資料類型的標頭檔，請勿使用 **include** ：請改用 [**import**](import.md) 指示詞。

## <a name="example-1"></a>範例 1

``` syntax
[
  auto_handle
] 
interface X86PC
{ 
  include "gendefs.h", "protos.h", "myfile.h"; 
  //interface typdefs and function declarations here
}
```

IDL 匯 [**入**](import.md) 指示詞是一種標準方法，可將其他 IDL (或 ODL) 檔案和標頭檔中的型別和介面定義帶入 IDL 檔案中。 匯入的檔案中的所有 IDL 語句，例如 typedef、 [**const**](const.md) 宣告和介面定義，都會變成可供匯入的 IDL 檔案使用。

如同 C 語言預處理器指示詞， [**import-module**](import.md)會告知編譯器 **\# 要包含匯** 入的 IDL 檔案中所定義的資料類型。 和 **\# include** 指示詞不同，匯 **入** 指示詞會忽略程式原型，因為匯入檔案中的任何作業都不會產生任何 stub。 因為會針對匯入的檔案個別叫用預處理器，所以預處理器指示詞 (例如 * * ) 不會延續至匯入的 IDL 檔。

如需使用匯 [**入**](import.md) 在 IDL 檔案中包含系統標頭檔的詳細資訊，請參閱匯 [入系統標頭檔](importing-system-header-files.md)。

## <a name="example-2"></a>範例 2

``` syntax
[
  uuid(. . .), object
] 
interface IKnown : IUnknown
{
  import "base.idl", "unknwn.idl", "helper.idl";
  //remainder of interface definition
}
```

ODL [**importlib**](importlib.md) 指示詞可讓您參考 IDL 或 ODL 檔案中已編譯的類型程式庫。 **Importlib** 指示詞必須在程式庫 [**語句內**](library.md)，而且必須在程式庫中的其他類型描述之前。 匯入的程式庫以及產生的程式庫，都必須可供應用程式在執行時間使用。

## <a name="example-3"></a>範例 3

``` syntax
library NewBrowser
{
  importlib("stdole32.tlb");
  importlib("legacy.tlb");
  //remainder of library definition
};
```

您也可以使用 C 預處理器 **\# include** 指示詞，在 IDL 或 ODL 檔案中包含標頭和其他檔案。 不過請注意，這個指示詞實際上會包含指定檔案的整個內容。 如果標頭檔包含在 MIDL 產生的存根檔案中不需要或不想要的原型，或包含不可遠端處理類型定義，則您應該使用 MIDL 匯 [**入**](import.md)指示詞，而不是 **\# include** 指示詞。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**進口**](import.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**包括**](include.md)
</dt> <dt>

[匯入系統標頭檔](importing-system-header-files.md)
</dt> </dl>

 

 




