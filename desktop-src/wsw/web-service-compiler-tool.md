---
title: Web 服務編譯器工具
description: 為了支援服務模型，wsutil.exe 會產生要用於用戶端和服務端的標頭。 它會視需要產生用戶端的 C proxy 檔案，以及服務端的 C 存根檔案。
ms.assetid: 1c73297d-0d3d-421c-9e19-44a6012a5c65
keywords:
- Windows 的 web 服務編譯器工具 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6789b9e2b6e38d89e422adc363326656b8f693e2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880985"
---
# <a name="web-service-compiler-tool"></a>Web 服務編譯器工具

為了支援服務模型，wsutil.exe 會產生要用於用戶端和服務端的標頭。 它會視需要產生用戶端的 C proxy 檔案，以及服務端的 C 存根檔案。


為了支援 [序列化](serialization.md)，編譯器會針對全域專案定義產生專案描述的標頭，並針對序列化引擎使用 proxy 檔案中的所有類型定義資訊。

使用方式

**WsUtil.exe \[ 命令列參數 \[ 參數-選項 \] ： \] &lt; filename&gt;**

命令列參數

指定 WsUtil.exe 編譯器選項。 參數可以依任何順序顯示。 虛線 ( '-' ) 和斜線 ( '/' ) 會視為相同。

命令列選項清單

-   @filename 指定應將輸入檔視為回應檔。 這個選項可以在引數清單中的任何位置使用多次。
-   /wsdl： &lt; filename &gt; ： <選擇性 \_ url> 指定應將輸入檔視為 wsdl 檔。 允許多個 wsdl 輸入，並處理所有指定的 wsdl 檔案。 選擇性 url 會指定從中抓取 \_ 中繼資料的位置。 如果未 \_ 指定選擇性的 url，Wsutil 會在內部產生唯一的 url。 另請參閱 [原則支援](policy-support.md)。
-   /xsd： &lt; filename &gt; 指定應將輸入檔案名視為架構檔。 允許多個 xsd 輸入，並處理所有指定的架構檔案。
-   /wsp： &lt; filename &gt; ： <選擇性 \_ url> 指定應將輸入檔案名視為原則中繼資料。 允許多個 wsp 輸入，並處理所有指定的原則檔案。 選擇性 url 會指定從中抓取 \_ 中繼資料的位置。 如果未 \_ 指定選擇性的 url，Wsutil 會在內部產生唯一的 url。 如果指定了/nopolicy 旗標，則會忽略原則檔。 另請參閱 [原則支援](policy-support.md)。
-   /nopolicy 停用原則處理。
-   /out： &lt; dirname &gt; 指定輸出檔案的目錄名稱
-   /noclient 不會產生用戶端存根。
-   /noservice 不會產生服務端存根。
-   /prefix： &lt; 字串 &gt; 在指定的字串前面加上所有產生的識別碼。
-   /fullname 在產生的識別碼前面加上正規化的檔案名。 依預設，只會使用 "name" 屬性中指定的名稱來產生相關描述的識別碼。
-   /string： <WS \_ 字串>\|<WCHAR \*> 根據預設，wsutil 會產生 \* xsd： string 類型的 WCHAR。 應用程式可以使用此旗標來覆寫該行為，並 \_ 改為產生 xsd： type 的 WS 字串。
-   /help 顯示說明訊息
-   /? 與/help 相同
-   /W： x 錯誤處理選項。 可能是 W:0-W： 4 \| WX
-   /nologo 不會產生主控台輸出的編譯器特定資訊。
-   /nostamp 不會產生所產生檔案的編譯器特定資訊。

根據預設，編譯器會為 WSDL 檔案或從中繼資料交換傳回的 WSDL 產生下列檔案：

-   用戶端 proxy ( {inputfilename} .c) 
-   服務 Stub ( {inputfilename} .c) 
-   標頭檔 ( {inputfilename} .h) 

    所產生檔案名的根目錄是輸入檔名稱。 保留原始輸入副檔名，以防止產生之檔案的檔案名衝突。 依預設，會在相同的檔案中產生用戶端和服務存根，並在 proxy 程式碼之後產生服務 stub 程式碼。

    根據預設，編譯器會針對從中繼資料交換傳回的架構，為 XSD 檔案產生下列檔案：

-   序列化描述 ( {inputfilename} .c) 
-   標頭檔 ( {inputfilename} .h) 

    檔案名的根目錄是服務名稱。

Wsutil.exe 會在所有產生的檔案開頭產生「戳記」區段，指出編譯器選項、工具版本、適用的命令列選項等。您可以使用/nostamp 選項來關閉此區段，以避免在比較產生的檔案時產生干擾。

Wsutil 不支援下載中繼資料

