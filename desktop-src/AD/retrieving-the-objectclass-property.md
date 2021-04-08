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
# <a name="retrieving-the-objectclass-attribute"></a>正在抓取 objectClass 屬性

**ObjectClass** 屬性包含物件為其實例的類別，以及衍生該類別的所有類別。 例如， **使用者** 類別繼承自 **top**、 **person** 和 **organizationalPerson**;因此， **objectClass** 屬性包含這些類別的名稱，以及使用者。 那麼，您要如何找出該物件是實例的類別呢？ **ObjectClass** 屬性是唯一具有多個值（具有已排序值）的屬性。 第一個值是類別階層的頂端，也就是最上層的類別，而最後一個值是最常衍生的類別，也就是物件為其實例的類別。

下列函式會採用包含 **objectClass** 屬性之資料行的指標，並傳回物件的具現化 **objectClass** 。


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



 

 




