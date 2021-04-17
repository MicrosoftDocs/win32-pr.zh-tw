---
description: 傳回 HRESULT。 在此 HRESULT 中，S 的值 \_ 表示已成功執行方法。
ms.assetid: 6722a74a-1ec1-4c71-84c6-fb103aca149f
title: C + + 中的憑證註冊控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76525f26f318178f122cc0feee6221bbd948bba0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511216"
---
# <a name="certificate-enrollment-control-properties-in-c"></a><span data-ttu-id="94662-104">C + + 中的憑證註冊控制項屬性</span><span class="sxs-lookup"><span data-stu-id="94662-104">Certificate Enrollment Control Properties in C++</span></span>

<span data-ttu-id="94662-105">當您在 c + + 中設定或取出憑證註冊控制項屬性時，方法呼叫會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="94662-105">When you set or retrieve a Certificate Enrollment Control property in C++, the method call returns an **HRESULT**.</span></span> <span data-ttu-id="94662-106">在此 **HRESULT** 中，S 的值 \_ 表示已成功執行方法。</span><span class="sxs-lookup"><span data-stu-id="94662-106">In this an **HRESULT**, a value of S\_OK indicates that the method was successfully executed.</span></span>

<span data-ttu-id="94662-107">以 c + + 撰寫的程式可透過下列形式的方法呼叫來抓取憑證註冊控制項屬性。</span><span class="sxs-lookup"><span data-stu-id="94662-107">Programs written in C++ can retrieve the Certificate Enrollment Control properties by method calls in the following form.</span></span>


```C++
#include <windows.h>

HRESULT get_propertyName( datatype * pPropValue);
```



<span data-ttu-id="94662-108">其中 *propertyName* 會指定所要存取的屬性名稱，而 *pPropValue* 則是適當資料類型之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="94662-108">Where *propertyName* specifies the name of the property being accessed, and *pPropValue* is a pointer to a variable of the appropriate data type.</span></span> <span data-ttu-id="94662-109">成功完成此方法呼叫之後， *pPropValue* 會指向包含 *propertyName* 屬性值的變數。</span><span class="sxs-lookup"><span data-stu-id="94662-109">After successful completion of this method call, *pPropValue* will point to the variable that contains the value of the *propertyName* property.</span></span>

<span data-ttu-id="94662-110">例如，若要取出 **RootStoreType** 屬性的值，請使用下列程式碼。</span><span class="sxs-lookup"><span data-stu-id="94662-110">For example, to retrieve the value for the **RootStoreType** property, you use the following code.</span></span>


```C++
// Get the store type.
// hr is an HRESULT.
// bstrStoreType is a BSTR variable.
hr = pEnroll->get_RootStoreType( &bstrStoreType );
```



<span data-ttu-id="94662-111">以 c + + 撰寫的程式可以藉由呼叫下列格式的方法來設定憑證註冊控制項屬性。</span><span class="sxs-lookup"><span data-stu-id="94662-111">Programs written in C++ can set the Certificate Enrollment Control properties by calling methods in the following form.</span></span>


```C++
#include <windows.h>

HRESULT put_propertyName( datatype PropValue);
```



<span data-ttu-id="94662-112">其中 *propertyName* 指定要存取的屬性名稱，而 *PropValue* 是適當資料類型的值。</span><span class="sxs-lookup"><span data-stu-id="94662-112">Where *propertyName* specifies the name of the property being accessed, and *PropValue* is a value of the appropriate data type.</span></span> <span data-ttu-id="94662-113">成功完成此方法呼叫之後， *propertyName* 屬性的新值將會是 *PropValue*。</span><span class="sxs-lookup"><span data-stu-id="94662-113">After successful completion of this method call, the new value of the *propertyName* property will be *PropValue*.</span></span>

<span data-ttu-id="94662-114">例如，若要設定 **RootStoreType** 的屬性值，可以使用下列程式碼。</span><span class="sxs-lookup"><span data-stu-id="94662-114">For example, to set the property value for the **RootStoreType**, the following code could be used.</span></span>


```C++
// Set the store type.
// bstrNewType previously set to a valid store type
hr = pEnroll->put_RootStoreType( bstrNewType );
```



 

 



