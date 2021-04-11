---
title: 使用 IDirectoryObject 介面存取屬性
description: IDirectoryObject 介面提供以 C 和 c + + 撰寫的用戶端應用程式，可直接存取目錄服務物件。
ms.assetid: 006be48e-222f-4f77-ac91-58830f2b7363
ms.tgt_platform: multiple
keywords:
- 使用 IDirectoryObject 介面 ADSI 存取屬性
- IDirectoryObject ADSI，存取屬性
- ADSI ADSI，使用 IDirectoryObject 介面存取屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1da62b6a5cf7e1389276475c46faac6455672790
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931867"
---
# <a name="accessing-attributes-with-the-idirectoryobject-interface"></a><span data-ttu-id="134e8-106">使用 IDirectoryObject 介面存取屬性</span><span class="sxs-lookup"><span data-stu-id="134e8-106">Accessing Attributes With the IDirectoryObject Interface</span></span>

<span data-ttu-id="134e8-107">[**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)介面提供以 C 和 c + + 撰寫的用戶端應用程式，可直接存取目錄服務物件。</span><span class="sxs-lookup"><span data-stu-id="134e8-107">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface provides a client application written in C and C++ with direct access to directory service objects.</span></span> <span data-ttu-id="134e8-108">介面會透過直接網路通訊協定（而不是透過 ADSI 屬性快取）來啟用存取。</span><span class="sxs-lookup"><span data-stu-id="134e8-108">The interface enables access by means of a direct network protocol, rather than through the ADSI attribute cache.</span></span> <span data-ttu-id="134e8-109">為了取代 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面所支援的屬性， **IDirectoryObject** 提供的方法可支援物件之維護方法的重要子集，並可讓您存取其屬性。</span><span class="sxs-lookup"><span data-stu-id="134e8-109">In place of the properties supported by the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface, **IDirectoryObject** provides methods that support a critical subset of an object's maintenance methods and provide access to its attributes.</span></span> <span data-ttu-id="134e8-110">透過 **IDirectoryObject**，用戶端可以使用一個方法呼叫來取得或設定任何數目的物件屬性。</span><span class="sxs-lookup"><span data-stu-id="134e8-110">With **IDirectoryObject**, a client can get or set any number of object attributes with one method call.</span></span> <span data-ttu-id="134e8-111">不同于已批次處理的對應 Automation 方法，會在呼叫時執行 **IDirectoryObject** 。</span><span class="sxs-lookup"><span data-stu-id="134e8-111">Unlike the corresponding Automation methods, which are batched, those of **IDirectoryObject** are executed when called.</span></span> <span data-ttu-id="134e8-112">因為此介面上的方法不需要建立 Automation 目錄物件的實例，所以效能的額外負荷很小。</span><span class="sxs-lookup"><span data-stu-id="134e8-112">Because methods on this interface do not require creating an instance of an Automation directory object, the performance overhead is small.</span></span>

<span data-ttu-id="134e8-113">以 C 和 c + + 等語言撰寫的用戶端應該使用 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 介面的方法，將效能優化，並利用原生目錄服務介面。</span><span class="sxs-lookup"><span data-stu-id="134e8-113">Clients written in languages such as C and C++ should use the methods of the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface to optimize performance and take advantage of native directory service interfaces.</span></span> <span data-ttu-id="134e8-114">Automation 用戶端無法使用 **IDirectoryObject**。</span><span class="sxs-lookup"><span data-stu-id="134e8-114">Automation clients cannot use **IDirectoryObject**.</span></span> <span data-ttu-id="134e8-115">相反地，它們應該使用 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面。</span><span class="sxs-lookup"><span data-stu-id="134e8-115">Instead, they should use the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>

