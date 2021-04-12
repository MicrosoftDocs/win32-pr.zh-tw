---
title: 列舉網路資源
description: 下列範例說明應用程式定義的函式 (EnumerateFunc) 列舉網路上的所有資源。
ms.assetid: f5872ee7-483d-406a-b7d8-4ce93613fd29
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2313e679746b09603d2514b418abf281fefa9bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376000"
---
# <a name="enumerating-network-resources"></a><span data-ttu-id="8ad41-103">列舉網路資源</span><span class="sxs-lookup"><span data-stu-id="8ad41-103">Enumerating Network Resources</span></span>

<span data-ttu-id="8ad41-104">下列範例說明應用程式定義的函式 (EnumerateFunc) 列舉網路上的所有資源。</span><span class="sxs-lookup"><span data-stu-id="8ad41-104">The following example illustrates an application-defined function (EnumerateFunc) that enumerates all the resources on a network.</span></span> <span data-ttu-id="8ad41-105">此範例會針對 [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea)結構的指標指定 **Null** ，因為當 [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma)收到 **Null** 指標時，它會抓取網路根目錄的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8ad41-105">The sample specifies **NULL** for the pointer to the [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure because when [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) receives a **NULL** pointer, it retrieves a handle to the root of the network.</span></span>

<span data-ttu-id="8ad41-106">若要開始列舉網路容器資源，您的應用程式應該執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="8ad41-106">To begin the enumeration of a network container resource, your application should perform the following steps:</span></span>

