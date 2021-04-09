---
description: .
ms.assetid: F9907D49-F9FE-406A-BF5F-17C61706ADC1
title: AJAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e140604846570b523910bb8ab815b185f26fa4dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945300"
---
# <a name="ajax"></a><span data-ttu-id="097ed-103">AJAX</span><span class="sxs-lookup"><span data-stu-id="097ed-103">AJAX</span></span>

<span data-ttu-id="097ed-104">Windows Internet Explorer 8 中的 AJAX 功能（例如 [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) 和 [跨檔訊息 (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) 具有可能與現有自訂屬性衝突的原生屬性。</span><span class="sxs-lookup"><span data-stu-id="097ed-104">AJAX features in Windows Internet Explorer 8 like [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) and [Cross-Document Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) have native properties that might conflict with existing custom properties.</span></span>

<span data-ttu-id="097ed-105">Windows Internet Explorer 會公開某些 AJAX 功能的新屬性，例如 [跨檔訊息 (XDM) ](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf)，即使在相容性檢視中也是如此。</span><span class="sxs-lookup"><span data-stu-id="097ed-105">Windows Internet Explorer exposes new properties for certain AJAX features, such as [Cross-Document Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), even in Compatibility View.</span></span> <span data-ttu-id="097ed-106">如果您將自訂屬性新增至事件物件，這些屬性可能會與這些新屬性（例如 **來源**）相衝突。</span><span class="sxs-lookup"><span data-stu-id="097ed-106">If you add custom properties to the event object, they might conflict with these new properties, such as **source**.</span></span>

<span data-ttu-id="097ed-107">下列程式碼範例適用于舊版 Internet Explorer，但不在較新版本中，因為新功能使用 **source** 屬性。</span><span class="sxs-lookup"><span data-stu-id="097ed-107">The following code example works in older versions of Internet Explorer but not in newer versions because new features use the **source** property.</span></span>


```JScript
event.source = myObject;
```



<span data-ttu-id="097ed-108">下列程式碼範例會示範如何將這個物件變更為保持相容。</span><span class="sxs-lookup"><span data-stu-id="097ed-108">The following code example shows how you can change this object to remain compatible.</span></span>


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a><span data-ttu-id="097ed-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="097ed-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="097ed-110">使用相容性檢視修正 Web 應用程式中的相容性問題</span><span class="sxs-lookup"><span data-stu-id="097ed-110">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



