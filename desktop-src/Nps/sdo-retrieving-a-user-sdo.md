---
title: 正在抓取使用者 SDO
description: 正在抓取使用者 SDO
ms.assetid: 440628f8-081b-4e7f-bdb2-760ff9bd0d77
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c1d6320398afb4eed22f72f0c5e12495010323
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933418"
---
# <a name="retrieving-a-user-sdo"></a><span data-ttu-id="c3c0e-103">正在抓取使用者 SDO</span><span class="sxs-lookup"><span data-stu-id="c3c0e-103">Retrieving a User SDO</span></span>

<span data-ttu-id="c3c0e-104">下列程式碼會為系統管理員 (SDO) 抓取伺服器資料物件。</span><span class="sxs-lookup"><span data-stu-id="c3c0e-104">The following code retrieves a Server Data Object (SDO) for the Administrator.</span></span>


```C++
   HRESULT  hr;
   _bstr_t bstrUserName = L"Administrator";
   CComPtr<IUnknown> pUserUnknown;

   hr = pSdoMachine->GetUserSDO(
      DATA_STORE_LOCAL,
      bstrUserName,
      (IUnknown**) &pUserUnknown
   );
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pUserSDO;
   hr = pUserUnknown->QueryInterface(
      __uuidof(ISdo),
      (void**) &pUserSDO
   );
   if (FAILED(hr))
   {
      return hr;
   }
```



## <a name="related-topics"></a><span data-ttu-id="c3c0e-105">相關主題</span><span class="sxs-lookup"><span data-stu-id="c3c0e-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3c0e-106">附加至 SDO-Enabled 電腦</span><span class="sxs-lookup"><span data-stu-id="c3c0e-106">Attaching to an SDO-Enabled Computer</span></span>](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer)
</dt> <dt>

[<span data-ttu-id="c3c0e-107">**ISdo**</span><span class="sxs-lookup"><span data-stu-id="c3c0e-107">**ISdo**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

[<span data-ttu-id="c3c0e-108">**ISdoMachine**</span><span class="sxs-lookup"><span data-stu-id="c3c0e-108">**ISdoMachine**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdomachine)
</dt> <dt>

[<span data-ttu-id="c3c0e-109">**ISdoMachine::GetUserSDO**</span><span class="sxs-lookup"><span data-stu-id="c3c0e-109">**ISdoMachine::GetUserSDO**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo)
</dt> <dt>

[<span data-ttu-id="c3c0e-110">**SysAllocString**</span><span class="sxs-lookup"><span data-stu-id="c3c0e-110">**SysAllocString**</span></span>](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)
</dt> <dt>

[<span data-ttu-id="c3c0e-111">**SysFreeString**</span><span class="sxs-lookup"><span data-stu-id="c3c0e-111">**SysFreeString**</span></span>](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)
</dt> </dl>

 

 