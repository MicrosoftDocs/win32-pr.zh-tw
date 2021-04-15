---
title: 撰寫 RpcNs 服務的 Spn
description: 下列程式碼範例會針對在目錄的 RpcServices 容器中具有專案的 RPC 服務，撰寫 (Spn) 的服務主體名稱。 RPC 服務會使用 RpcNsBindingExport 函式來建立其 RpcServices 專案。
ms.assetid: 4fd585b3-3f9b-4f7f-bc1b-22879587a590
ms.tgt_platform: multiple
keywords:
- 撰寫 RpcNs 服務 AD 的 Spn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb65b377b5bdd041c5a34b05262f7e62f43801c5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462912"
---
# <a name="composing-spns-for-an-rpcns-service"></a>撰寫 RpcNs 服務的 Spn

下列程式碼範例會針對在目錄的 RpcServices 容器中具有專案的 RPC 服務，撰寫 (Spn) 的服務主體名稱。 RPC 服務會使用 [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) 函式來建立其 RpcServices 專案。

RPC 服務會使用這個程式碼範例來建立 SPN 或 Spn，以識別服務的實例。 此服務會使用此常式來執行下列工作：

-   在安裝或移除服務時，註冊或取消註冊目錄中的 Spn。 如需詳細資訊和程式碼範例，請參閱 [註冊服務的 spn](registering-the-spns-for-a-service.md)。
-   當服務啟動時，請向 RPC 驗證服務註冊其本身。 如需詳細資訊，請參閱 [RPC 應用程式中的相互驗證](mutual-authentication-in-rpc-applications.md)。

這個程式碼範例會使用服務之 RpcServices 專案的分辨名稱來組成 SPN。 呼叫此程式碼之前，請先呼叫 [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) 函式來建立服務的 RpcServices 專案。

這個程式碼範例會呼叫 [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) 函數來建立 SPN。 SPN 是由服務類別名稱和服務 RpcServices 專案的分辨名稱所組成。


```C++
/**********

    SpnCompose()

    Composes a service principal name from a service name and class.

    Parameters:

    pszServiceName - Contains a null-terminated string that contains 
    the name of the service.

    pszServiceClass - Contains a null-terminated string that contains 
    the name of the service class.

    pspn - Pointer to an LPTSTR array that receives the array of 
    SPNs. This array must freed with the DsFreeSpnArray function when 
    it is no longer required.

    pulSpn - Pointer to a unsigned long that receives the number of 
    elements in the pspn array.

***********/

HRESULT SpnCompose(LPTSTR pszServiceName, 
                   LPTSTR pszServiceClass, 
                   LPTSTR **pspn, 
                   unsigned long *pulSpn) 
{
    HRESULT hr;
    CComPtr<IADs> spRoot;

    // Get the defaultNamingContext for the local domain.
    hr = ADsGetObject(L"LDAP://RootDSE",
                      IID_IADs,
                      (void**)&spRoot);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the distinguished name of the current domain.
    CComVariant svarDSRoot;
    hr = spRoot->Get(CComBSTR("defaultNamingContext"), &svarDSRoot);
     
    /*
    Compose the DN of the service's entry in the RpcServices 
    container, created by a call to RpcNsBindingExport. The entry 
    for an RPC service is in the System/RpcServices container in the 
    defaultNamingContext of the local domain.
    */
    
    CComBSTR sbstrDsEntryName = "CN=";
    sbstrDsEntryName += pszServiceName;
    sbstrDsEntryName += ",CN=RpcServices,CN=System,";
    sbstrDsEntryName += svarDSRoot.bstrVal;

    USES_CONVERSION;  // Required for the W2T() macro.
    DWORD status;

    /*
    Build the SPN for this service using the DN and the service 
    class.
    */
    status = DsGetSpn(
        DS_SPN_SERVICE, // Type of SPN to create.
        pszServiceClass, // Service class - a name in this case.
        W2T(sbstrDsEntryName), // DN of the RpcServices for 
                               // this RPC service.
        0, // Use the default instance port.
        0, // Number of additional instance names.
        NULL, // No additional instance names.
        NULL, // No additional instance ports.
        pulSpn, // Size of SPN array.
        pspn // Returned SPN(s).
        );
     
    return HRESULT_FROM_WIN32(status);
}
```



 

 