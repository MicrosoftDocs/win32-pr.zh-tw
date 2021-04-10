---
title: 使用 GetInfoEx 的優化
description: 用來將特定屬性值從基礎目錄服務載入至本機快取。
ms.assetid: e6111957-22cb-4473-9814-5bcbc79583b2
ms.tgt_platform: multiple
keywords:
- 使用 GetInfoEx ADSI 優化
- 使用 IADs GetInfoEx GetInfoEx ADSI、優化
- ADSI ADSI，使用，使用 IADs GetInfoEx 方法優化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b522093fff00700cf35b864edde2a6ae7f8f9922
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316453"
---
# <a name="optimization-using-getinfoex"></a><span data-ttu-id="a3b55-106">使用 GetInfoEx 的優化</span><span class="sxs-lookup"><span data-stu-id="a3b55-106">Optimization Using GetInfoEx</span></span>

<span data-ttu-id="a3b55-107">[**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex)方法是用來將特定的屬性值從基礎目錄服務載入至本機快取。</span><span class="sxs-lookup"><span data-stu-id="a3b55-107">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method is used to load specific attribute values into the local cache from the underlying directory service.</span></span> <span data-ttu-id="a3b55-108">這個方法只會將指定的屬性值載入至本機快取。</span><span class="sxs-lookup"><span data-stu-id="a3b55-108">This method only loads the specified attribute values into the local cache.</span></span> <span data-ttu-id="a3b55-109">[**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo)方法是用來將所有屬性值載入至本機快取。</span><span class="sxs-lookup"><span data-stu-id="a3b55-109">The [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method is used to load all attribute values into the local cache.</span></span>

<span data-ttu-id="a3b55-110">[**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex)方法會從基礎目錄存放區取得 Active Directory 物件屬性的特定目前值，並重新整理快取的值。</span><span class="sxs-lookup"><span data-stu-id="a3b55-110">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method gets specific current values for the properties of an Active Directory object from the underlying directory store, refreshing the cached values.</span></span>

<span data-ttu-id="a3b55-111">但是，如果值已存在於屬性快取中，則呼叫 [**IADs**](/windows/desktop/api/Iads/nf-iads-iads-get) 或 [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) 方法時，若未先呼叫 [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) ，該屬性將會抓取快取的值，而不是基礎目錄的最新值。</span><span class="sxs-lookup"><span data-stu-id="a3b55-111">If a value already exists in the property cache, however, calling the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) or [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method without first calling [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) for that attribute will retrieve the cached value rather than the most current value from the underlying directory.</span></span> <span data-ttu-id="a3b55-112">這可能會在本機快取已修改的情況下覆寫已更新的屬性值，但值尚未認可至基礎目錄服務，而呼叫 [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 方法。</span><span class="sxs-lookup"><span data-stu-id="a3b55-112">This can cause updated attribute values to be overwritten if the local cache has been modified, but the values have not been committed to the underlying directory service with a call to the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span> <span data-ttu-id="a3b55-113">避免快取問題的建議方法是，在呼叫 [**IADs**](/windows/desktop/api/Iads/nf-iads-iads-getinfo)之前呼叫 **IADs SetInfo** ，一律認可屬性值變更。</span><span class="sxs-lookup"><span data-stu-id="a3b55-113">The suggested method for avoiding caching problems is to always commit attribute value changes by calling **IADs.SetInfo** before calling [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).</span></span>


```VB
Dim usr As IADs
Dim PropArray As Variant

On Error GoTo Cleanup

' Bind to a specific user object.
Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' The code example assumes that the property description has a single value in the directory.
' Be aware that this will implicitly call GetInfo because, at this point, GetInfo
' has not yet been called (implicitly or explicitly) on the usr object.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Change two of the attribute values in the local cache.
usr.Put "cn", "Jeff Smith"
usr.Put "title", "Vice President"
usr.Put "department", "Head Office"
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Initialize the array of properties to pass to GetInfoEx.
PropArray = Array("department", "title")
 
' Get the specified attribute values.
usr.GetInfoEx PropArray, 0

' The specific attributes values were overwritten, but the attribute
' value not retrieved has not changed.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="retrieving-active-directory-constructed-attributes"></a><span data-ttu-id="a3b55-114">抓取 Active Directory 的結構化屬性</span><span class="sxs-lookup"><span data-stu-id="a3b55-114">Retrieving Active Directory Constructed Attributes</span></span>

<span data-ttu-id="a3b55-115">在 Active Directory 中，當呼叫 [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) 方法 (IADs 時，會抓取和快取大部分的結構化屬性。如果 [**快取**](/windows/desktop/api/Iads/nf-iads-iads-get) 是空的) ，則會執行隱含 **IADs. GetInfo** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="a3b55-115">In Active Directory, most of the constructed attributes are retrieved and cached when the [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method is called ([**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) performs an implicit **IADs.GetInfo** call if the cache is empty).</span></span> <span data-ttu-id="a3b55-116">但是，某些已建立的屬性不會自動取得和快取，因此，需要明確呼叫 [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) 方法才能取得它們。</span><span class="sxs-lookup"><span data-stu-id="a3b55-116">Some constructed attributes, however, are not automatically retrieved and cached and, therefore, require that the [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method be called explicitly to retrieve them.</span></span> <span data-ttu-id="a3b55-117">例如，在 Active Directory 中，呼叫 **IADs. GetInfo** 方法並 IADs 時，不會抓取 [**CanonicalName**](/windows/desktop/ADSchema/a-canonicalname)屬性。 **Get** 會傳回 **\_ \_ \_ 未 \_ 找到的 E ADS 屬性**。</span><span class="sxs-lookup"><span data-stu-id="a3b55-117">For example, in Active Directory, the [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) attribute is not retrieved when the **IADs.GetInfo** method is called and **IADs.Get** will return **E\_ADS\_PROPERTY\_NOT\_FOUND**.</span></span> <span data-ttu-id="a3b55-118">您必須呼叫 **IADs GetInfoEx** 方法，才能取出 **canonicalName** 屬性。</span><span class="sxs-lookup"><span data-stu-id="a3b55-118">The **IADs.GetInfoEx** method must be called to retrieve the **canonicalName** attribute.</span></span> <span data-ttu-id="a3b55-119">這些相同的結構化屬性也不會使用 [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) 介面來列舉屬性。</span><span class="sxs-lookup"><span data-stu-id="a3b55-119">These same constructed attributes will also not be retrieved using the [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface to enumerate the attributes.</span></span>

<span data-ttu-id="a3b55-120">如需詳細資訊和示範如何取出所有屬性值的程式碼範例，請參閱 [讀取已建立之屬性的範例程式碼](example-code-for-reading-a-constructed-attribute.md)。</span><span class="sxs-lookup"><span data-stu-id="a3b55-120">For more information and a code example that shows how to retrieve all attribute values, see [Example Code for Reading a Constructed Attribute](example-code-for-reading-a-constructed-attribute.md).</span></span>

 

 