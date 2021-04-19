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
# <a name="method-return-values"></a>方法傳回值

C + + 介面方法的傳回值一律為 **HRESULT** 類型;您可以檢查此值，以判斷成功或失敗。 使用 "output" 參數可在方法或屬性呼叫期間，將值指派給變數。 下列範例顯示 c + + 方法呼叫來列舉提供者。


```C++
UINT          ucEnumProvIndex = 0;
BSTR          bstrProvider = NULL;
HRESULT       hr;

// pEnroll is previously instantiated CEnroll interface pointer
hr = pEnroll->enumProviders(ucEnumProvIndex, 0, &bstrProvider);
```



在上述的程式碼片段中，成功或失敗會傳回給 "hr" 變數。 如果呼叫成功，hr 將設定為 S \_ OK，而且變數 bstrProvider 會包含列舉提供者的名稱。

取得屬性值的 c + + 呼叫如下所示。


```C++
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated CEnroll interface pointer

// get the storename
hr = pEnroll->get_CAStoreName( &bstrStoreName );

// (When done using bstrStoreName, free it by calling SysFreeString).
```



設定屬性值的 c + + 呼叫如下所示。


```C++
// bstrNewName previously set to a valid store name
hr = pEnroll->put_CAStoreName( bstrNewName );
```



 

 