1.  <span data-ttu-id="8ad41-107">將代表資源的 [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) 結構位址傳遞至 [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) 函數。</span><span class="sxs-lookup"><span data-stu-id="8ad41-107">Pass the address of a [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure that represents the resource to the [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) function.</span></span>
2.  <span data-ttu-id="8ad41-108">配置夠大的緩衝區來保存 [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)函式所傳回的 [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea)結構陣列，以及其成員指向的字串。</span><span class="sxs-lookup"><span data-stu-id="8ad41-108">Allocate a buffer large enough to hold the array of [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structures that the [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) function returns, plus the strings to which their members point.</span></span>
3.  <span data-ttu-id="8ad41-109">將 [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) 傳回的資源控制碼傳遞至 [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) 函數。</span><span class="sxs-lookup"><span data-stu-id="8ad41-109">Pass the resource handle returned by [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) to the [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) function.</span></span>
4.  <span data-ttu-id="8ad41-110">呼叫 [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) 函數，關閉不再需要的資源控制碼。</span><span class="sxs-lookup"><span data-stu-id="8ad41-110">Close the resource handle when it is no longer needed by calling the [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) function.</span></span>

<span data-ttu-id="8ad41-111">您可以繼續列舉 [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)所抓取的 [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea)結構陣列中所述的容器資源。</span><span class="sxs-lookup"><span data-stu-id="8ad41-111">You can continue enumerating a container resource described in the array of [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structures retrieved by [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea).</span></span> <span data-ttu-id="8ad41-112">如果 **NETRESOURCE** 結構的 **DWUSAGE** 成員等於 RESOURCEUSAGE \_ 容器，請將結構的位址傳遞至 [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma)函式，以開啟容器並繼續列舉。</span><span class="sxs-lookup"><span data-stu-id="8ad41-112">If the **dwUsage** member of the **NETRESOURCE** structure is equal to RESOURCEUSAGE\_CONTAINER, pass the address of the structure to the [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) function to open the container and continue the enumeration.</span></span> <span data-ttu-id="8ad41-113">如果 **dwUsage** 等於 RESOURCEUSAGE 可 \_ 連接，則應用程式可以將結構的位址傳遞至 [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) 函式或 [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) 函式，以連線至資源。</span><span class="sxs-lookup"><span data-stu-id="8ad41-113">If **dwUsage** is equal to RESOURCEUSAGE\_CONNECTABLE, the application can pass the structure's address to the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) function or the [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) function to connect to the resource.</span></span>

<span data-ttu-id="8ad41-114">首先，範例會呼叫 [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) 函數來開始列舉。</span><span class="sxs-lookup"><span data-stu-id="8ad41-114">First the sample calls the [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) function to begin the enumeration.</span></span> <span data-ttu-id="8ad41-115">此範例會呼叫 [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) 函式來配置所需的緩衝區，然後呼叫 [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) 函數將緩衝區內容設定為零。</span><span class="sxs-lookup"><span data-stu-id="8ad41-115">The sample calls the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function to allocate the required buffer, and then calls the [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) function to set the buffer contents to zero.</span></span> <span data-ttu-id="8ad41-116">然後，此範例會呼叫 [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) 函數以繼續列舉。</span><span class="sxs-lookup"><span data-stu-id="8ad41-116">Then the sample calls the [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) function to continue the enumeration.</span></span> <span data-ttu-id="8ad41-117">每當 **WNetEnumResource** 所抓取之 [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea)結構的 **dwUsage** 成員等於 RESOURCEUSAGE 容器時，EnumerateFunc 函式就會 \_ 以遞迴方式呼叫本身，並在其對 **WNetOpenEnum** 的呼叫中使用該結構的指標。</span><span class="sxs-lookup"><span data-stu-id="8ad41-117">Whenever the **dwUsage** member of a [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure retrieved by **WNetEnumResource** is equal to RESOURCEUSAGE\_CONTAINER, the EnumerateFunc function calls itself recursively and uses a pointer to that structure in its call to **WNetOpenEnum**.</span></span> <span data-ttu-id="8ad41-118">最後，此範例會呼叫 [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) 函式來釋放已配置的記憶體，並呼叫 [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) 來結束列舉。</span><span class="sxs-lookup"><span data-stu-id="8ad41-118">Finally, the sample calls the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function to free the allocated memory, and the [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) to end the enumeration.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "mpr.lib")

#include <windows.h>
#include <stdio.h>
#include <winnetwk.h>

BOOL WINAPI EnumerateFunc(LPNETRESOURCE lpnr);
void DisplayStruct(int i, LPNETRESOURCE lpnrLocal);

int main()
{

    LPNETRESOURCE lpnr = NULL;

    if (EnumerateFunc(lpnr) == FALSE) {
        printf("Call to EnumerateFunc failed\n");
        return 1;
    } else
        return 0;

}

BOOL WINAPI EnumerateFunc(LPNETRESOURCE lpnr)
{
    DWORD dwResult, dwResultEnum;
    HANDLE hEnum;
    DWORD cbBuffer = 16384;     // 16K is a good size
    DWORD cEntries = -1;        // enumerate all possible entries
    LPNETRESOURCE lpnrLocal;    // pointer to enumerated structures
    DWORD i;
    //
    // Call the WNetOpenEnum function to begin the enumeration.
    //
    dwResult = WNetOpenEnum(RESOURCE_GLOBALNET, // all network resources
                            RESOURCETYPE_ANY,   // all resources
                            0,  // enumerate all resources
                            lpnr,       // NULL first time the function is called
                            &hEnum);    // handle to the resource

    if (dwResult != NO_ERROR) {
        printf("WnetOpenEnum failed with error %d\n", dwResult);
        return FALSE;
    }
    //
    // Call the GlobalAlloc function to allocate resources.
    //
    lpnrLocal = (LPNETRESOURCE) GlobalAlloc(GPTR, cbBuffer);
    if (lpnrLocal == NULL) {
        printf("WnetOpenEnum failed with error %d\n", dwResult);
//      NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetOpenEnum");
        return FALSE;
    }

    do {
        //
        // Initialize the buffer.
        //
        ZeroMemory(lpnrLocal, cbBuffer);
        //
        // Call the WNetEnumResource function to continue
        //  the enumeration.
        //
        dwResultEnum = WNetEnumResource(hEnum,  // resource handle
                                        &cEntries,      // defined locally as -1
                                        lpnrLocal,      // LPNETRESOURCE
                                        &cbBuffer);     // buffer size
        //
        // If the call succeeds, loop through the structures.
        //
        if (dwResultEnum == NO_ERROR) {
            for (i = 0; i < cEntries; i++) {
                // Call an application-defined function to
                //  display the contents of the NETRESOURCE structures.
                //
                DisplayStruct(i, &lpnrLocal[i]);

                // If the NETRESOURCE structure represents a container resource, 
                //  call the EnumerateFunc function recursively.

                if (RESOURCEUSAGE_CONTAINER == (lpnrLocal[i].dwUsage
                                                & RESOURCEUSAGE_CONTAINER))
//          if(!EnumerateFunc(hwnd, hdc, &lpnrLocal[i]))
                    if (!EnumerateFunc(&lpnrLocal[i]))
                        printf("EnumerateFunc returned FALSE\n");
//            TextOut(hdc, 10, 10, "EnumerateFunc returned FALSE.", 29);
            }
        }
        // Process errors.
        //
        else if (dwResultEnum != ERROR_NO_MORE_ITEMS) {
            printf("WNetEnumResource failed with error %d\n", dwResultEnum);

//      NetErrorHandler(hwnd, dwResultEnum, (LPSTR)"WNetEnumResource");
            break;
        }
    }
    //
    // End do.
    //
    while (dwResultEnum != ERROR_NO_MORE_ITEMS);
    //
    // Call the GlobalFree function to free the memory.
    //
    GlobalFree((HGLOBAL) lpnrLocal);
    //
    // Call WNetCloseEnum to end the enumeration.
    //
    dwResult = WNetCloseEnum(hEnum);

    if (dwResult != NO_ERROR) {
        //
        // Process errors.
        //
        printf("WNetCloseEnum failed with error %d\n", dwResult);
//    NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetCloseEnum");
        return FALSE;
    }

    return TRUE;
}

void DisplayStruct(int i, LPNETRESOURCE lpnrLocal)
{
    printf("NETRESOURCE[%d] Scope: ", i);
    switch (lpnrLocal->dwScope) {
    case (RESOURCE_CONNECTED):
        printf("connected\n");
        break;
    case (RESOURCE_GLOBALNET):
        printf("all resources\n");
        break;
    case (RESOURCE_REMEMBERED):
        printf("remembered\n");
        break;
    default:
        printf("unknown scope %d\n", lpnrLocal->dwScope);
        break;
    }

    printf("NETRESOURCE[%d] Type: ", i);
    switch (lpnrLocal->dwType) {
    case (RESOURCETYPE_ANY):
        printf("any\n");
        break;
    case (RESOURCETYPE_DISK):
        printf("disk\n");
        break;
    case (RESOURCETYPE_PRINT):
        printf("print\n");
        break;
    default:
        printf("unknown type %d\n", lpnrLocal->dwType);
        break;
    }

    printf("NETRESOURCE[%d] DisplayType: ", i);
    switch (lpnrLocal->dwDisplayType) {
    case (RESOURCEDISPLAYTYPE_GENERIC):
        printf("generic\n");
        break;
    case (RESOURCEDISPLAYTYPE_DOMAIN):
        printf("domain\n");
        break;
    case (RESOURCEDISPLAYTYPE_SERVER):
        printf("server\n");
        break;
    case (RESOURCEDISPLAYTYPE_SHARE):
        printf("share\n");
        break;
    case (RESOURCEDISPLAYTYPE_FILE):
        printf("file\n");
        break;
    case (RESOURCEDISPLAYTYPE_GROUP):
        printf("group\n");
        break;
    case (RESOURCEDISPLAYTYPE_NETWORK):
        printf("network\n");
        break;
    default:
        printf("unknown display type %d\n", lpnrLocal->dwDisplayType);
        break;
    }

    printf("NETRESOURCE[%d] Usage: 0x%x = ", i, lpnrLocal->dwUsage);
    if (lpnrLocal->dwUsage & RESOURCEUSAGE_CONNECTABLE)
        printf("connectable ");
    if (lpnrLocal->dwUsage & RESOURCEUSAGE_CONTAINER)
        printf("container ");
    printf("\n");

    printf("NETRESOURCE[%d] Localname: %S\n", i, lpnrLocal->lpLocalName);
    printf("NETRESOURCE[%d] Remotename: %S\n", i, lpnrLocal->lpRemoteName);
    printf("NETRESOURCE[%d] Comment: %S\n", i, lpnrLocal->lpComment);
    printf("NETRESOURCE[%d] Provider: %S\n", i, lpnrLocal->lpProvider);
    printf("\n");
}

```



<span data-ttu-id="8ad41-119">如需使用應用程式定義錯誤處理常式的詳細資訊，請參閱抓取 [網路錯誤](retrieving-network-errors.md)。</span><span class="sxs-lookup"><span data-stu-id="8ad41-119">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 