Wsutil 編譯器只適用于本機中繼資料檔案。 此工具不支援從執行中的 web 服務下載中繼資料。 開發人員可以使用其他支援的 webservice 工具（例如 svcutil），將中繼資料下載至本機電腦、檢查儲存的檔案，並將這些檔案傳遞至 wsutil.exe 進行編譯。

多個輸入/輸出檔案支援

WSDL 和 XML 架構可讓您從其他位置/檔案中指定的其他命名空間包含/匯入定義。 Wsutil 支援多個架構/wsdl/原則輸入，並為每個輸入檔產生一組存根/標頭。 Wsutil 不會遵循 include 和 import 語句。 相反地，應用程式應該將包含所有必要命名空間的檔案傳入 wsutil，如此一來，工具就可以在編譯期間解析所有相依性。

**WsUtil.exe/xsd： stockquote .xsd/wsdl： stockquote .wsdl/wsdl： stockquoteservice .wsdl**

wsutil 會產生三組輸出檔案：

-   stockquote .xsd stockquote .xsd
-   stockquote .wsdl stockquote。h
-   stockquoteservice .wsdl stockquoteservices .wsdl

輸出檔案格式

針對每個輸出檔案，wsutil 會在標頭檔中產生外部可用的定義。 除了 C 結構定義和存根函式原型之外，所有其他的 web 服務相關定義都會封裝在名為 with 正規化檔案名的全域結構中。

``` syntax
typedef struct _stockquote_wsdl {
  struct {
  ... // list of WS_STRUCT_DESCRIPTION for all global complex types.
  } globalTypes;
  struct {
  ... // WS_ELEMENT_DESCRIPTION for all global elements.
  } globalElements;
  struct {
  ...
  } messages;
  struct {
  ...
  } contracts;
} _stockquote_wsdl;

EXTERN_C _stockquote_wsdl stockquote_wsdl;
```

請注意，並非所有欄位都是針對全域結構產生的。 只有在輸入檔案中指定相關定義時，才會產生最上層欄位。 例如，xsd 檔案不會產生任何訊息、作業和合約欄位。

警告層級和錯誤層級

類似于 C 編譯器，WsUtil.exe 支援四個警告層級和一個錯誤層級：

-   WsUtil.exe 會產生無法復原失敗的錯誤，例如不正確 wsdl 檔案、不正確編譯器選項等。
-   WsUtil 會產生具有嚴重可復原問題的 W1 警告。 編譯器可以繼續進行，但使用者應該留意問題。 例如，在不會影響程式碼產生的 wsdl 中有不支援的屬性時，將會產生 W1 警告。
-   WsUtil 會產生較不嚴重問題的 W2 警告。 功能沒有遺失，但應用程式開發人員可能會想要知道。 與其他平臺可能不同的行為。
-   WsUtil 會產生與產生的程式碼不會影響極低的 W3 警告。 例如，當正規化字串與原始字串不同時，wsutil.exe 會產生 W3 警告。
-   W4 警告比較像是「資訊」警告，以及 WsUtil 在 WSDL 中忽略檔案屬性等情況下 W4 的問題。
-   WX 指出編譯器將警告視為錯誤。 例如，如果指定了/W： 1/WX，wsutil 就會針對所有 W1 警告產生錯誤。

/W： {N} 指定應產生的警告訊息層級。 /W：1表示應產生警告層級1警告，而且警告層級2和以下警告應遮罩，而不是由工具產生。

## <a name="fullname"></a>/fullname

此選項指出 WsUtil.exe 會產生識別碼的完整名稱，以避免潛在的名稱衝突。 例如，在範例中，我們有：

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:element name="SimpleStruct">
   <xs:complexType>
    <xs:sequence>
     <xs:element name="a" type="xs:int" />
     <xs:element name="b" type="xs:int" />
    </xs:sequence>
   </xs:complexType>
  </xs:element>
 </wsdl:types>
</wsdl:definitions>
```

根據預設，WsUtil.exe 會產生：

``` syntax
typedef struct SimpleStruct {
  int a;
  int b;
};
```

但是，如果指定了/fullname 命令列選項，WsUtil.exe 會改為產生下列結構定義：

``` syntax
typedef struct exmaple_xsd_SimpleStruct {
  int a;
  int b;
};
```

## <a name="globalization"></a>全球化

此工具是中性語言，可以當地語系化成不同的語言。 所有錯誤訊息/主控台輸出都可以當地語系化。 不過，命令列選項仍會保留英文。

## <a name="environment-variable"></a>環境變數

WsUtil.exe 不會使用任何環境變數。

## <a name="platform-independent"></a>平台獨立

WsUtil.exe 的輸出檔案與平臺無關。 存根未產生任何架構相依程式碼;任何特定的架構都將由 C 編譯器負責處理。 存根可以在我們支援的所有平臺中使用。

您可以在 [WSDL 支援](wsdl-support.md) 和 [架構支援](schema-support.md) 部分找到 wsutil.exe 輸出的描述。

 

 




