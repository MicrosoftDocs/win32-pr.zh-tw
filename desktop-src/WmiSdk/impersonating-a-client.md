---
description: 當使用者應用程式透過 WMI 提供者向系統上的物件要求資料時，模擬表示提供者會顯示代表用戶端安全性層級的認證，而不是提供者。
ms.assetid: 6d54f234-45aa-445b-ad50-7d5a9946c134
ms.tgt_platform: multiple
title: 模擬用戶端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 162857d90c8bddb70d90eb2e10efbc08537299d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850772"
---
# <a name="impersonating-a-client"></a>模擬用戶端

當使用者應用程式透過 WMI 提供者向系統上的物件要求資料時，模擬表示提供者所呈現的認證代表用戶端的安全性層級，而不是提供者的認證。 模擬可防止用戶端取得系統上資訊的未經授權存取權。

本主題將討論下列各節：

-   [註冊提供者進行模擬](#registering-a-provider-for-impersonation)
-   [設定提供者內的模擬層級](#setting-impersonation-levels-within-a-provider)
-   [維護提供者中的安全性層級](#maintaining-security-levels-in-a-provider)
-   [處理提供者中的拒絕存取訊息](#handling-access-denied-messages-in-a-provider)
-   [報告部分實例](#reporting-partial-instances)
-   [報告部分列舉](#reporting-partial-enumerations)
-   [對拒絕存取程式碼進行偵錯工具](#debugging-your-access-denied-code)
-   [相關主題](#related-topics)

WMI 通常會以高安全性層級的系統管理服務來執行，並使用 LocalServer 安全性內容。 使用系統管理服務會提供 WMI 存取特殊許可權資訊的方法。 當呼叫提供者取得資訊時，WMI 會將其安全識別碼 (SID) 傳送給提供者，讓提供者能夠存取相同高安全性層級的資訊。

在 WMI 應用程式啟動過程中，Windows 作業系統會為 WMI 應用程式提供開始處理常式之使用者的安全性內容。 使用者的安全性內容通常是比 LocalServer 更低的安全性層級，因此使用者可能沒有許可權可以存取 WMI 可用的所有資訊。 當使用者應用程式要求動態資訊時，WMI 會將使用者的 SID 傳遞給對應的提供者。 如果有適當的寫入，則提供者會嘗試使用使用者 SID （而不是提供者 SID）來存取訊號。

若要讓提供者成功模擬用戶端應用程式，用戶端應用程式和提供者必須符合下列準則：

-   用戶端應用程式必須使用 **RPC \_ c \_ IMP \_ level \_** 模擬或 **RPC \_ c \_ IMP \_ 層級 \_ 委派** 的 COM 連接安全性層級來呼叫 WMI。 如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md)。
-   提供者必須以模擬提供者的形式向 WMI 註冊。 如需詳細資訊，請參閱 [註冊提供者以進行](#registering-a-provider-for-impersonation)模擬。
-   提供者必須先切換至用戶端應用程式的安全性層級，才能存取特殊許可權資訊。 如需詳細資訊，請參閱 [設定提供者內的模擬層級](#setting-impersonation-levels-within-a-provider)。
-   如果拒絕存取這項資訊，則提供者必須正確地處理錯誤狀況。 如需詳細資訊，請參閱 [處理提供者中的拒絕存取訊息](#handling-access-denied-messages-in-a-provider)。

## <a name="registering-a-provider-for-impersonation"></a>註冊提供者進行模擬

WMI 只會將用戶端應用程式的 SID 傳遞給已註冊為模擬提供者的提供者。 若要讓提供者執行模擬，您必須修改提供者註冊程式。

下列程式說明如何註冊提供者以進行模擬。 此程式假設您已瞭解註冊程式。 如需註冊程式的詳細資訊，請參閱 [註冊提供者](registering-a-provider.md)。

**註冊提供者進行模擬**

1.  將代表提供者的 [**\_ \_ Win32Provider**](--win32provider.md)類別的 [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md)屬性設定為1。

    [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md)屬性會記錄提供者是否支援模擬。 將 **ImpersonationLevel** 設定為0，表示提供者不會模擬用戶端，並在與 WMI 相同的使用者內容中執行所有要求的作業。 將 **ImpersonationLevel** 設定為1，表示提供者使用模擬呼叫來檢查代表用戶端執行的作業。

2.  將相同 [**\_ \_ Win32Provider**](--win32provider.md)類別的 **PerUserInitialization** 屬性設定為 **TRUE**。

> [!Note]  
> 如果您註冊提供者，並將 [**\_ \_ Win32Provider**](--win32provider.md)屬性 **InitializeAsAdminFirst** 設定為 **TRUE**，則提供者只會在初始化階段使用管理層級執行緒安全性權杖。 呼叫 [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) 時，提供者會使用 WMI 的安全性內容，而不會使用用戶端的安全性內容。

 

下列程式碼範例示範如何註冊提供者以進行模擬。

``` syntax
instance of __Win32Provider
{
    CLSID = "{FD4F53E0-65DC-11d1-AB64-00C04FD9159E}";
    ImpersonationLevel = 1;
    Name = "MS_NT_EVENTLOG_PROVIDER";
    PerUserInitialization = TRUE;
};
```

## <a name="setting-impersonation-levels-within-a-provider"></a>設定提供者內的模擬層級

如果您使用 [**\_ \_ Win32Provider**](--win32provider.md)類別屬性 [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md)設定為1來註冊提供者，則 WMI 會呼叫您的提供者來模擬不同的用戶端。 若要處理這些呼叫，請在您的 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)介面的執行中使用 [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient)和 [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) COM 函數。

[**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient)函式可讓伺服器模擬發出呼叫的用戶端。 藉由將 **CoImpersonateClient** 呼叫放入 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)的執行，您可以讓您的提供者設定提供者的執行緒 token，使其符合用戶端的執行緒 token，進而模擬用戶端。 如果您未呼叫 **CoImpersonateClient**，則您的提供者會以系統管理員層級的安全性執行程式碼，進而造成潛在的安全性弱點。 如果您的提供者暫時需要以系統管理員身分執行，或要手動執行存取檢查，請呼叫 [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself)。

相較于 [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient)， [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) 是處理執行緒模擬層級的 COM 函數。 在此情況下， **CoRevertToSelf** 會將模擬等級變更回原始的模擬設定。 一般情況下，提供者一開始是系統管理員，而且會根據其是否正在進行代表呼叫端或本身呼叫的呼叫，在 **CoImpersonateClient** 和 **CoRevertToSelf** 之間進行替代。 提供者必須負責正確地放置這些呼叫，如此才不會向終端使用者公開安全性漏洞。 例如，提供者應該只在模擬的程式碼序列內呼叫原生 Windows 函數。

> [!Note]  
> [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient)和 [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself)的目的是設定提供者的安全性。 如果您判斷您的模擬失敗，您應該透過 [**IWbemObjectSink：： SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus)將適當的完成程式碼傳回至 WMI。 如需詳細資訊，請參閱 [處理提供者中的拒絕存取訊息](#handling-access-denied-messages-in-a-provider)。

 

## <a name="maintaining-security-levels-in-a-provider"></a>維護提供者中的安全性層級

提供者無法在 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)的執行中呼叫 [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient)一次，並假設提供者的持續時間內會保留模擬認證。 相反地，在執行過程中多次呼叫 **CoImpersonateClient** ，以防止 WMI 變更認證。

為提供者設定模擬的主要考慮是重新進入。 在此內容中，當提供者呼叫 WMI 以取得資訊並等候 WMI 回呼提供者時，就會發生重新進入。 基本上，執行的執行緒會離開提供者程式碼，只會在日後重新輸入程式碼。 「重入」是 COM 設計的一部分，而且通常不會有問題。 不過，當執行的執行緒進入 WMI 時，執行緒會採用 WMI 的模擬層級。 當執行緒返回提供者時，您必須使用另一個 [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient)呼叫來重設模擬層級。

若要保護您的提供者中的安全性漏洞，您應該只在模擬用戶端時，將可重新進入的呼叫加入至 WMI。 也就是說，在您呼叫 [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) 之後，以及在呼叫 [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself)之前，應該發出 WMI 的呼叫。 因為 **CoRevertToSelf** 會將模擬設定為使用者層級的 wmi 正在執行，通常是 LocalSystem，在呼叫 **CoRevertToSelf** 之後可重新進入 wmi 的呼叫，可讓使用者和任何呼叫的提供者都有更多功能。

> [!Note]  
> 如果您呼叫系統函數或其他介面方法，則不保證會維護呼叫內容。

 

## <a name="handling-access-denied-messages-in-a-provider"></a>處理提供者中的拒絕存取訊息

當用戶端要求沒有存取權的類別或資訊時，會出現大部分的拒絕存取錯誤訊息。 如果提供者傳回拒絕存取的錯誤訊息至 WMI，而 WMI 將此訊息傳遞至用戶端，則用戶端可以推斷該資訊是否存在。 在某些情況下，這可能會違反安全性。 因此，您的提供者不應將訊息傳播至用戶端。 相反地，不應該公開提供者所提供的一組類別。 同樣地，動態執行個體提供者應該呼叫基礎資料來源，以判斷如何處理拒絕存取訊息。 提供者必須負責將該原理複寫至 WMI 環境。 如需詳細資訊，請參閱 [報告部分實例](#reporting-partial-instances) 和 [報告部分](#reporting-partial-enumerations)列舉。

當您判斷您的提供者應該如何處理拒絕存取訊息時，您必須撰寫程式碼並對其進行偵錯工具。 在進行偵錯工具時，您通常很方便分辨因為低模擬而造成的拒絕，以及因您的程式碼錯誤而造成的拒絕。 您可以在程式碼中使用簡單的測試來判斷差異。 如需詳細資訊，請參閱 [偵錯工具拒絕存取程式碼](#debugging-your-access-denied-code)。

## <a name="reporting-partial-instances"></a>報告部分實例

拒絕存取訊息的其中一種常見的情況是 WMI 無法提供所有資訊來填滿實例。 例如，用戶端可能會有權查看硬碟物件，但可能沒有許可權可查看硬碟上有多少可用的空間。 當提供者因為存取違規而無法完全填滿具有屬性的實例時，您的提供者必須判斷如何處理任何情況。

WMI 不需要單一回應對實例具有部分存取權的用戶端。 相反地，WMI 1.x 版允許提供者下列其中一個選項：

-   使用 **WBEM \_ E \_ \_ 拒絕存取** 來使整個作業失敗，並不會傳回任何實例。

    傳回錯誤物件以及 **WBEM \_ E \_ \_ 拒絕存取**，以描述拒絕的原因。

-   傳回所有可用的屬性，並以 **Null** 填滿無法使用的屬性。

> [!Note]  
> 請確定傳回 **WBEM \_ E \_ \_ 拒絕存取** 未在您的企業中建立安全性漏洞。

 

## <a name="reporting-partial-enumerations"></a>報告部分列舉

存取違規的另一項常見的情況是 WMI 無法傳回所有列舉。 例如，用戶端可能會有存取權來查看所有區域網路電腦物件，但可能無法存取其網域以外的電腦物件。 當列舉因存取違規而無法完成時，您的提供者必須決定如何處理任何情況。

與執行個體提供者一樣，WMI 不需要對部分列舉進行單一回應。 相反地，WMI 1.x 版允許提供者使用下列其中一個選項：

-   針對提供者可存取的所有實例，傳回 **WBEM \_ S \_ \_** 。

    如果您使用此選項，使用者就不會察覺到某些實例無法使用。 許多提供者（例如使用結構化查詢語言 (SQL)  (SQL) 具有資料列層級安全性）的提供者，會使用呼叫端的安全性層級來定義結果集，以傳回成功的部分結果。

-   使用 **WBEM \_ E \_ \_ 拒絕存取** 來使整個作業失敗，並不會傳回任何實例。

    提供者可以選擇性地包含描述用戶端情況的錯誤物件。 請注意，某些提供者可能會以序列方式存取資料來源，而且在透過列舉中途之前可能不會發生拒絕。

-   傳回所有可存取的實例，但也會傳回 nonerror 狀態碼 **WBEM \_ S \_ \_ 拒絕存取**。

    提供者應該在列舉期間記下拒絕，並可繼續提供實例，並完成 nonerror 狀態碼。 提供者也可以選擇在第一次拒絕時終止列舉。 此選項的理由是不同的提供者具有不同的抓取範例。 在探索存取違規之前，提供者可能已經提供實例。 有些提供者可能會選擇繼續提供其他實例，而其他則可能想要終止。

由於 COM 的結構，因此您無法在錯誤物件以外的錯誤中封送處理回任何資訊。 因此，您無法同時傳回信息和錯誤碼。 如果您選擇傳回信息，則必須改為使用 nonerror 狀態碼。

## <a name="debugging-your-access-denied-code"></a>對拒絕存取程式碼進行偵錯工具

某些應用程式可能會使用低於 **RPC \_ C \_ IMP \_ 層級 \_** 模擬的模擬層級。 在此情況下，用戶端應用程式提供者所做的大部分模擬呼叫將會失敗。 若要成功設計和執行提供者，您必須記住這個概念。

依預設，只能存取提供者的其他模擬層級是 **RPC \_ C \_ IMP \_ level \_ 識別**。 在用戶端應用程式使用 **RPC \_ C \_ IMP \_ 層級 \_ 識別** 的情況下， [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) 不會傳回錯誤碼。 相反地，提供者只會模擬用戶端以供識別之用。 因此，提供者所呼叫的大部分 Windows 方法都會傳回拒絕存取訊息。 這在實務上是無害的，因為不允許使用者進行任何不適當的動作。 不過，在提供者開發期間，它可能會很有用，以得知用戶端是否真的經過模擬。

程式碼需要下列參考，且必須 \# 要有語句才能正確編譯。


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



下列程式碼範例示範如何判斷提供者是否已成功模擬用戶端應用程式。


```C++
DWORD dwImp = 0;
HANDLE hThreadTok;
DWORD dwBytesReturned;
BOOL bRes;

// You must call this before trying to open a thread token!
CoImpersonateClient();

bRes = OpenThreadToken(
    GetCurrentThread(),
    TOKEN_QUERY,
    TRUE,
    &hThreadTok
);

if (bRes == FALSE)
{
    printf("Unable to read thread token (%d)\n", GetLastError());
    return 0;
}

bRes = GetTokenInformation(
    hThreadTok,
    TokenImpersonationLevel, 
    &dwImp,
    sizeof(DWORD),
    &dwBytesReturned
);

if (!bRes)
{
    printf("Unable to read impersonation level\n");
    CloseHandle(hThreadTok);
    return 0;
}

switch (dwImp)
{
case SecurityAnonymous:
    printf("SecurityAnonymous\n");
    break;

case SecurityIdentification:
    printf("SecurityIdentification\n");
    break;

case SecurityImpersonation:
    printf("SecurityImpersonation\n");
    break;

case SecurityDelegation:
    printf("SecurityDelegation\n");
    break;

default:
    printf("Error. Unable to determine impersonation level\n");
    break;
}

CloseHandle(hThreadTok);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[開發 WMI 提供者](developing-a-wmi-provider.md)
</dt> <dt>

[設定命名空間安全描述項](setting-namespace-security-descriptors.md)
</dt> <dt>

[保護您的提供者](securing-your-provider.md)
</dt> </dl>

 

 
