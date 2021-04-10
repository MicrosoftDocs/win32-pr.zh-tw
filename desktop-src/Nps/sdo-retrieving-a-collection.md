---
title: 正在抓取集合
description: 正在抓取集合
ms.assetid: b9090ad5-564c-4f48-b7bd-24617d582d2e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 517acfa320069f9c94ee291e9215459d27ba25ad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933419"
---
# <a name="retrieving-a-collection"></a><span data-ttu-id="fbb20-103">正在抓取集合</span><span class="sxs-lookup"><span data-stu-id="fbb20-103">Retrieving a Collection</span></span>

> [!Note]  
> <span data-ttu-id="fbb20-104">從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。</span><span class="sxs-lookup"><span data-stu-id="fbb20-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="fbb20-105">本主題的內容適用于 IAS 和 NPS。</span><span class="sxs-lookup"><span data-stu-id="fbb20-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="fbb20-106">在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。</span><span class="sxs-lookup"><span data-stu-id="fbb20-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="fbb20-107">下列程式碼會抓取網路原則伺服器的用戶端集合。</span><span class="sxs-lookup"><span data-stu-id="fbb20-107">The following code retrieves the clients collection for the Network Policy Server.</span></span>


```C++
// Retrieve the clients collection 
   HRESULT hr;
   CComPtr<ISdo>  pSdo;
   hr = pSdoServiceControl->QueryInterface(
      __uuidof(ISdo),
      (void**) &pSdo
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // First Retrieve the protocols collection
   //
   _variant_t  vtProtocolsCollection;
   hr = pSdo->GetProperty(
      PROPERTY_IAS_PROTOCOLS_COLLECTION,
      &vtProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Get the ISdoCollection interface 
   // for the object.
   //
   CComPtr<ISdoCollection>  pProtocolsCollection;
   hr = vtProtocolsCollection.pdispVal->QueryInterface(
      __uuidof(ISdoCollection), 
      (void **) &pProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Then retrieve the RADIUS protocol
   //
   CComPtr<IDispatch> pRadiusDispatch;
   _variant_t  vtProtocolName = L"Microsoft Radius Protocol";
   hr = pProtocolsCollection->Item(&vtProtocolName, &pRadiusDispatch);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pRadiusSdo;
   hr = pRadiusDispatch->QueryInterface(      
      __uuidof(ISdo), 
      (void **) &pRadiusSdo
   );

   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Then retrieve the clients collection
   //
   _variant_t  vtClientsCollection;
   hr = pRadiusSdo->GetProperty(PROPERTY_RADIUS_CLIENTS_COLLECTION, &vtClientsCollection);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdoCollection> pClientsCollection;
   hr = vtClientsCollection.pdispVal->QueryInterface(      
      __uuidof(ISdoCollection), 
      (void **) &pClientsCollection
   );

   if (FAILED(hr))
   {
      return hr;
   }

```



## <a name="remarks"></a><span data-ttu-id="fbb20-108">備註</span><span class="sxs-lookup"><span data-stu-id="fbb20-108">Remarks</span></span>

<span data-ttu-id="fbb20-109">PSdoServiceControl 變數包含 NPS 的伺服器資料物件指標。</span><span class="sxs-lookup"><span data-stu-id="fbb20-109">The pSdoServiceControl variable contains a pointer to a Server Data Object for NPS.</span></span> <span data-ttu-id="fbb20-110">如需詳細資訊，請參閱「取得 [服務 SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)」主題。</span><span class="sxs-lookup"><span data-stu-id="fbb20-110">For more information, see the topic [Retrieving a Service SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo).</span></span>

<span data-ttu-id="fbb20-111">VtClientsCollection 變數的類型為[ \_ variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))。</span><span class="sxs-lookup"><span data-stu-id="fbb20-111">The vtClientsCollection variable is of type [\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)).</span></span> <span data-ttu-id="fbb20-112">\_Variant \_ t 物件會封裝或括住 [**variant**](/windows/win32/api/oaidl/ns-oaidl-variant)資料類型。</span><span class="sxs-lookup"><span data-stu-id="fbb20-112">A \_variant\_t object encapsulates, or encloses, the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) data type.</span></span> <span data-ttu-id="fbb20-113">類別會管理資源配置和解除配置，並視需要對 [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) 和 [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) 進行函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="fbb20-113">The class manages resource allocation and deallocation, and makes function calls to [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) and [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) as appropriate.</span></span>

<span data-ttu-id="fbb20-114">在呼叫 "pSdo->GetProperty () " 之後，vtProtocolsCollection 變數會指定物件。</span><span class="sxs-lookup"><span data-stu-id="fbb20-114">After the call to "pSdo->GetProperty()", the vtProtocolsCollection variable specifies an object.</span></span> <span data-ttu-id="fbb20-115">VtProtocolsCollection 的 **pdispVal** 成員包含物件的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="fbb20-115">The **pdispVal** member of vtProtocolsCollection contains a pointer to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface for the object.</span></span>

<span data-ttu-id="fbb20-116">上述範例程式碼可以調整以取得其他 NPS 集合，例如 NPS 要求處理常式集合。</span><span class="sxs-lookup"><span data-stu-id="fbb20-116">The above sample code can be adapted to retrieve other NPS collections, for example the NPS Request Handlers collections.</span></span> <span data-ttu-id="fbb20-117">[**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)列舉型別會列舉對應至可用 NPS 集合的值。</span><span class="sxs-lookup"><span data-stu-id="fbb20-117">The [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) enumeration type enumerated values that correspond to the available NPS collections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fbb20-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="fbb20-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fbb20-119">[\_variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="fbb20-119">[\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span></span>
</dt> <dt>

[<span data-ttu-id="fbb20-120">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="fbb20-120">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> <dt>

[<span data-ttu-id="fbb20-121">**ISdo：： GetProperty**</span><span class="sxs-lookup"><span data-stu-id="fbb20-121">**ISdo::GetProperty**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[<span data-ttu-id="fbb20-122">**ISdoCollection**</span><span class="sxs-lookup"><span data-stu-id="fbb20-122">**ISdoCollection**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[<span data-ttu-id="fbb20-123">正在抓取服務 SDO</span><span class="sxs-lookup"><span data-stu-id="fbb20-123">Retrieving a Service SDO</span></span>](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[<span data-ttu-id="fbb20-124">**VariantClear**</span><span class="sxs-lookup"><span data-stu-id="fbb20-124">**VariantClear**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[<span data-ttu-id="fbb20-125">**VariantInit**</span><span class="sxs-lookup"><span data-stu-id="fbb20-125">**VariantInit**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[<span data-ttu-id="fbb20-126">**變異**</span><span class="sxs-lookup"><span data-stu-id="fbb20-126">**VARIANT**</span></span>](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 