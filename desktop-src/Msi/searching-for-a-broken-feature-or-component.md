---
description: 安裝程式可以自動重新安裝損毀的元件，藉此提升應用程式的復原能力。
ms.assetid: aa565e34-f89d-4d26-945d-67b439586523
title: 搜尋中斷的功能或元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8398d084a543ee4c9491242faa287c60d83a5f7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193305"
---
# <a name="searching-for-a-broken-feature-or-component"></a><span data-ttu-id="4dfc1-103">搜尋中斷的功能或元件</span><span class="sxs-lookup"><span data-stu-id="4dfc1-103">Searching for a Broken Feature or Component</span></span>

<span data-ttu-id="4dfc1-104">安裝程式可以自動重新安裝損毀的元件，藉此提升應用程式的 [復原能力](resiliency.md) 。</span><span class="sxs-lookup"><span data-stu-id="4dfc1-104">The installer can increase application [resiliency](resiliency.md) by automatically reinstalling damaged components.</span></span> <span data-ttu-id="4dfc1-105">具體而言，安裝程式會在發現 [元件資料表](component-table.md) 的 KeyPath 資料行中指定的檔案或登錄機碼遺失時，重新安裝元件或功能。</span><span class="sxs-lookup"><span data-stu-id="4dfc1-105">Specifically, the installer reinstalls a component or feature if it finds that the file or registry key specified in the KeyPath column of the [Component table](component-table.md) is missing.</span></span>

<span data-ttu-id="4dfc1-106">如果來源中的功能元件 KeyPath 損毀，或在資料庫中撰寫 KeyPath 的方式發生錯誤，安裝程式可能會嘗試開啟安裝套件，並在每次啟用功能的快捷方式時重新安裝該功能。</span><span class="sxs-lookup"><span data-stu-id="4dfc1-106">If the KeyPath of a feature's component is damaged in the source, or if there is an error in how the KeyPath is authored in the database, the installer may attempt to open an installation package and reinstall the feature each time the feature's shortcut is activated.</span></span>

<span data-ttu-id="4dfc1-107">若要判斷重複嘗試重新安裝功能或應用程式的原因，請檢查事件記錄檔中的兩個專案，如下所示。</span><span class="sxs-lookup"><span data-stu-id="4dfc1-107">To determine the cause of repeated attempts to reinstall a feature or application, check the Event Log for two entries such as the following.</span></span>

``` syntax
Detection of product 'MyProduct', feature 'MyFeature' failed during
 request for component 'MyComponent'
Detection of product 'MyProduct', feature 'MyFeature', component
 'MyComponent' failed
```

<span data-ttu-id="4dfc1-108">第一個訊息指出正在安裝產品套件中的哪個元件。</span><span class="sxs-lookup"><span data-stu-id="4dfc1-108">The first message states which component in the product's package was being installed.</span></span> <span data-ttu-id="4dfc1-109">這是 \_ [快捷方式資料表](shortcut-table.md)之 [元件] 資料行中所參考的元件。</span><span class="sxs-lookup"><span data-stu-id="4dfc1-109">This is the component referenced in the Component\_ column of the [Shortcut table](shortcut-table.md).</span></span>

<span data-ttu-id="4dfc1-110">第二個訊息指出哪個元件偵測失敗。</span><span class="sxs-lookup"><span data-stu-id="4dfc1-110">The second message states which component is failing detection.</span></span> <span data-ttu-id="4dfc1-111">這是有遺失或損毀的 KeyPath 會觸發重新安裝的元件。</span><span class="sxs-lookup"><span data-stu-id="4dfc1-111">This is the component with the missing or damaged KeyPath that's triggering the reinstall.</span></span>

 

 



