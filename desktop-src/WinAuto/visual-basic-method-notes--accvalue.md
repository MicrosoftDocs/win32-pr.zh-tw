---
title: Visual Basic 方法附注 accValue
description: 物件描述語言 (ODL) 檔 Oleacc. ODL，其中包含與 C/c + + 執行不同的資訊。 Oleacc 檔案包含設定函數屬性之版本的下列定義。
ms.assetid: 8c27d63a-ae69-4667-9b65-be743a00b49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ce93bc5d4ff2a2e01da55e30630fda42c573b7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021297"
---
# <a name="visual-basic-method-notes-accvalue"></a><span data-ttu-id="15298-104">Visual Basic 方法附注： accValue</span><span class="sxs-lookup"><span data-stu-id="15298-104">Visual Basic Method Notes: accValue</span></span>

<span data-ttu-id="15298-105">物件描述語言 (ODL) 檔 Oleacc. ODL，其中包含與 C/c + + 執行不同的資訊。</span><span class="sxs-lookup"><span data-stu-id="15298-105">The Object Description Language (ODL) file, Oleacc.odl, contains information that differs from the C/C++ implementation.</span></span> <span data-ttu-id="15298-106">Oleacc 檔案包含設定函數屬性之版本的下列定義。</span><span class="sxs-lookup"><span data-stu-id="15298-106">The file Oleacc.odl contains the following definition for the version that sets the property of the function.</span></span>


```C++
    [hidden, propput, id(DISPID_ACC_VALUE)]
    HRESULT accValue(
        [in, optional] VARIANT varChild,
        [in] BSTR szValue);
```



<span data-ttu-id="15298-107">雖然 *varChild* 參數在 ODL 檔和物件瀏覽器中列為選擇性，但在呼叫 [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue)的屬性設定版本時，您必須將它加入。</span><span class="sxs-lookup"><span data-stu-id="15298-107">Although the *varChild* parameter is listed as optional in the ODL file and the object browser, you must include it when calling the property-setting version of [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).</span></span>

 

 




