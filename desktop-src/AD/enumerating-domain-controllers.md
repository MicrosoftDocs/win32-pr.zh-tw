---
title: 列舉網域控制站
description: 在舊版的 Windows 中，應用程式只能透過呼叫 DsGetDcName 取得網域中的單一網域控制站。
ms.assetid: bfc92777-6944-406a-8b93-949a1cf3e2c3
ms.tgt_platform: multiple
keywords:
- 列舉網域控制站 Active Directory 範例 Active Directory Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94384bb8c62edb7b0d45328dabe7765a43e4e610
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671331"
---
# <a name="enumerating-domain-controllers"></a><span data-ttu-id="9c7dd-104">列舉網域控制站</span><span class="sxs-lookup"><span data-stu-id="9c7dd-104">Enumerating Domain Controllers</span></span>

<span data-ttu-id="9c7dd-105">在舊版的 Windows 中，應用程式只能透過呼叫 [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea)取得網域中的單一網域控制站。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-105">In earlier versions of Windows, an application could only obtain a single domain controller in a domain by calling [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea).</span></span> <span data-ttu-id="9c7dd-106">沒有任何方法可以預測要抓取的網域控制站，或取得網域控制站的清單。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-106">There was no way to predict which domain controller would be retrieved or to obtain a list of the domain controllers.</span></span> <span data-ttu-id="9c7dd-107">Windows 可讓應用程式使用 [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)、 [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)和 [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) 函數來列舉網域中的網域控制站。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-107">Windows enables an application to enumerate the domain controllers in a domain by using the [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta), and [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) functions.</span></span>

