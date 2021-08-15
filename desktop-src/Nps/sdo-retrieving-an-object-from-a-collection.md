---
title: 從集合中取出物件
description: 從集合中取出物件
ms.assetid: df7cbff5-2d09-4031-8f41-3f4eea51598f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936cde1b897be9fc9fd7855401fdcef16b0754a59ae726a561acebd4ccd93283
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128558"
---
# <a name="retrieving-an-object-from-a-collection"></a>從集合中取出物件

下列程式碼會從用戶端的集合抓取用戶端的 IP 位址。 變數 pClientsCollection 會指向集合的 [**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) 介面。 如需如何取得集合物件的相關資訊，請參閱取得 [集合](/windows/desktop/Nps/sdo-retrieving-a-collection) 。


```C++
   HRESULT hr
   _variant_t vtClientName = L"Test Client";
   
   //
   // Get the client "Test Client" from the collection of clients
   //
   CComPtr<IDispatch> pFoundClientDispatch;
   hr = pClientsCollection->Item(&vtClientName, &pFoundClientDispatch);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pFoundClientSdo;
   hr = pFoundClientDispatch->QueryInterface(
      __uuidof(ISdo),
      (void **) &pFoundClientSdo
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Get the IP address of that client 
   //
   _variant_t vtAddress;
   hr = pFoundClientSdo->GetProperty(PROPERTY_CLIENT_ADDRESS ,&vtAddress);
   if (FAILED(hr))
   {
      return hr;
   }
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ISdoCollection：： Item**](/windows/desktop/api/sdoias/nf-sdoias-isdocollection-item)
</dt> <dt>

[正在抓取集合](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)
</dt> <dt>

[**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)
</dt> <dt>

[**變異**](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 