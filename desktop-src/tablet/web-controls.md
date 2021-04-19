---
description: 建立啟用筆墨之 Web 應用程式的其中一種方式，是將 Windows Forms 控制項放在 awebpagewithin Microsoft Internet Explorer 內。
ms.assetid: a4fcd692-cd4a-4d2a-bfad-198010e27c6f
title: Web 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b28fa2a3293b6b780412ddbc755634c745b44e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986334"
---
# <a name="web-controls"></a>Web 控制項

建立啟用筆墨之 Web 應用程式的其中一種方式，是將 Windows Forms 控制項放在 awebpagewithin Microsoft Internet Explorer 內。 在 [Internet Explorer 中使用 Windows Forms 控制項](https://windowsclient.net/articles/iesourcing.aspx)可以找到這項技術的良好教學課程。 本教學課程中的基本步驟如下：

1.  建立繼承自 [**UserControl**](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)的控制項。
2.  使用參考該 UserControl 的物件標記建立 HTML 網頁。
3.  建立虛擬目錄並設定許可權。
4.  將 HTML 網頁的 URL 載入瀏覽器。

這項技術可以套用至啟用筆墨的控制項，就像任何其他 Windows Forms [**控制項**](/dotnet/api/system.windows.forms.control?view=netcore-3.1)一樣。 事實上，這項技術可以搭配 Microsoft .NET Framework 中的任何類別使用。 Microsoft Windows XP Tablet PC Edition 軟體發展工具組所提供的範例 (SDK) 在 Ink Web 範例一節中包含自動宣告範例的 Web 控制項版本。 此範例會採用原始的 [自動宣告表單範例](auto-claims-form-sample.md) ，並將它轉換成放在網頁上的控制項。 如需啟用此範例之 Web 的詳細資訊，請參閱 [筆墨 Web 控制項範例](ink-web-control-sample.md)。

> [!Note]  
> 當您部署透過 Web 使用 .NET 建立的應用程式時，該應用程式可能會受到 .NET 的安全性模型影響。 如需安全性如何搭配啟用筆墨之 Web 應用程式的詳細資訊，請參閱 [安全性與信任](security-and-trust.md)。

 

 

 