<span data-ttu-id="134e8-116">[**IDirectoryObject：： GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes)方法會取出具有單一和多個值的屬性。</span><span class="sxs-lookup"><span data-stu-id="134e8-116">The [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method retrieves attributes with both single and multiple values.</span></span> <span data-ttu-id="134e8-117">這個方法會採用要求的屬性清單，並傳回 [**ADS \_ ATTR \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) 結構。</span><span class="sxs-lookup"><span data-stu-id="134e8-117">This method takes a list of requested attributes and returns an [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure.</span></span> <span data-ttu-id="134e8-118">ADSI 會配置此結構;當呼叫端不再需要使用 [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) 函式時，呼叫端必須釋放這個記憶體。</span><span class="sxs-lookup"><span data-stu-id="134e8-118">ADSI allocates this structure; the caller must free this memory when it is no longer required using the [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) function.</span></span>

<span data-ttu-id="134e8-119">傳回屬性值的順序不一定與要求屬性的順序相同。</span><span class="sxs-lookup"><span data-stu-id="134e8-119">The order of returned attribute values is not necessarily the same as the order in which the attributes were requested.</span></span> <span data-ttu-id="134e8-120">因此，必須比較從 ADSI 傳回的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="134e8-120">Therefore, it is necessary to compare the attribute names returned from ADSI.</span></span>

> [!Note]  
> <span data-ttu-id="134e8-121">[**ADS \_ ATTR \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)結構不會傳回所有要求的屬性。</span><span class="sxs-lookup"><span data-stu-id="134e8-121">The [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure does not return all of the attributes requested.</span></span> <span data-ttu-id="134e8-122">只有包含值的屬性才是傳回結構的一部分。</span><span class="sxs-lookup"><span data-stu-id="134e8-122">Only those attributes that contain values are part of the returned structure.</span></span>

 

<span data-ttu-id="134e8-123">傳回的屬性數目取決於傳遞給 [**IDirectoryObject：： GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes)方法的 *dwNumberAttributes* 參數。</span><span class="sxs-lookup"><span data-stu-id="134e8-123">The number of attributes returned is determined by the *dwNumberAttributes* parameter passed to the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method.</span></span>

<span data-ttu-id="134e8-124">下列程式碼範例會系結至物件，並使用 [**IDirectoryObject：： GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) 方法來取得物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="134e8-124">The following code example binds to an object and uses the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method to retrieve attributes of the object.</span></span>


```C++
HRESULT hr;
IDirectoryObject *pDirObject;

CoInitialize(NULL);

hr = ADsGetObject(
       L"LDAP://CN=Jeff Smith,OU=Users,DC=Fabrikam,DC=com",
       IID_IDirectoryObject, 
       (void**)&pDirObject);

if(SUCCEEDED(hr))
{
  ADS_ATTR_INFO *pAttrInfo = NULL;
  LPWSTR pAttrNames[] = {L"cn", L"title", L"otherTelephone"};
  DWORD dwNumAttr = sizeof(pAttrNames)/sizeof(LPWSTR);
  DWORD dwReturn;

  //////////////////////////////////////////////////
  // Get attribute values requested.
  // Be aware that the order is not necessarily the 
  // same as requested using pAttrNames.
  //////////////////////////////////////////////////
  hr = pDirObject->GetObjectAttributes(pAttrNames, 
                                       dwNumAttr, 
                                       &pAttrInfo, 
                                       &dwReturn);
     
  if(SUCCEEDED(hr))
  {
    for(DWORD idx = 0; idx < dwReturn; idx++)
      {
        if(_wcsicmp(pAttrInfo[idx].pszAttrName, L"cn") == 0)
        {
          if(pAttrInfo[idx].dwADsType == ADSTYPE_CASE_IGNORE_STRING)
          {
            wprintf(L"Common Name: %s\n", 
                    pAttrInfo[idx].pADsValues[0].CaseIgnoreString);
          }
        }
        else if(_wcsicmp(pAttrInfo[idx].pszAttrName, L"title") == 0)
        {
          if(pAttrInfo->dwADsType == ADSTYPE_CASE_IGNORE_STRING)
          {
            wprintf(L"Title: %s\n", 
                    pAttrInfo[idx].pADsValues[0].CaseIgnoreString);
          }
        }
        else if(_wcsicmp(pAttrInfo[idx].pszAttrName, 
                L"otherTelephone") == 0)
        {  
          // Print the multi-valued property, "Other Telephones".
          if(pAttrInfo[idx].dwADsType == ADSTYPE_CASE_IGNORE_STRING)
        {
          wprintf(L"Other Telephones:");
          for(DWORD val = 0; val < pAttrInfo[idx].dwNumValues; val++) 
          {
            wprintf(L"  %s\n", 
                    pAttrInfo[idx].pADsValues[val].CaseIgnoreString);
          }
        }
      }
    }

    FreeADsMem(pAttrInfo);
  }
     
  pDirObject->Release();
}

CoUninitialize();
```



 

 