<span data-ttu-id="9c7dd-108">若要列舉網域控制站，請呼叫 [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-108">To enumerate a domain controller, call [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena).</span></span> <span data-ttu-id="9c7dd-109">此函式會使用定義要列舉之網域的參數和其他列舉選項。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-109">This function takes parameters that define the domain to enumerate and other enumeration options.</span></span> <span data-ttu-id="9c7dd-110">**DsGetDcOpen** 會提供網域列舉內容控制碼，用來識別呼叫 [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) 和 [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) 時的列舉運算。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-110">**DsGetDcOpen** provides a domain enumeration context handle that is used to identify the enumeration operation when [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) and [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) are called.</span></span>

<span data-ttu-id="9c7dd-111">[**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)函式會使用網域列舉內容控制碼來呼叫，以取得列舉中的下一個網域控制站。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-111">The [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) function is called with the domain enumeration context handle to retrieve the next domain controller in the enumeration.</span></span> <span data-ttu-id="9c7dd-112">第一次呼叫此函式時，會取出列舉中的第一個網域控制站。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-112">The first time this function is called, the first domain controller in the enumeration is retrieved.</span></span> <span data-ttu-id="9c7dd-113">第二次呼叫此函式時，會取出列舉中的第二個網域控制站。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-113">The second time this function is called, the second domain controller in the enumeration is retrieved.</span></span> <span data-ttu-id="9c7dd-114">此程式會重複執行，直到 **DsGetDcNext** 傳回 **\_ 沒有 \_ 其他 \_ 專案的錯誤**，以指出列舉的結尾。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-114">This process is repeated until **DsGetDcNext** returns **ERROR\_NO\_MORE\_ITEMS**, that indicates the end of the enumeration.</span></span>

<span data-ttu-id="9c7dd-115">[**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)函式會列舉兩個群組中的網域控制站。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-115">The [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) function will enumerate the domain controllers in two groups.</span></span> <span data-ttu-id="9c7dd-116">第一個群組包含的網域控制站涵蓋執行該函式之電腦的網站，而第二個群組包含的網域控制站未涵蓋執行該函式之電腦的網站。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-116">The first group contains the domain controllers that cover the site of the computer where the function is executed and the second group contains the domain controllers that do not cover the site of the computer where the function is executed.</span></span> <span data-ttu-id="9c7dd-117">如果在 [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)的 *OptionFlags* 參數中指定了 **\_ \_ \_ 網站 \_ 記錄旗標後的 DS 通知**，則 **DsGetDcNext** 函式會傳回在抓取所有網站特定網域控制站之後偵測 **\_ \_ 到的錯誤** 標記。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-117">If the **DS\_NOTIFY\_AFTER\_SITE\_RECORDS** flag is specified in the *OptionFlags* parameter in [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), the **DsGetDcNext** function will return **ERROR\_FILEMARK\_DETECTED** after all of the site-specific domain controllers have been retrieved.</span></span> <span data-ttu-id="9c7dd-118">**DsGetDcNext** 接著會開始列舉第二個群組，其中包含網域中的所有網域控制站，包括包含在第一個群組中的網站特定網域控制站。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-118">**DsGetDcNext** will then begin enumerating the second group, which contains all domain controllers in the domain, including the site-specific domain controllers contained in the first group.</span></span>

<span data-ttu-id="9c7dd-119">處理執行函式之電腦網站的網域控制站會先列舉，後面接著未涵蓋執行該函式之電腦網站的網域控制站。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-119">Domain controllers that handle the site of the computer where the function is executed are enumerated first followed by the domain controllers that do not cover the site of the computer where the function is executed.</span></span> <span data-ttu-id="9c7dd-120">如果網域控制站設定為位於該網站，或網域控制站位於最接近網站的網站（以設定的網站間連結成本為限），則會將網域控制站視為涵蓋網站。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-120">A domain controller is said to cover a site if the domain controller is configured to reside in that site or if the domain controller resides in a site that is nearest to the site in question in terms of the configured inter-site link cost.</span></span> <span data-ttu-id="9c7dd-121">如果涵蓋的網域控制站群組中有任何網域控制站，以及未涵蓋電腦網站的網域控制站群組，則會在群組內傳回網域控制站，以設定在 DNS 中指定的優先順序和加權。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-121">If there are any domain controllers in both the group of domain controllers that cover and the group of domain controllers that do not cover the computer site, domain controllers are returned within the group in order of their configured priorities and weights that are specified in DNS.</span></span> <span data-ttu-id="9c7dd-122">具有較低數值優先順序的網域控制站會先在群組中傳回。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-122">Domain controllers that have lower numeric priority are returned within a group first.</span></span> <span data-ttu-id="9c7dd-123">如果在網站相關群組中有多個具有相同優先順序之網域控制站的子群組，則會以加權隨機順序傳回網域控制站，其中較高的網域控制站會先傳回較高的機率。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-123">If within a site-related group there is a subgroup of several domain controllers with the same priority, domain controllers are returned in a weighted random order where domain controllers with higher weight have more probability to be returned first.</span></span> <span data-ttu-id="9c7dd-124">網域系統管理員會設定網站、優先順序和權數，以在網域中的多個網域控制站之間達到有效的效能和負載平衡。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-124">The sites, priorities, and weights are configured by the domain administrator to achieve effective performance and load balancing among multiple domain controllers available in the domain.</span></span> <span data-ttu-id="9c7dd-125">因此，使用 [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)DsGetDcNext DsGetDcClose 函式的應用程式 / [](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) / [](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew)會自動利用這些優化功能。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-125">Because of this, applications that use the [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)/[**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)/[**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) functions automatically take advantage of these optimizations.</span></span>

<span data-ttu-id="9c7dd-126">當列舉已完成或不再需要時，必須藉由呼叫 [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) 和網域列舉內容控制碼來關閉列舉。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-126">When the enumeration is complete or is no longer required, the enumeration must be closed by calling [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) with the domain enumeration context handle.</span></span>

<span data-ttu-id="9c7dd-127">若要重設列舉，必須藉由呼叫 [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) 來關閉目前的列舉，然後再次呼叫 [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) 來重新開啟列舉。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-127">To reset the enumeration, it is necessary to close the current enumeration by calling [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) and then reopen the enumeration by calling [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) again.</span></span>

## <a name="example"></a><span data-ttu-id="9c7dd-128">範例</span><span class="sxs-lookup"><span data-stu-id="9c7dd-128">Example</span></span>

<span data-ttu-id="9c7dd-129">下列程式碼範例顯示如何使用這些函式來列舉本機網域中的網域控制站。</span><span class="sxs-lookup"><span data-stu-id="9c7dd-129">The following code example shows how to use these functions to enumerate the domain controllers in the local domain.</span></span>


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



 

 




