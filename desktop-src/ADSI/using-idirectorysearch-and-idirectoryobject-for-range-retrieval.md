---
title: 使用 >idirectorysearch 和 IDirectoryObject 進行範圍抓取
description: IDirectoryObject 或 >idirectorysearch 介面可以用來取得屬性值的範圍。 若要這樣做，請為查詢中要求的其中一個屬性指定屬性和範圍。
ms.assetid: 4d9d2a98-51d5-4326-b43e-a2ac3bc54a75
ms.tgt_platform: multiple
keywords:
- '>idirectorysearch ADSI，用來取得群組成員的範圍'
- IDirectoryObject ADSI，用來取得群組成員的範圍
- 使用 >idirectorysearch 和 IDirectoryObject 的範圍抓取 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506d061dd49c98bdb3b8cc731a28d0dc0ee5fe9a0df5816abf259ece17e456ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023056"
---
# <a name="using-idirectorysearch-and-idirectoryobject-for-range-retrieval"></a>使用 >idirectorysearch 和 IDirectoryObject 進行範圍抓取

[**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)或 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)介面可以用來取得屬性值的範圍。 若要這樣做，請為查詢中要求的其中一個屬性指定屬性和範圍。

## <a name="range-retrieval-with-idirectoryobject"></a>使用 IDirectoryObject 的範圍抓取

[**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)介面可用於範圍抓取，方法是在呼叫 [**IDirectoryObject：： GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes)方法時，指定屬性和 *pAttributesName* 陣列中其中一個屬性的範圍。


```C++
PADS_ATTR_INFO pAttrInfo;
DWORD dwRetrieved;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->GetObjectAttributes(pszAttrs, 2, &pAttrInfo, &dwRetrieved);
```



如需詳細資訊和示範如何使用 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 介面進行範圍抓取的程式碼範例，請參閱 [使用 IDirectoryObject 範圍的範例程式碼](example-code-for-ranging-with-idirectoryobject.md)。

## <a name="range-retrieval-with-idirectorysearch"></a>使用 >idirectorysearch 的範圍抓取

[**>Idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)介面可用於範圍抓取，方法是在呼叫 [**>idirectorysearch：： ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch)方法時，指定屬性和 *pAttributesName* 陣列中其中一個已抓取屬性的範圍。


```C++
ADS_SEARCH_HANDLE hSearch;
LPWSTR pszAttrs[2];
 
pszAttrs[0] = L"Name";
pszAttrs[1] = L"member;range=0-100";

hr = pdo->ExecuteSearch(L"(objectClass=user)", pszAttrs, 2, &hSearch);
```



使用 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 介面進行範圍抓取時，有一個問題必須特別解決。 當要求的範圍超過剩余值的數目時， [**>idirectorysearch：： GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) 會傳回 **\_ \_ \_ 未 \_ 設定的 E ADS 資料行**。 若要取得剩餘的值，必須使用範圍萬用字元 ' \* '。 例如，如果群組包含150成員，則可以使用範圍抓取來正常地取出成員值0-100。 如果接著要求範圍101-200， **>idirectorysearch：： GetColumn** 會傳回 **\_ \_ \_ 未 \_ 設定的 E ADS 資料行**。 使用 [**>idirectorysearch：： GetNextColumnName**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextcolumnname) 方法可以避免這個問題。 一般來說， **GetNextColumnName** 會傳回原始查詢字串。 不過，當要求的範圍超過剩余值的數目時， **GetNextColumnName** 會以範圍萬用字元 ' ' 取代高範圍的值，以傳回已修改的查詢字串版本 \* 。 在上述範例中，第一個查詢會使用 "member; range = 0-100" 的屬性字串來執行，且 **GetNextColumnName** 會傳回 "member; range = 0-100"。 在第二個查詢中，屬性字串會是 "member; range = 101-200"，但 **GetNextColumnName** 會傳回 "member; range = 101- \* "。 您可以藉由比較原始屬性字串與 **GetNextColumnName** 的結果來判斷這種情況。 如果字串不同，則應該使用範圍萬用字元再次要求最後一個值區塊。

如需詳細資訊和示範如何使用 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 介面進行範圍抓取的程式碼範例，請參閱 [使用 >idirectorysearch 範圍的範例程式碼](example-code-for-ranging-with-idirectorysearch.md)。

 

 




