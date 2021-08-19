---
title: Teredo 的必要防火牆例外
description: 若要讓應用程式接收 Teredo 流量，必須允許應用程式接收主機防火牆中的 IPv6 流量，且需要應用程式將通訊端選項 [IPV6 保護等級] 設定為 [不 \_ \_ \_ 受保護等級] \_ 。
ms.assetid: 2fc74d86-9696-4ba9-adbe-e5558ae7d7c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a67d7de38ed91de7d8d8afeada6fe9705ff55f2af1b726ed5c5d49b271464dc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354441"
---
# <a name="required-firewall-exceptions-for-teredo"></a>Teredo 的必要防火牆例外

若要讓應用程式接收 Teredo 流量，必須允許應用程式接收主機防火牆中的 IPv6 流量，且需要應用程式將通訊端選項 [ [IPv6 \_ 保護 \_ 等級](/windows/desktop/WinSock/ipv6-protection-level) ] 設定為 [不 \_ 受保護等級] \_ 。 若要啟用這種類型的案例，必須執行本檔中詳述的防火牆例外。

需要下列防火牆設定，以確保防火牆與 Teredo 之間的互通性：

-   用戶端防火牆必須允許解析 teredo.ipv6.microsoft.com。
-   必須開啟 UDP 埠3544，以確保 Teredo 用戶端可以成功與 Teredo 伺服器通訊。
-   防火牆必須藉由呼叫 [**FwpmSystemPortsGet0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsystemportsget0) 函式，在本機電腦上取得 Teredo 服務所使用的動態 UDP 埠;相關埠的類型為 FWPM \_ 系統 \_ 埠 \_ TEREDO。 應該實 **FwpmSystemPortsGet0** 函式來取代現在已淘汰的 [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport) 或 [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange) 函數。
-   防火牆允許系統在本機子網上傳送和接收 UDP/IPv4 封包至 UDP 埠1900，因為這可讓 UPnP 探索流量流動，並有可能改善連線速度。
    > [!Note]  
    > 如果不符合這種情況，就會導入與特定 NAT 類型之間通訊相關之相容性問題的情況。尤其是在對稱式 Nat 和受限式 Nat 之間。 雖然對稱式 Nat 很受熱點限制，而受限式 Nat 在家庭中很普遍，但兩者之間的通訊在受限式 NAT 的端可能會發生錯誤。

     

-   必須啟用連入和連出的 ICMPv6 「回顯要求」和「回應回復」例外狀況。 這些例外狀況是確保 Teredo 用戶端可以作為 Teredo 主機特定轉送的必要項。 Teredo 主機特定轉送可由其他原生 IPv6 位址或 Teredo 位址提供的6to4 位址來識別。

用戶端防火牆必須支援下列每個 RFC 4443 的 ICMPv6 錯誤訊息和探索功能：



| 程式碼    | 描述                                    |
|---------|------------------------------------------------|
| 135/136 | ICMPV6 鄰居請求和公告 |
| 133/134 | 路由器請求和公告          |
| 128/129 | ICMPV6 Echo 要求和回復                  |
| 1       | 目的地無法連線                        |
| 2       | 封包太大                               |
| 3       | 超過時間                                  |
| 4       | 不正確參數                              |



 

如果無法明確允許這些訊息，則應該在防火牆上啟用所有 ICMPv6 訊息的豁免。 此外，主機防火牆可能會注意到，由代碼135/136 或133/134 分類的封包源自于使用者模式服務 **iphlpsvc** ，而不是從堆疊。 主機防火牆不能卸載這些封包。 Teredo 服務主要是在「使用者模式」 IP Helper 服務內執行。

使用 [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) Windows 防火牆 API 來列舉已設定 Edge 遍歷旗標的所有規則，所有想要接聽未要求流量的應用程式都會列舉防火牆例外狀況。 有關使用 Edge 遍歷選項的特定資訊，詳細說明如何透過 [Teredo 接收未經](receiving-unsolicited-traffic-over-teredo.md)要求的流量。

回呼未與下列範例列舉程式碼相關聯;強烈建議協力廠商防火牆定期執行列舉，或每次防火牆偵測到嘗試通過防火牆的新應用程式。


