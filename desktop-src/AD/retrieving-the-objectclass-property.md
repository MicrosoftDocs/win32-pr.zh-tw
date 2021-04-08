---
title: 正在抓取 objectClass 屬性
description: ObjectClass 屬性包含物件為其實例的類別，以及衍生該類別的所有類別。
ms.assetid: 6066d9c3-f97b-482a-88c7-0fde1dc2f4c4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f237efff1e13c7f3498a51f38588c9885fbab76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671243"
---
# <a name="retrieving-the-objectclass-attribute"></a><span data-ttu-id="0e916-103">正在抓取 objectClass 屬性</span><span class="sxs-lookup"><span data-stu-id="0e916-103">Retrieving the objectClass Attribute</span></span>

<span data-ttu-id="0e916-104">**ObjectClass** 屬性包含物件為其實例的類別，以及衍生該類別的所有類別。</span><span class="sxs-lookup"><span data-stu-id="0e916-104">The **objectClass** attribute contains the class of which the object is an instance, as well as all classes from which that class is derived.</span></span> <span data-ttu-id="0e916-105">例如， **使用者** 類別繼承自 **top**、 **person** 和 **organizationalPerson**;因此， **objectClass** 屬性包含這些類別的名稱，以及使用者。</span><span class="sxs-lookup"><span data-stu-id="0e916-105">For example, the **user** class inherits from **top**, **person**, and **organizationalPerson**; therefore, the **objectClass** attribute contains the names of those classes, as well as user.</span></span> <span data-ttu-id="0e916-106">那麼，您要如何找出該物件是實例的類別呢？</span><span class="sxs-lookup"><span data-stu-id="0e916-106">So, how do you find out what class the object is an instance of?</span></span> <span data-ttu-id="0e916-107">**ObjectClass** 屬性是唯一具有多個值（具有已排序值）的屬性。</span><span class="sxs-lookup"><span data-stu-id="0e916-107">The **objectClass** attribute is the only attribute with multiple values that has ordered values.</span></span> <span data-ttu-id="0e916-108">第一個值是類別階層的頂端，也就是最上層的類別，而最後一個值是最常衍生的類別，也就是物件為其實例的類別。</span><span class="sxs-lookup"><span data-stu-id="0e916-108">The first value is the top of the class hierarchy, which is the top class, and the last value is the most derived class, which is the class that the object is an instance of.</span></span>

<span data-ttu-id="0e916-109">下列函式會採用包含 **objectClass** 屬性之資料行的指標，並傳回物件的具現化 **objectClass** 。</span><span class="sxs-lookup"><span data-stu-id="0e916-109">The following function takes a pointer to a column containing an **objectClass** attribute and returns the instantiated **objectClass** of the object.</span></span>


```C++
HRESULT GetClass(ADS_SEARCH_COLUMN *pcol, LPOLESTR *ppClass)
{
  if (!pcol)
    return E_POINTER;
 
  HRESULT hr = E_FAIL;
  if (ppClass)
  {
    LPOLESTR szClass = new OLECHAR[MAX_PATH];
    wcscpy_s(szClass, L"");
    if ( _wcsicmp(pcol->pszAttrName,L"objectClass") == 0 )
    {
      for (DWORD x = 0; x< pcol->dwNumValues; x++)
      {
        wcscpy_s(szClass, pcol->pADsValues[x].CaseIgnoreString);
      }
    }
    if (0==wcscmp(L"", szClass))
    {
      hr = E_FAIL;
    }
    else
    {
      //Allocate memory for string.
      //Caller must free using CoTaskMemFree.
      *ppClass = (OLECHAR *)CoTaskMemAlloc (
                             sizeof(OLECHAR)*(wcslen(szClass)+1));
      if (*ppClass)
      {
        wcscpy_s(*ppClass, szClass);
        hr = S_OK;
      }
      else
      hr=E_FAIL;
    }
  }
  return hr;
}
```



 

 




