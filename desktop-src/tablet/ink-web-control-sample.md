---
description: 這個範例示範如何建立啟用筆墨的控制項，以在網頁瀏覽器中使用。 此範例會採用原始的自動宣告表單範例，並將它轉換成放在網頁上的控制項。
ms.assetid: 7a9e304c-57ef-41a3-83be-2b2d31435da8
title: 筆墨 Web 控制項範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a2f305f1dcbb412325970510c6eaa5f09732bf10d870c961820ab8d8749eda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032196"
---
# <a name="ink-web-control-sample"></a>筆墨 Web 控制項範例

這個範例示範如何建立啟用筆墨的控制項，以在網頁瀏覽器中使用。 此範例會採用原始的 [自動宣告表單範例](auto-claims-form-sample.md) ，並將它轉換成放在網頁上的控制項。

如需在 Web 上使用筆墨的詳細資訊，請參閱 [網路上的筆跡](ink-on-the-web.md)。

## <a name="modifications-to-the-original-sample-project"></a>原始範例的修改 Project

此範例包含包含兩個專案和一個 HTML 檔案的方案。 第一個專案 AutoClaims 是 Microsoft Visual C \# 控制項程式庫專案， (使用者控制項) 。 此控制項的原始程式碼與 AutoClaims 範例的原始程式碼幾乎完全相同，但有兩項差異：

-   `AutoClaims`此範例中的類別繼承自[UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)類別，而不是[Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1)類別。

    ```C++
    public class AutoClaims : System.Windows.Forms.UserControl 
    ```

    

-   此範例中的 AutoClaims 類別具有新增的公用方法， `DisposeResources` 可處置用來收集筆墨的內部子控制項。 當使用控制項完成該頁面時，thewebpageon 會使用此方法來呼叫此方法。

## <a name="referencing-the-control-in-html"></a>以 HTML 參考控制項

解決方案包含 HTML 檔案 default.htm。 此檔案是瀏覽器導覽的頁面，以便載入控制項。 檔案包含 <object> 參考控制項的標記。 它也包含在頁面卸載時所呼叫的腳本，如中的 onload = "" 屬性是否存在。 `OnUnload()` <body> 的相片或視訊。 此函式 `DisposeResources` 會在控制項上呼叫方法，以確保所有資源在關機時都能正確地釋放。


```C++
<html>
    <script language="jscript">
        // Release any resources held by the AutoClaims control
        function OnUnload()
        {
            autoClaimsControl.DisposeResources();
        }
    </script>
    <head>
        <title>AutoClaims (Web Control)</title>
    </head>
    <body onunload="OnUnload()">
        <object 
          id="autoClaimsControl" 
          classid="AutoClaims.dll#AutoClaims.AutoClaims">
        </object>
    </body>
</html> 
```



請注意標記之 classid 屬性值的格式 <object> 。 它會將元件命名為，後面接著 \# 符號分隔符號，然後是包含控制項的命名空間，然後是控制項的類別名稱。

實際的使用者控制項可能包含用來保存或傳送在應用程式中收集之資料的其他方法。

## <a name="the-autoclaims_webcontrol-project"></a>AutoClaims \_ WebControl Project

AutoClaims \_ WebControl 專案是部署 Project，會建立安裝程式，以便在安裝時將虛擬根目錄（AutoClaims \_ WebControl）新增至 Web 服務器。 控制項和 HTML 檔案都會放在這個虛擬根目錄中。

> [!Note]  
> SDK 的預設安裝選項不會安裝已編譯的 web 範例。 您必須完成自訂安裝，然後選取 [預先編譯的 Web 範例] 子選項來進行安裝。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[自動宣告表單範例](auto-claims-form-sample.md)
</dt> <dt>

[Web 上的筆墨](ink-on-the-web.md)
</dt> </dl>

 

 
