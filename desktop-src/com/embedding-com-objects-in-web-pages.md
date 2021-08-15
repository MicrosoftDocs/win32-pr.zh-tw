---
title: 在網頁中內嵌 COM 物件
description: 您可以在網頁中使用 COM 物件。 若要這樣做，請先建立該 COM 物件的實例。 建立物件實例之後，您可以在該網頁的後續腳本中使用它。
ms.assetid: 7e2c9da7-aeae-4206-8be9-1303240b2b1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d13a92bd2de152e71ac4284ce37b977e8305f25dcb2aef5eb94d6019d115812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736889"
---
# <a name="embedding-com-objects-in-web-pages"></a>在網頁中內嵌 COM 物件

您可以在網頁中使用 COM 物件。 若要這樣做，請先建立該 COM 物件的實例。 建立物件實例之後，您可以在該網頁的後續腳本中使用它。

若要在網頁中建立 COM 物件實例，您可以使用物件標記。 或者，如果您的指令碼語言提供原生的方式來建立 COM 物件，您就可以使用腳本來建立物件實例。

請注意，在網頁中內嵌 COM 物件僅適用于支援 ActiveX 和 COM 的瀏覽器，例如 Internet Explorer。

下列範例說明如何使用物件標記，在網頁中內嵌 COM 物件：

``` syntax
<OBJECT 
  ID = vid 
  CLASSID = "clsid:31263EC0-2957-11CF-A1E5-00AA9EC79700" 
  BORDER = 0 
  VSPACE = 0 
  HSPACE = 0 
  ALIGN = TOP 
  HEIGHT = 100% 
  WIDTH = 100%
>
</OBJECT>
 
```

如果您的指令碼語言提供建立 COM 物件的方法，您也可以在腳本中建立 COM 物件實例。 例如，VBScript 提供 CreateObject 方法，JScript 提供 ActiveXObject 物件。 下列範例說明如何在腳本中建立物件。

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Dim objXL
  Set objXL = CreateObject("Excel.Application")
</SCRIPT>
 
<SCRIPT LANGUAGE = "JScript">
  var objXL = new ActiveXObject("Excel.Application");
</SCRIPT>
 
```

除了 CreateObject 方法和 ActiveXObject 物件之外，VBScript 和 JScript 都會提供 GetObject 的方法，以傳回物件實例。

建立 COM 物件之後，您可以使用物件標記識別項屬性中指定的識別碼，在後續的腳本中參考它。 在上述範例中，此識別碼已指定為「vid」。 請注意，使用 COM 物件的腳本必須出現在建立物件實例的物件標記或腳本之後;否則，物件識別碼是未定義的。 下列腳本會使用 objXL 物件來顯示 Microsoft Excel 的版本資訊。

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Msgbox objXL.Version
</SCRIPT>
 
```

如果您要撰寫內嵌于網頁的腳本，則瀏覽器也會公開您的腳本可以存取的物件模型。 Internet Explorer 所使用的模型符合全球資訊網協會 (W3C) 所建議的檔物件模型 (DOM) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 COM 物件編寫腳本](scripting-with-com-objects.md)
</dt> </dl>

 

 




