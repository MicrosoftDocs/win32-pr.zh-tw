---
title: Visual Basic 方法附注 accName
description: 物件描述語言 (ODL) 檔 Oleacc. ODL，其中包含與 C/c + + 執行不同的資訊。
ms.assetid: f7960acd-cb1a-4c34-a392-0243155a100f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c404c093fc3b92b4d653b0b1258c62918af8e25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840132"
---
# <a name="visual-basic-method-notes-accname"></a><span data-ttu-id="ee3e0-103">Visual Basic 方法附注： accName</span><span class="sxs-lookup"><span data-stu-id="ee3e0-103">Visual Basic Method Notes: accName</span></span>

<span data-ttu-id="ee3e0-104">物件描述語言 (ODL) 檔 Oleacc. ODL，其中包含與 C/c + + 執行不同的資訊。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-104">The Object Description Language (ODL) file, Oleacc.odl, contains information that differs from the C/C++ implementation.</span></span> <span data-ttu-id="ee3e0-105">Oleacc 檔案包含設定函數屬性之版本的下列定義：</span><span class="sxs-lookup"><span data-stu-id="ee3e0-105">The file Oleacc.odl contains the following definition for the version that sets the property of the function:</span></span>


```C++
    [hidden, propput, id(DISPID_ACC_NAME)]
    HRESULT accName(
        [in, optional] VARIANT varChild,
        [in] BSTR szName);
```



<span data-ttu-id="ee3e0-106">雖然 *varChild* 參數在 ODL 檔和物件瀏覽器中列為選擇性，但在呼叫 [**accName**](https://www.bing.com/search?q=**accName**)的屬性設定版本時，您必須將它加入。</span><span class="sxs-lookup"><span data-stu-id="ee3e0-106">Although the *varChild* parameter is listed as optional in the ODL file and the object browser, you must include it when calling the property-setting version of [**accName**](https://www.bing.com/search?q=**accName**).</span></span>

 

 