```C++
#include <windows.h>
#include <objbase.h>
#include <stdio.h>
#include <atlcomcli.h>
#include <strsafe.h>
#include <netfw.h>

#define NET_FW_IP_PROTOCOL_TCP_NAME L"TCP"
#define NET_FW_IP_PROTOCOL_UDP_NAME L"UDP"

#define NET_FW_RULE_DIR_IN_NAME L"In"
#define NET_FW_RULE_DIR_OUT_NAME L"Out"

#define NET_FW_RULE_ACTION_BLOCK_NAME L"Block"
#define NET_FW_RULE_ACTION_ALLOW_NAME L"Allow"

#define NET_FW_RULE_ENABLE_IN_NAME L"TRUE"
#define NET_FW_RULE_DISABLE_IN_NAME L"FALSE"

#import "netfw.tlb"

void DumpFWRulesInCollection(long Allprofiletypes, NetFwPublicTypeLib::INetFwRulePtr FwRule)
{
    variant_t InterfaceArray;
    variant_t InterfaceString;    

    if(FwRule->Profiles == Allprofiletypes)
    {
        wprintf(L"---------------------------------------------\n");
        wprintf(L"Name:             %s\n", (BSTR)FwRule->Name);        
        wprintf(L"Description:      %s\n", (BSTR)FwRule->Description);
        wprintf(L"Application Name: %s\n", (BSTR)FwRule->ApplicationName);
        wprintf(L"Service Name:     %s\n", (BSTR)FwRule->serviceName);

        switch(FwRule->Protocol)
        {
        case NET_FW_IP_PROTOCOL_TCP: wprintf(L"IP Protocol:      %s\n", NET_FW_IP_PROTOCOL_TCP_NAME);
            break;
        case NET_FW_IP_PROTOCOL_UDP: wprintf(L"IP Protocol:      %s\n", NET_FW_IP_PROTOCOL_UDP_NAME);
            break;
        default:
            break;
        }

        if(FwRule->Protocol != NET_FW_IP_VERSION_V4 && FwRule->Protocol != NET_FW_IP_VERSION_V6)
        {
            wprintf(L"Local Ports:      %s\n", (BSTR)FwRule->LocalPorts);
            wprintf(L"Remote Ports:     %s\n", (BSTR)FwRule->RemotePorts);
        }
        
        wprintf(L"LocalAddresses:   %s\n", (BSTR)FwRule->LocalAddresses);
        wprintf(L"RemoteAddresses:  %s\n", (BSTR)FwRule->RemoteAddresses);
        wprintf(L"Profile:          %d\n", Allprofiletypes);
        

        if(FwRule->Protocol == NET_FW_IP_VERSION_V4 || FwRule->Protocol == NET_FW_IP_VERSION_V6)
        {
            wprintf(L"ICMP TypeCode:    %s\n", (BSTR)FwRule->IcmpTypesAndCodes);
        }

        switch(FwRule->Direction)
        {
        case NET_FW_RULE_DIR_IN:
            wprintf(L"Direction:        %s\n", NET_FW_RULE_DIR_IN_NAME);
            break;
        case NET_FW_RULE_DIR_OUT:
            wprintf(L"Direction:        %s\n", NET_FW_RULE_DIR_OUT_NAME);
            break;
        default:
            break;
        }

        switch(FwRule->Action)
        {
        case NET_FW_ACTION_BLOCK:
            wprintf(L"Action:           %s\n", NET_FW_RULE_ACTION_BLOCK_NAME);
            break;
        case NET_FW_ACTION_ALLOW:
            wprintf(L"Action:           %s\n", NET_FW_RULE_ACTION_ALLOW_NAME);
            break;
        default:
            break;
        }
        
        InterfaceArray = FwRule->Interfaces;

        if(InterfaceArray.vt != VT_EMPTY)
        {
            SAFEARRAY    *pSa = NULL;
            long index = 0;

            pSa = InterfaceArray.parray;

            for(long index= pSa->rgsabound->lLbound; index < (long)pSa->rgsabound->cElements; index++)
            {
                SafeArrayGetElement(pSa, &index, &InterfaceString);
                wprintf(L"Interfaces:       %s\n", (BSTR)InterfaceString.bstrVal);
            }
        }
        wprintf(L"Interface Types:  %s\n", (BSTR)FwRule->InterfaceTypes);
        if(FwRule->Enabled)
        {
            wprintf(L"Enabled:          %s\n", NET_FW_RULE_ENABLE_IN_NAME);
        }
        else
        {
            wprintf(L"Enabled:          %s\n", NET_FW_RULE_DISABLE_IN_NAME);
        }
        wprintf(L"Grouping:         %s\n", (BSTR)FwRule->Grouping);
        wprintf(L"Edge:             %s\n", (BSTR)FwRule->EdgeTraversal);
    }
}

int __cdecl main()
{
    HRESULT hr;
    BOOL fComInitialized = FALSE;
    ULONG cFetched = 0; 
    CComVariant var;
    long Allprofiletypes = 0;

    try
    {
        IUnknownPtr pEnumerator = NULL;
        IEnumVARIANT* pVariant = NULL;
        NetFwPublicTypeLib::INetFwPolicy2Ptr sipFwPolicy2;

        //
        // Initialize the COM library on the current thread.
        //
        hr = CoInitialize(NULL);
        if (FAILED(hr))
        {
            _com_issue_error(hr);
        }
        fComInitialized = TRUE;
        
        hr = sipFwPolicy2.CreateInstance("HNetCfg.FwPolicy2");
        if (FAILED(hr))
        {
            _com_issue_error(hr);
        }
        Allprofiletypes = NET_FW_PROFILE2_ALL; // 0x7FFFFFFF
        
        printf("The number of rules in the Windows Firewall are %d\n", sipFwPolicy2->Rules->Count);

        pEnumerator = sipFwPolicy2->Rules->Get_NewEnum();

        if(pEnumerator)
        {
            hr = pEnumerator->QueryInterface(__uuidof(IEnumVARIANT), (void **) &pVariant);
        }

        while(SUCCEEDED(hr) && hr != S_FALSE)
        {        
            NetFwPublicTypeLib::INetFwRulePtr sipFwRule;

            var.Clear();
            hr = pVariant->Next(1, &var, &cFetched);
            if (S_FALSE != hr)
            {
                if (SUCCEEDED(hr))
                {
                    hr = var.ChangeType(VT_DISPATCH);
                }
                if (SUCCEEDED(hr))
                {
                    hr = (V_DISPATCH(&var))->QueryInterface(__uuidof(INetFwRule), reinterpret_cast<void**>(&sipFwRule));
                }

                if (SUCCEEDED(hr))
                {
                    DumpFWRulesInCollection(Allprofiletypes, sipFwRule);
                }
            }
        }
    }
    catch(_com_error& e)
    {
        printf ("Error. HRESULT message is: %s (0x%08lx)\n", e.ErrorMessage(), e.Error());
        if (e.ErrorInfo())
        {
            printf ("Description: %s\n", (char *)e.Description());
        }
    }
    if (fComInitialized)
    {
        CoUninitialize();
    }
    return 0;
}

```



 

 