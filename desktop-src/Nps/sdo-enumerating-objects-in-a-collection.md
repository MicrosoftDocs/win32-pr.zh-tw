---
title: 列舉集合中的物件
description: 列舉集合中的物件
ms.assetid: 664e4d99-48ed-4948-b816-e92ad1ca3ece
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f3c543e01f3c8f154628c6e204aff53c6ad210
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965450"
---
# <a name="enumerating-objects-in-a-collection"></a><span data-ttu-id="99ab6-103">列舉集合中的物件</span><span class="sxs-lookup"><span data-stu-id="99ab6-103">Enumerating Objects in a Collection</span></span>

> [!Note]  
> <span data-ttu-id="99ab6-104">從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。</span><span class="sxs-lookup"><span data-stu-id="99ab6-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="99ab6-105">本主題的內容適用于 IAS 和 NPS。</span><span class="sxs-lookup"><span data-stu-id="99ab6-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="99ab6-106">在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。</span><span class="sxs-lookup"><span data-stu-id="99ab6-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="99ab6-107">下列程式碼會列舉 NPS 通訊協定集合中的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="99ab6-107">The following code enumerates the protocols in the NPS protocols collection.</span></span>


```C++
   HRESULT hr;

   //
   // Retrieve the protocols collection object
   //
   _variant_t vtIASProtocolsCollection;
   hr = pSdo->GetProperty(
      PROPERTY_IAS_PROTOCOLS_COLLECTION,
      &vtIASProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Retrieve the ISdoCollection interface 
   // for the object.
   //
   CComPtr<ISdoCollection> pIASProtocolsCollection;
   hr = vtIASProtocolsCollection.pdispVal->QueryInterface(
      __uuidof(ISdoCollection), 
      (void **) &pIASProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Retrieve the enumeration interface, IEnumVARIANT
   //
   CComPtr<IUnknown> pUnknownProtocol;
   hr = pIASProtocolsCollection->get__NewEnum(&pUnknownProtocol);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<IEnumVARIANT> pEnumProtocols;
   hr = pUnknownProtocol->QueryInterface(
      __uuidof(IEnumVARIANT), 
      (void **) &pEnumProtocols
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Retrieve the first protocol from the collection
   //
   DWORD      dwRetrieved = 1;
   _variant_t vtProtocol;
   hr = pEnumProtocols->Next(1, &vtProtocol, &dwRetrieved);
   if (FAILED(hr))
   {
      return hr;
   }

   while (hr != S_FALSE) {
      // 
      // Retrieve the name of the protocol
      //
      CComPtr<ISdo> pLocalSdo;
      hr = vtProtocol.pdispVal->QueryInterface(
         __uuidof(ISdo), 
         (void**)&pLocalSdo
      );
      if (FAILED(hr))
      {
         return hr;
      }

      _variant_t vtName;
      hr = pLocalSdo->GetProperty(PROPERTY_SDO_NAME, &vtName);
      if (FAILED(hr))
      {
         return hr;
      }

      vtProtocol.Clear();
      vtName.Clear();

      //
      // Retrieve the next protocol from the collection
      //
      dwRetrieved = 1;
      hr = pEnumProtocols->Next(1, &vtProtocol, &dwRetrieved);
      if (FAILED(hr))
      {
         return hr;
      }
   }

```



## <a name="remarks"></a><span data-ttu-id="99ab6-108">備註</span><span class="sxs-lookup"><span data-stu-id="99ab6-108">Remarks</span></span>

<span data-ttu-id="99ab6-109">VtName 和 vtProtocol 變數的類型為[ \_ variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))。</span><span class="sxs-lookup"><span data-stu-id="99ab6-109">The vtName and vtProtocol variables are of type [\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)).</span></span> <span data-ttu-id="99ab6-110">[ \_ Variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))物件會封裝或括住 **variant** 資料類型。</span><span class="sxs-lookup"><span data-stu-id="99ab6-110">A [\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)) object encapsulates, or encloses, the **VARIANT** data type.</span></span> <span data-ttu-id="99ab6-111">類別會管理資源配置和解除配置，並視需要對 [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) 和 [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) 進行函式呼叫。</span><span class="sxs-lookup"><span data-stu-id="99ab6-111">The class manages resource allocation and deallocation, and makes function calls to [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) and [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) as appropriate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99ab6-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="99ab6-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="99ab6-113">[\_variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="99ab6-113">[\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span></span>
</dt> <dt>

[<span data-ttu-id="99ab6-114">新增用戶端</span><span class="sxs-lookup"><span data-stu-id="99ab6-114">Adding a Client</span></span>](/windows/desktop/Nps/sdo-adding-a-client)
</dt> <dt>

[<span data-ttu-id="99ab6-115">**IASCOMMONPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="99ab6-115">**IASCOMMONPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties)
</dt> <dt>

[<span data-ttu-id="99ab6-116">**IEnumVARIANT**</span><span class="sxs-lookup"><span data-stu-id="99ab6-116">**IEnumVARIANT**</span></span>](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)
</dt> <dt>

[<span data-ttu-id="99ab6-117">**ISdo：： GetProperty**</span><span class="sxs-lookup"><span data-stu-id="99ab6-117">**ISdo::GetProperty**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[<span data-ttu-id="99ab6-118">正在抓取服務 SDO</span><span class="sxs-lookup"><span data-stu-id="99ab6-118">Retrieving a Service SDO</span></span>](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[<span data-ttu-id="99ab6-119">**VariantClear**</span><span class="sxs-lookup"><span data-stu-id="99ab6-119">**VariantClear**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[<span data-ttu-id="99ab6-120">**VariantInit**</span><span class="sxs-lookup"><span data-stu-id="99ab6-120">**VariantInit**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[<span data-ttu-id="99ab6-121">**變異**</span><span class="sxs-lookup"><span data-stu-id="99ab6-121">**VARIANT**</span></span>](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 