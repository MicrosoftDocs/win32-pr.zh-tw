---
title: 正在抓取集合
description: 正在抓取集合
ms.assetid: b9090ad5-564c-4f48-b7bd-24617d582d2e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 343f00ee28475d1e6180646a0e548c18d51701afed587c99582dad7dc60d094c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063308"
---
# <a name="retrieving-a-collection"></a>正在抓取集合

> [!Note]  
> 網際網路驗證服務 (IAS) 已重新命名網路原則伺服器 (NPS) 從 Windows Server 2008 開始。 本主題的內容適用于 IAS 和 NPS。 在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。

 

下列程式碼會抓取網路原則伺服器的用戶端集合。


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



## <a name="remarks"></a>備註

PSdoServiceControl 變數包含 NPS 的伺服器資料物件指標。 如需詳細資訊，請參閱「取得 [服務 SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)」主題。

VtClientsCollection 變數的類型為[ \_ variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))。 \_Variant \_ t 物件會封裝或括住 [**variant**](/windows/win32/api/oaidl/ns-oaidl-variant)資料類型。 類別會管理資源配置和解除配置，並視需要對 [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) 和 [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) 進行函式呼叫。

在呼叫 "pSdo->GetProperty () " 之後，vtProtocolsCollection 變數會指定物件。 VtProtocolsCollection 的 **pdispVal** 成員包含物件的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面指標。

上述範例程式碼可以調整以取得其他 NPS 集合，例如 NPS 要求處理常式集合。 [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)列舉型別會列舉對應至可用 NPS 集合的值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[\_variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))
</dt> <dt>

[**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> <dt>

[**ISdo：： GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[正在抓取服務 SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[**變異**](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 