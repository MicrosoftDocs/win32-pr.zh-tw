---
description: 此範例示範如何使用無觸控部署，透過 Web 部署受管理的 Tablet PC 應用程式。
ms.assetid: d226bd67-e20d-431b-b0c3-9361b00a9340
title: No-Touch 部署 Web 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0742deef8ea9b418fba6de4724975ee27693f8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104514289"
---
# <a name="no-touch-deployment-web-sample"></a>No-Touch 部署 Web 範例

此範例示範如何使用無觸控部署，透過 Web 部署受管理的 Tablet PC 應用程式。 您應該熟悉 .NET Framework 中的 [無觸控部署](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp)所討論的概念。 您的電腦必須安裝 Microsoft Internet Information Services (IIS) ，才能執行此範例。

## <a name="overview"></a>概觀

使用無觸控部署，Tablet PCWindows Forms 應用程式-使用 Microsoft .NET Framework 和 Microsoft Windows XP Tablet PC Edition 開發工具組1.7 中的類別所建立的桌面應用程式，可以直接在使用者的電腦上下載、安裝及執行，而不需要變更登錄或共用的系統元件。

此範例會採用 [自動宣告表單範例](auto-claims-form-sample.md)、AutoClaims 的原始專案，並提供安裝程式專案 AutoClaims \_ NoTouchWeb。 編譯並執行之後，安裝程式專案會建立新的虛擬根目錄，也稱為 AutoClaims \_ NoTouchWeb。 安裝程式會複製 default.htm 的檔案，其中包含 AutoClaims.exe 元件的連結。 若要啟動豐富型用戶端應用程式，請流覽至 Microsoft Internet Explorer 的虛擬根目錄，然後按一下 [default.htm] 頁面中的連結。

> [!Note]  
> 例如，您必須透過 IIS (流覽至虛擬根目錄， https://localhost/AutoClaims\_NoTouchWeb/default.htm) 而不是直接透過檔案系統，以便讓應用程式在 Internet Explorer 應用程式域中運作。

 


```C++
<html>
    <head>
        <title>AutoClaims (No Touch Web)</title>
      </head>
      <body>
          <a href="AutoClaims.exe">Launch AutoClaims Sample</a>
      </body>
</html>
```



## <a name="no-touch-deployment-requirements"></a>No-Touch 部署需求

所有相依元件都必須位於網站之虛擬目錄的元件搜尋路徑或根目錄中。 AutoClaims \_ NoTouchWeb 部署專案會將元件和參考頁面（default.htm）安裝至相同的虛擬根目錄 (AutoClaims \_ NoTouchWeb) 。

> [!Note]  
> SDK 的預設安裝選項不會安裝已編譯的 web 範例。 您必須完成自訂安裝，然後選取 [預先編譯的 Web 範例] 子選項來進行安裝。

 

如需在 Web 上使用筆墨的詳細資訊，請參閱 [網路上的筆跡](ink-on-the-web.md)。

 

 