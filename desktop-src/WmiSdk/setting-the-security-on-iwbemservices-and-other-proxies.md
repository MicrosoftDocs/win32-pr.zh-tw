---
description: 在 c + + 中，您可以在透過 IWbemLocator：： ConnectServer 連接至 WMI 之前呼叫 CoInitializeSecurity，以設定整個進程的安全性。
ms.assetid: 83c04a96-3829-4c07-91a7-06e5b75b2c12
ms.tgt_platform: multiple
title: 設定 IWbemServices 和其他 proxy 的安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d593c52091182b1f0580908624e0b4068ed3f8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984245"
---
# <a name="setting-the-security-on-iwbemservices-and-other-proxies"></a>設定 IWbemServices 和其他 proxy 的安全性

在 c + + 中，您可以在透過 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)連接至 WMI 之前呼叫 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ，以設定整個進程的安全性。 您也可以在取得 WMI proxy 指標的呼叫中，變更驗證等級、模擬等級或驗證服務，例如 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 或 [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)。 呼叫 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) 也可讓您變更 (KERBEROS、NTLM 或 negotiate) 的驗證服務。

腳本和 Visual Basic 應用程式只會透過呼叫 [**SWbemServices**](swbemservices.md) 和其他 automation 物件，間接設定 proxy 上的安全性。 如需有關在腳本中設定和變更驗證和模擬的詳細資訊，請參閱 [使用 VBScript 設定預設進程安全性等級](setting-the-default-process-security-level-using-vbscript.md)。

在執行不同作業系統的遠端電腦上連線至 WMI 時，變更安全性層級或服務主要是一項考慮。 如需詳細資訊，請參閱 [在不同的作業系統之間進行連接](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)。

用戶端應用程式會使用身分識別連接到 WMI proxy。 身分識別是包含使用者名稱、密碼和授權設定的資料物件。 針對 WMI 用戶端應用程式，呼叫 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) 介面會建立初始身分識別。 [**ConnectServer**](swbemlocator-connectserver.md)方法會採用一組三個參數中的身分識別，您可以將其設定為 **Null** 以表示目前的使用者。 您也可以指定非 **Null** 參數，以指出特定的使用者和網域。 如果呼叫成功， **ConnectServer** 會傳回可讓您存取各種遠端進程的指標，例如 WMI 服務或 Windows 作業系統。

如同許多 COM 介面， [**ConnectServer**](swbemlocator-connectserver.md) 會傳回 proxy 的指標。 Proxy 是代表遠端進程的資料物件，例如 WMI 或遠端提供者。 COM 會使用 proxy 來允許開發人員存取遠端資料，就像是在本機資料一樣。

下列 WMI 介面會使用 proxy：

-   [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) ([**SWbemServices**](swbemservices.md) 腳本物件) 
-   [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)
-   [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)
-   [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) ([**SWbemRefresher**](swbemrefresher.md) 腳本物件) 

    WMI 重新整理程式是特殊案例，因為它會傳遞 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 指標，而其安全性設定必須正確設定。 如需使用重新整理程式物件的詳細資訊，請參閱使用 [c + + 存取效能資料](accessing-performance-data-in-c--.md)。

當您收到遠端進程的指標之後，您可以進行兩項作業。 如果您知道進程的功能，您可以選擇在指標上設定安全性，並正常存取進程。 大部分的 WMI 服務指標都是如此。 如需詳細資訊，請參閱 [設定 WMI 連接的安全性層級](setting-the-security-levels-on-a-wmi-connection.md)。 或者，您必須透過呼叫 proxy 上的 [**iunknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面，在 proxy 上存取不同的 COM 介面，例如 [**Iunknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)。

## <a name="defaults-and-recommendations"></a>預設值和建議

元件物件模型的分散式版本 (DCOM) 將預設驗證服務 (Kerberos、NTLM 或 Negotiate) 進行協調，而您無法使用 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)指定預設驗證服務。 在 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)的驗證服務參數中指定 **RPC \_ C \_ 驗證 \_ 預設值**，可讓 DCOM 選取適當的服務。 針對遠端連線，預設服務是 Negotiate，這是在 Kerberos 和非 Kerberos 網域中運作的應用程式所建議的服務。 針對本機連接，預設驗證服務為 NT LAN Manager (NTLM) 。

下列程式碼範例顯示所使用的預設驗證服務。


```C++
// The pWbemServices variable is of type IWbemServices*

HRESULT hr = CoSetProxyBlanket(
     pWbemServices,                //Proxy
     RPC_C_AUTHN_DEFAULT,          //Authentication service 
     RPC_C_AUTHZ_DEFAULT,          //Authorization service 
     COLE_DEFAULT_PRINCIPAL,       //Server principal name used 
                                       // by authentication service
     RPC_C_AUTHN_LEVEL_DEFAULT,    //Authentication level
     RPC_C_IMP_LEVEL_IMPERSONATE,  //Impersonation level
     COLE_DEFAULT_AUTHINFO,       //Client identity
     EOAC_DEFAULT                  //Capability flags
     );
```



本主題中的程式碼範例需要下列參考和 \# include 語句。


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



針對腳本，建議您使用 DCOM 針對遠端呼叫所選取的預設值。 在本機電腦上，您不能指定驗證服務來呼叫 WMI。 如需詳細資訊，請參閱 [使用 VBScript 設定驗證服務](setting-the-authentication-service-using-vbscript.md) 和 [建立標記字串](constructing-a-moniker-string.md)。

 

 
