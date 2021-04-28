---
description: AJAX
ms.assetid: F9907D49-F9FE-406A-BF5F-17C61706ADC1
title: AJAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 575ab08530936ab083baa4bb3fcfa2956ffe3b2d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088756"
---
# <a name="ajax"></a>AJAX

Windows Internet Explorer 8 中的 AJAX 功能（例如 [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) 和 [跨檔訊息 (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) 具有可能與現有自訂屬性衝突的原生屬性。

Windows Internet Explorer 會公開某些 AJAX 功能的新屬性，例如 [跨檔訊息 (XDM) ](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf)，即使在相容性檢視中也是如此。 如果您將自訂屬性新增至事件物件，這些屬性可能會與這些新屬性（例如 **來源**）相衝突。

下列程式碼範例適用于舊版 Internet Explorer，但不在較新版本中，因為新功能使用 **source** 屬性。


```JScript
event.source = myObject;
```



下列程式碼範例會示範如何將這個物件變更為保持相容。


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用相容性檢視修正 Web 應用程式中的相容性問題](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



