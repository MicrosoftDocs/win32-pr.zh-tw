---
title: 使用 Active Server Pages 中的 COM 物件
description: 您可以在 Active Server Pages (ASP) 應用程式中編寫 COM 物件的腳本。
ms.assetid: 3a074360-8b6c-4cb6-813b-73863fe11c46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8ba1bbdd0729a8893b1c28d1a2347fc5ddea04c8d0de4e1ea413e765ab8df4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896197"
---
# <a name="using-com-objects-in-active-server-pages"></a>使用 Active Server Pages 中的 COM 物件

您可以在 Active Server Pages (ASP) 應用程式中編寫 COM 物件的腳本。 若要這樣做，您必須先使用物件標記或呼叫 ASP Server 物件的 CreateObject 方法，建立物件的實例。 一旦建立 COM 物件之後，您就可以在 ASP 頁面的後續腳本中使用它。

您可以使用 ASP 來處理許多不同類型的腳本引擎，每種引擎都支援不同的指令碼語言。 ASP 隨附 VBScript 和 JScript 腳本引擎。 您也可以插入由其他公司開發的腳本引擎，以支援 PerlScript、PScript、Python 等語言。

如果您未設定 ASP 頁面的指令碼語言，則預設值為 VBScript。 若要指定 VBScript 以外的指令碼語言，請在每個 ASP 頁面頂端加入一行，如下所示：

``` syntax
<%@ LANGUAGE=JScript %>
 
```

若要在 ASP 頁面中使用 COM 物件，您必須先建立該物件的實例。 若要這麼做，請使用物件標記並為 RUNAT 屬性指定 "SERVER" 值，如下列範例所示。 根據預設，物件標記會在用戶端上建立物件的實例。 將 RUNAT 屬性設定為 [伺服器] 會在伺服器上建立物件。 物件必須在伺服器上執行，ASP 才能使用。

``` syntax
<OBJECT 
RUNAT=SERVER 
ID=MyAds 
CLASSID="Clsid:1621F7C0-60AC-11CF-9427-444553540000">
</OBJECT> 
 
```

您也可以藉由呼叫 ASP 伺服器物件的 CreateObject 方法，在 ASP 頁面上建立 COM 物件的實例。 使用 CreateObject 比使用物件標記建立物件慢，但是它會稍微更容易讀取，因為它會指定程式設計的識別碼，而不是 COM 物件的類別識別碼。 伺服器物件是由 ASP 公開，不需要建立。 如何呼叫 CreateObject，如下列範例所示。 第一個範例是 VBScript：

``` syntax
<% 
  Set MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

下一個範例是 JScript：

``` syntax
<% 
  var MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

呼叫 CreateObject 比使用物件標記來建立 COM 物件慢。 在效能很重要的應用程式中，您應該使用物件標記。

建立 COM 物件的實例之後，您可以在腳本中使用它。 這會在下列 VBScript 範例中說明，此範例會設定 COM 物件的 Border 屬性值。

``` syntax
<% MyAds.Border = 0 %>
 
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 COM 物件編寫腳本](scripting-with-com-objects.md)
</dt> </dl>

 

 




