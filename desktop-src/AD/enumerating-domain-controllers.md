---
title: 列舉網域控制站
description: 在舊版 Windows 中，應用程式只能透過呼叫 DsGetDcName 取得網域中的單一網域控制站。
ms.assetid: bfc92777-6944-406a-8b93-949a1cf3e2c3
ms.tgt_platform: multiple
keywords:
- 列舉網域控制站 Active Directory 範例 Active Directory Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54234301ad843708fd4e9b20e38f2b4fd8391e1134a78cea8b0d45a001d701d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695146"
---
# <a name="enumerating-domain-controllers"></a>列舉網域控制站

在舊版 Windows 中，應用程式只能透過呼叫 [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea)取得網域中的單一網域控制站。 沒有任何方法可以預測要抓取的網域控制站，或取得網域控制站的清單。 Windows 可讓應用程式使用 [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)、 [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)和 [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew)函數來列舉網域中的網域控制站。

若要列舉網域控制站，請呼叫 [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)。 此函式會使用定義要列舉之網域的參數和其他列舉選項。 **DsGetDcOpen** 會提供網域列舉內容控制碼，用來識別呼叫 [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) 和 [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) 時的列舉運算。

[**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)函式會使用網域列舉內容控制碼來呼叫，以取得列舉中的下一個網域控制站。 第一次呼叫此函式時，會取出列舉中的第一個網域控制站。 第二次呼叫此函式時，會取出列舉中的第二個網域控制站。 此程式會重複執行，直到 **DsGetDcNext** 傳回 **\_ 沒有 \_ 其他 \_ 專案的錯誤**，以指出列舉的結尾。

[**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)函式會列舉兩個群組中的網域控制站。 第一個群組包含的網域控制站涵蓋執行該函式之電腦的網站，而第二個群組包含的網域控制站未涵蓋執行該函式之電腦的網站。 如果在 [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)的 *OptionFlags* 參數中指定了 **\_ \_ \_ 網站 \_ 記錄旗標後的 DS 通知**，則 **DsGetDcNext** 函式會傳回在抓取所有網站特定網域控制站之後偵測 **\_ \_ 到的錯誤** 標記。 **DsGetDcNext** 接著會開始列舉第二個群組，其中包含網域中的所有網域控制站，包括包含在第一個群組中的網站特定網域控制站。

處理執行函式之電腦網站的網域控制站會先列舉，後面接著未涵蓋執行該函式之電腦網站的網域控制站。 如果網域控制站設定為位於該網站，或網域控制站位於最接近網站的網站（以設定的網站間連結成本為限），則會將網域控制站視為涵蓋網站。 如果涵蓋的網域控制站群組中有任何網域控制站，以及未涵蓋電腦網站的網域控制站群組，則會在群組內傳回網域控制站，以設定在 DNS 中指定的優先順序和加權。 具有較低數值優先順序的網域控制站會先在群組中傳回。 如果在網站相關群組中有多個具有相同優先順序之網域控制站的子群組，則會以加權隨機順序傳回網域控制站，其中較高的網域控制站會先傳回較高的機率。 網域系統管理員會設定網站、優先順序和權數，以在網域中的多個網域控制站之間達到有效的效能和負載平衡。 因此，使用 [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)DsGetDcNext DsGetDcClose 函式的應用程式 / [](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) / [](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew)會自動利用這些優化功能。

當列舉已完成或不再需要時，必須藉由呼叫 [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) 和網域列舉內容控制碼來關閉列舉。

若要重設列舉，必須藉由呼叫 [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) 來關閉目前的列舉，然後再次呼叫 [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) 來重新開啟列舉。

## <a name="example"></a>範例

下列程式碼範例顯示如何使用這些函式來列舉本機網域中的網域控制站。


```C++
DWORD dwRet;
PDOMAIN_CONTROLLER_INFO pdcInfo;

// Get a domain controller for the domain this computer is on.
dwRet = DsGetDcName(NULL, NULL, NULL, NULL, 0, &pdcInfo);
if(ERROR_SUCCESS == dwRet)
{
    HANDLE hGetDc;
    
    // Open the enumeration.
    dwRet = DsGetDcOpen(    pdcInfo->DomainName,
                            DS_NOTIFY_AFTER_SITE_RECORDS,
                            NULL,
                            NULL,
                            NULL,
                            0,
                            &hGetDc);
    if(ERROR_SUCCESS == dwRet)
    {
        LPTSTR pszDnsHostName;

        /*
        Enumerate each domain controller and print its name to the 
        debug window.
        */
        while(TRUE)
        {
            ULONG ulSocketCount;
            LPSOCKET_ADDRESS rgSocketAddresses;

            dwRet = DsGetDcNext(
                hGetDc, 
                &ulSocketCount, 
                &rgSocketAddresses, 
                &pszDnsHostName);
            
            if(ERROR_SUCCESS == dwRet)
            {
                OutputDebugString(pszDnsHostName);
                OutputDebugString(TEXT("\n"));
                
                // Free the allocated string.
                NetApiBufferFree(pszDnsHostName);

                // Free the socket address array.
                LocalFree(rgSocketAddresses);
            }
            else if(ERROR_NO_MORE_ITEMS == dwRet)
            {
                // The end of the list has been reached.
                break;
            }
            else if(ERROR_FILEMARK_DETECTED == dwRet)
            {
                /*
                DS_NOTIFY_AFTER_SITE_RECORDS was specified in 
                DsGetDcOpen and the end of the site-specific 
                records was reached.
                */
                OutputDebugString(
                  TEXT("End of site-specific domain controllers\n"));
                continue;
            }
            else
            {
                // Some other error occurred.
                break;
            }
        }
        
        // Close the enumeration.
        DsGetDcClose(hGetDc);
    }
    
    // Free the DOMAIN_CONTROLLER_INFO structure. 
    NetApiBufferFree(pdcInfo);
}
```



 

 




