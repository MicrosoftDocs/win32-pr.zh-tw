---
description: C + + 介面方法的傳回值一律為 HRESULT 類型;您可以檢查此值，以判斷成功或失敗。
ms.assetid: f6478e72-0fe9-4c3b-b08a-f71c9c943910
title: 方法傳回值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3871cf00bd48c7fbe1432ec86b503fba7795592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972658"
---
# <a name="method-return-values"></a><span data-ttu-id="75af3-103">方法傳回值</span><span class="sxs-lookup"><span data-stu-id="75af3-103">Method Return Values</span></span>

<span data-ttu-id="75af3-104">C + + 介面方法的傳回值一律為 **HRESULT** 類型;您可以檢查此值，以判斷成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="75af3-104">The return value for C++ interface methods is always of type **HRESULT**; this value can be checked to determine success or failure.</span></span> <span data-ttu-id="75af3-105">使用 "output" 參數可在方法或屬性呼叫期間，將值指派給變數。</span><span class="sxs-lookup"><span data-stu-id="75af3-105">The use of "output" parameters allows values to be assigned to variables during the method or property call.</span></span> <span data-ttu-id="75af3-106">下列範例顯示 c + + 方法呼叫來列舉提供者。</span><span class="sxs-lookup"><span data-stu-id="75af3-106">The following example shows a C++ method call to enumerate providers.</span></span>


```C++
UINT          ucEnumProvIndex = 0;
BSTR          bstrProvider = NULL;
HRESULT       hr;

// pEnroll is previously instantiated CEnroll interface pointer
hr = pEnroll->enumProviders(ucEnumProvIndex, 0, &bstrProvider);
```



<span data-ttu-id="75af3-107">在上述的程式碼片段中，成功或失敗會傳回給 "hr" 變數。</span><span class="sxs-lookup"><span data-stu-id="75af3-107">In the preceding code fragment, success or failure is returned to the "hr" variable.</span></span> <span data-ttu-id="75af3-108">如果呼叫成功，hr 將設定為 S \_ OK，而且變數 bstrProvider 會包含列舉提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="75af3-108">If the call was successful, hr will be set to S\_OK and the variable bstrProvider will contain the name of the enumerated provider.</span></span>

<span data-ttu-id="75af3-109">取得屬性值的 c + + 呼叫如下所示。</span><span class="sxs-lookup"><span data-stu-id="75af3-109">A C++ call to retrieve a property value would be as follows.</span></span>


```C++
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated CEnroll interface pointer

// get the storename
hr = pEnroll->get_CAStoreName( &bstrStoreName );

// (When done using bstrStoreName, free it by calling SysFreeString).
```



<span data-ttu-id="75af3-110">設定屬性值的 c + + 呼叫如下所示。</span><span class="sxs-lookup"><span data-stu-id="75af3-110">A C++ call to set a property value would be as follows.</span></span>


```C++
// bstrNewName previously set to a valid store name
hr = pEnroll->put_CAStoreName( bstrNewName );
```



 

 



