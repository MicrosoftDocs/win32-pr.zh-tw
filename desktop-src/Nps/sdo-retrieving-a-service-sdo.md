---
title: 正在抓取服務 SDO
description: 正在抓取服務 SDO
ms.assetid: bac95c42-8f7e-4011-960c-8f18b4b7c088
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afcea1885e0ed714587e99bc7c2dcd92f2fea422
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186035"
---
# <a name="retrieving-a-service-sdo"></a><span data-ttu-id="b7de9-103">正在抓取服務 SDO</span><span class="sxs-lookup"><span data-stu-id="b7de9-103">Retrieving a Service SDO</span></span>

> [!Note]  
> <span data-ttu-id="b7de9-104">從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。</span><span class="sxs-lookup"><span data-stu-id="b7de9-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

<span data-ttu-id="b7de9-105">下列程式碼會為網路原則伺服器 (SDO) 抓取伺服器資料物件。</span><span class="sxs-lookup"><span data-stu-id="b7de9-105">The following code retrieves a Server Data Object (SDO) for the Network Policy Server .</span></span>


```C++
   HRESULT hr;
   CComPtr<IUnknown> pServiceUnknown;
   _bstr_t bstrServiceName = L"IAS";

   hr = pSdoMachine->GetServiceSDO(
      DATA_STORE_LOCAL,
      bstrServiceName,
      (IUnknown**) &pServiceUnknown
   );
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdoServiceControl>  pSdoServiceControl;
   hr = pServiceUnknown->QueryInterface(
      __uuidof(ISdoServiceControl),
      (void**) &pSdoServiceControl
   );
   if (FAILED(hr))
   {
      return hr;
   }
```



## <a name="remarks"></a><span data-ttu-id="b7de9-106">備註</span><span class="sxs-lookup"><span data-stu-id="b7de9-106">Remarks</span></span>

<span data-ttu-id="b7de9-107">您必須先 [附加](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) 至電腦，才能呼叫任何 [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) 方法。</span><span class="sxs-lookup"><span data-stu-id="b7de9-107">You must [attach](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) to a computer before you can call any of the [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7de9-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="b7de9-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7de9-109">附加至 SDO-Enabled 電腦</span><span class="sxs-lookup"><span data-stu-id="b7de9-109">Attaching to an SDO-Enabled Computer</span></span>](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer)
</dt> <dt>

[<span data-ttu-id="b7de9-110">**ISdoMachine::GetServiceSDO**</span><span class="sxs-lookup"><span data-stu-id="b7de9-110">**ISdoMachine::GetServiceSDO**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo)
</dt> <dt>

[<span data-ttu-id="b7de9-111">**ISdoServiceControl**</span><span class="sxs-lookup"><span data-stu-id="b7de9-111">**ISdoServiceControl**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol)
</dt> </dl>

 

 