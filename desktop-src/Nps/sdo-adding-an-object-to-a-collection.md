---
title: 將物件加入至集合
description: 將物件加入至集合
ms.assetid: fc62698d-0bb9-478c-91cf-9f8fec36dba4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1990829e88d54838dbce2658c914ceff602d8e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966875"
---
# <a name="adding-an-object-to-a-collection"></a><span data-ttu-id="2da91-103">將物件加入至集合</span><span class="sxs-lookup"><span data-stu-id="2da91-103">Adding an Object to a Collection</span></span>

<span data-ttu-id="2da91-104">下列程式碼會將新的原則新增至 IAS 原則集合。</span><span class="sxs-lookup"><span data-stu-id="2da91-104">The following code adds a new policy to the IAS policies collection.</span></span> <span data-ttu-id="2da91-105">變數 pClientsCollection 會指向集合的 [**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) 介面。</span><span class="sxs-lookup"><span data-stu-id="2da91-105">The variable pClientsCollection points to an [**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) interface for the collection.</span></span> <span data-ttu-id="2da91-106">如需如何取得集合物件的相關資訊，請參閱取得 [集合](/windows/desktop/Nps/sdo-retrieving-a-collection) 。</span><span class="sxs-lookup"><span data-stu-id="2da91-106">See [Retrieving a Collection](/windows/desktop/Nps/sdo-retrieving-a-collection) for information on how to retrieve the collection object.</span></span>


```C++
   HRESULT hr;
   _bstr_t      bstrClientName = L"Test Client";
   VARIANT_BOOL vbNameUnique = VARIANT_FALSE;

   //
   // Check if the new client's name is unique
   //

   hr = pClientsCollection->IsNameUnique(bstrClientName, &vbNameUnique);
   if (FAILED(hr))
   {
      return hr;
   }

   if (VARIANT_FALSE == vbNameUnique)
   {
      //
      // The name is not unique. Handle the error
      //
      return E_FAIL;
   }

   //
   // Name is unique. Add the client.
   //
   CComPtr<IDispatch> pClientDispatch;
   pClientDispatch.p = NULL;
   hr = pClientsCollection->Add(bstrClientName, &pClientDispatch);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pClientSDO;
   hr = pClientDispatch->QueryInterface(
      __uuidof(ISdo),
      (void**) &pClientSDO
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Set the address for the client
   //
   _variant_t  vtClientAddress = L"127.0.0.1";
   hr = pClientSDO->PutProperty(PROPERTY_CLIENT_ADDRESS, &vtClientAddress);
   if (FAILED(hr))
   {
      return hr;
   }
       
   //
   // Set the shared secret for the client
   //
   _variant_t  vtClientSecret = L">@U#'6cc='5Ly9O5QKEj2RTJr*fM";
   hr = pClientSDO->PutProperty(PROPERTY_CLIENT_SHARED_SECRET, &vtClientSecret);
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Apply the changes
   //
   hr = pClientSDO->Apply();
   if (FAILED(hr))
   {
      return hr;
   }   
    
   //
   // Refresh the service using a ISdoServiceControl interface retrieved
   // in the code sample "Retrieve a Service SDO"
   //
   hr = pSdoServiceControl->ResetService();
   if (FAILED(hr))
   {
      //
      // If IAS is not installed or is not running then ignore the error
      //  
   }


```



## <a name="related-topics"></a><span data-ttu-id="2da91-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="2da91-107">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2da91-108">[\_bstr \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278286(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="2da91-108">[\_bstr\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278286(v=vs.60))</span></span>
</dt> <dt>

[<span data-ttu-id="2da91-109">**ISdoCollection：： Add**</span><span class="sxs-lookup"><span data-stu-id="2da91-109">**ISdoCollection::Add**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdocollection-add)
</dt> <dt>

[<span data-ttu-id="2da91-110">**ISdoCollection::IsNameUnique**</span><span class="sxs-lookup"><span data-stu-id="2da91-110">**ISdoCollection::IsNameUnique**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdocollection-isnameunique)
</dt> <dt>

[<span data-ttu-id="2da91-111">正在抓取集合</span><span class="sxs-lookup"><span data-stu-id="2da91-111">Retrieving a Collection</span></span>](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[<span data-ttu-id="2da91-112">**變異**</span><span class="sxs-lookup"><span data-stu-id="2da91-112">**VARIANT**</span></span>](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 