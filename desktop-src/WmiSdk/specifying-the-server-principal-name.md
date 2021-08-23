---
description: Kerberos 驗證服務會指定伺服器主體名稱，以確保它所連接之電腦的身分識別。
ms.assetid: 3d58db28-2e69-4e27-9f27-61529abbf750
ms.tgt_platform: multiple
title: 指定伺服器主體名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8b3d05d6933653a7d2a1737d36f00f6ca65c39bd7739e5f2e9f4232eb507f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816421"
---
# <a name="specifying-the-server-principal-name"></a>指定伺服器主體名稱

Kerberos 驗證服務會指定伺服器主體名稱，以確保它所連接之電腦的身分識別。 藉由提供遠端電腦的名稱，在對腳本方法 [**wbemscripting.swbemlocator**](swbemlocator-connectserver.md) 的呼叫中指定伺服器主體名稱。 在 c + + 中，為 proxy 呼叫 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)時，于 *pServerPrincName* 參數中指定伺服器主體名稱。 如需詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。

Kerberos 需要此參數才能支援相互驗證。 不過，使用預設的伺服器主體名稱不允許相互驗證。 相互驗證很重要的用戶端，必須指定符合 WMI 服務所使用之伺服器身分識別的伺服器主體名稱。 如需設定 proxy 安全性的詳細資訊，以及顯示如何設定伺服器主體名稱的 c + + 範例，請參閱 [設定 IWbemServices 和其他 proxy 的安全性](setting-the-security-on-iwbemservices-and-other-proxies.md)。

如需有關在腳本和 Visual Basic 中設定伺服器主體名稱的詳細資訊，請參閱 [**wbemscripting.swbemlocator. ConnectServer**](swbemlocator-connectserver.md)及 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。

不同于 Windows Management Instrumentation (WMI) 的大部分安全性通訊協定，以及 (COM) 的元件物件模型，您無法在 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)的呼叫中設定伺服器主體。 不過，您可以使用 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)的 *BstrAuthority* 參數或 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)的 *pServerPrincName* 參數來設定伺服器主體。

本主題中的程式碼範例需要下列 \# include 語句才能正確編譯。


```C++
#include <wbemidl.h>
```



下列程式碼範例示範如何使用 [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)設定伺服器主體名稱。


```C++
IWbemServices* g_pNameSpace = NULL;

// Namespace to which to connect
BSTR  bstrNameSpace = 
SysAllocString( L"\\\\MyMachine\\root\default" );

// The bstrAuthority string contains the server
// principal name MyDomain\\MyMachine
// and the authentication service, which is Kerberos.
BSTR  bstrAuthority = 
SysAllocString( L"kerberos:MyDomain\\MyMachine"  );

HRESULT hr = NULL;
IWbemLocator* pWbemLocator = 0;

  hr = pWbemLocator->ConnectServer(
          bstrNameSpace,  // NameSpace name
          NULL,           // User name
          NULL,           // Password
          NULL,           // Locale
          0L,             // Security flags
          bstrAuthority,  // Authority, server principal name
          NULL,           // WBEM context
          &g_pNameSpace   // Namespace
          );

  // Free memory resources.
  g_pNameSpace->Release();
  SysFreeString(bstrNameSpace);
  SysFreeString(bstrAuthority);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 VBScript 設定驗證服務](setting-the-authentication-service-using-vbscript.md)
</dt> <dt>

[使用 c + + 設定驗證](setting-authentication-using-c-.md)
</dt> <dt>

[設定 IWbemServices 和其他 proxy 的安全性](setting-the-security-on-iwbemservices-and-other-proxies.md)
</dt> </dl>

 

 
