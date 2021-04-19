---
title: 建立狀態回呼函數
description: 本教學課程說明如何建立狀態回呼函式，以用來監視網際網路要求的狀態。
ms.assetid: 518d0800-5ea6-4327-8459-901e6d9a8a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e46040d9b6f93645e2730af287a1955343ec3a
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "106967300"
---
# <a name="creating-status-callback-functions"></a><span data-ttu-id="90a00-103">建立狀態回呼函數</span><span class="sxs-lookup"><span data-stu-id="90a00-103">Creating Status Callback Functions</span></span>

<span data-ttu-id="90a00-104">本教學課程說明如何建立狀態回呼函式，以用來監視網際網路要求的狀態。</span><span class="sxs-lookup"><span data-stu-id="90a00-104">This tutorial describes how to create a status callback function used to monitor the status of an Internet request.</span></span>

<span data-ttu-id="90a00-105">狀態回呼函式會在源自任何傳遞非零內容值之 WinINet 函式的網際網路要求上接收狀態回呼。</span><span class="sxs-lookup"><span data-stu-id="90a00-105">Status callback functions receive status callbacks on any Internet requests that originated from any WinINet function that was passed a nonzero context value.</span></span>


<span data-ttu-id="90a00-106">以下是建立狀態回呼函式的必要步驟：</span><span class="sxs-lookup"><span data-stu-id="90a00-106">The following steps are necessary for creating a status callback function:</span></span>

1.  [<span data-ttu-id="90a00-107">定義內容值。</span><span class="sxs-lookup"><span data-stu-id="90a00-107">Define the context value.</span></span>](#defining-the-context-value)
2.  [<span data-ttu-id="90a00-108">建立狀態回呼函數。</span><span class="sxs-lookup"><span data-stu-id="90a00-108">Create the status callback function.</span></span>](#creating-status-callback-functions)

### <a name="defining-the-context-value"></a><span data-ttu-id="90a00-109">定義內容值</span><span class="sxs-lookup"><span data-stu-id="90a00-109">Defining the Context Value</span></span>

<span data-ttu-id="90a00-110">內容值可以是任何不帶正負號的長整數值。</span><span class="sxs-lookup"><span data-stu-id="90a00-110">The context value can be any unsigned long integer value.</span></span> <span data-ttu-id="90a00-111">在理想情況下，內容值應該識別剛完成的要求，以及任何相關聯資源的位置（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="90a00-111">Ideally, the context value should identify what request has just been completed and the location of any associated resources, if needed.</span></span>

<span data-ttu-id="90a00-112">使用內容值最有用的方式之一，就是傳遞結構的位址，並將它轉換成 **DWORD \_ 指標**。</span><span class="sxs-lookup"><span data-stu-id="90a00-112">One of the most useful ways to use the context value is to pass the address of a structure and cast it to a **DWORD\_PTR**.</span></span> <span data-ttu-id="90a00-113">您可以使用此結構來儲存要求的相關資訊，以便將其傳遞至狀態回呼函數。</span><span class="sxs-lookup"><span data-stu-id="90a00-113">The structure can be used to store information about the request, so that it is passed to the status callback function.</span></span>

<span data-ttu-id="90a00-114">下列結構是可能的內容值範例。</span><span class="sxs-lookup"><span data-stu-id="90a00-114">The following structure is an example of a possible context value.</span></span> <span data-ttu-id="90a00-115">考慮使用 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 函式來選擇結構的成員。</span><span class="sxs-lookup"><span data-stu-id="90a00-115">The members of the structure are chosen with the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function in mind.</span></span>


```C++
typedef struct{
    HWND       hWindow;      // Window handle
    int        nStatusList;  // List box control to hold callbacks
    HINTERNET  hResource;    // HINTERNET handle created by InternetOpenUrl
    char       szMemo[512];  // String to store status memo
} REQUEST_CONTEXT;
```



<span data-ttu-id="90a00-116">在此範例中，狀態回呼函式可以存取視窗控制碼，讓它能夠顯示使用者介面。</span><span class="sxs-lookup"><span data-stu-id="90a00-116">In this example, the status callback function would have access to the window handle, which would allow it to display a user interface.</span></span> <span data-ttu-id="90a00-117">[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)建立的 [**HINTERNET**](appendix-a-hinternet-handles.md)控制碼可傳遞至另一個函式，該函式可下載資源和可用來傳遞要求相關資訊的字元陣列。</span><span class="sxs-lookup"><span data-stu-id="90a00-117">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) could be passed to another function that can download the resource and an array of characters that can be used to pass information about the request.</span></span>

<span data-ttu-id="90a00-118">結構的成員可以變更為符合特定應用程式的需求，因此在此範例中不受限制。</span><span class="sxs-lookup"><span data-stu-id="90a00-118">The members of the structure can be changed to fit the needs of a particular application, so do not feel constrained by this example.</span></span>

### <a name="creating-the-status-callback-function"></a><span data-ttu-id="90a00-119">建立狀態回呼函數</span><span class="sxs-lookup"><span data-stu-id="90a00-119">Creating the Status Callback Function</span></span>

<span data-ttu-id="90a00-120">狀態回呼函數必須遵循 [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback)的格式。</span><span class="sxs-lookup"><span data-stu-id="90a00-120">The status callback function must follow the format of [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).</span></span> <span data-ttu-id="90a00-121">若要這樣做：</span><span class="sxs-lookup"><span data-stu-id="90a00-121">To do this:</span></span>

1.  <span data-ttu-id="90a00-122">為您的狀態回呼函數撰寫函式宣告。</span><span class="sxs-lookup"><span data-stu-id="90a00-122">Write a function declaration for your status callback function.</span></span>

    <span data-ttu-id="90a00-123">下列範例顯示範例宣告。</span><span class="sxs-lookup"><span data-stu-id="90a00-123">The following example shows a sample declaration.</span></span>

    ```C++
    void CALLBACK CallMaster( HINTERNET,
                              DWORD_PTR,
                              DWORD,
                              LPVOID,
                              DWORD );
    ```

    

2.  <span data-ttu-id="90a00-124">判斷您的狀態回呼函式會有什麼作用。</span><span class="sxs-lookup"><span data-stu-id="90a00-124">Determine what your status callback function will do.</span></span> <span data-ttu-id="90a00-125">針對正在進行非同步呼叫的應用程式，狀態回呼函式必須處理 [網際網路 \_ 狀態 \_ 要求完成] \_ 值，表示非同步要求已完成。</span><span class="sxs-lookup"><span data-stu-id="90a00-125">For applications that are making asynchronous calls, the status callback function must handle the INTERNET\_STATUS\_REQUEST\_COMPLETE value, which indicates an asynchronous request is complete.</span></span> <span data-ttu-id="90a00-126">狀態回呼函數也可以用來追蹤網際網路要求的進度。</span><span class="sxs-lookup"><span data-stu-id="90a00-126">The status callback function can also be used to track the progress of an Internet request.</span></span>

    <span data-ttu-id="90a00-127">一般而言，最好使用 switch 語句搭配 *dwInternetStatus* 做為參數值，並使用 case 語句的狀態值。</span><span class="sxs-lookup"><span data-stu-id="90a00-127">In general, it works best to use a switch statement with *dwInternetStatus* as the switch value and the status values for the case statements.</span></span> <span data-ttu-id="90a00-128">根據您的應用程式所呼叫的函式類型而定，您可以忽略某些狀態值。</span><span class="sxs-lookup"><span data-stu-id="90a00-128">Depending on the types of functions your application is calling, you can ignore some of the status values.</span></span> <span data-ttu-id="90a00-129">如需不同狀態值的定義，請參閱 [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback)的 *dwInternetStatus* 參數底下的清單。</span><span class="sxs-lookup"><span data-stu-id="90a00-129">For a definition of the different status values, see the listing under the *dwInternetStatus* parameter of [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).</span></span>

    <span data-ttu-id="90a00-130">下列 switch 語句是如何處理狀態回呼的範例。</span><span class="sxs-lookup"><span data-stu-id="90a00-130">The following switch statement is an example of how to handle status callbacks.</span></span>

    ``` syntax
    switch (dwInternetStatus)
    {
        case INTERNET_STATUS_REQUEST_COMPLETE:
            // Add code
            break;
        default:
            // Add code
            break;
    }
    ```

3.  <span data-ttu-id="90a00-131">建立程式碼來處理狀態值。</span><span class="sxs-lookup"><span data-stu-id="90a00-131">Create the code to handle the status values.</span></span>

    <span data-ttu-id="90a00-132">處理每個狀態值的程式碼，主要取決於您要使用的狀態回呼函數。</span><span class="sxs-lookup"><span data-stu-id="90a00-132">The code to handle each of the status values depends heavily on your intended use of the status callback function.</span></span> <span data-ttu-id="90a00-133">針對只追蹤要求進度的應用程式，您可能只需要將字串寫入清單方塊。</span><span class="sxs-lookup"><span data-stu-id="90a00-133">For applications that are just tracking the progress of a request, writing a string to a list box might be all you need.</span></span> <span data-ttu-id="90a00-134">針對非同步作業，程式碼必須處理回呼中傳回的部分資料。</span><span class="sxs-lookup"><span data-stu-id="90a00-134">For asynchronous operations, the code must handle some of the data returned in the callback.</span></span>

    <span data-ttu-id="90a00-135">下列狀態回呼函式會使用 switch 函式來決定狀態值是什麼，並建立字串，其中包含狀態值的名稱和先前呼叫的函式，該函式會儲存在要求內容結構的 szMemo 成員中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="90a00-135">The following status callback function uses a switch function to determine what the status value is and creates a string that includes the name of the status value and the previous function called, which is stored in the szMemo member of the REQUEST\_CONTEXT structure.</span></span>

    ```C++
    void __stdcall CallMaster(
        HINTERNET hInternet,
        DWORD_PTR dwContext,
        DWORD dwInternetStatus,
        LPVOID lpvStatusInformation,
        DWORD dwStatusInformationLength
    )
    {
        UNREFERENCED_PARAMETER(hInternet);
        UNREFERENCED_PARAMETER(lpvStatusInformation);
        UNREFERENCED_PARAMETER(dwStatusInformationLength);

        REQUEST_CONTEXT *cpContext;
        cpContext = (REQUEST_CONTEXT*)dwContext;
        char szStatusText[80];

        switch (dwInternetStatus)
        {
            case INTERNET_STATUS_CLOSING_CONNECTION:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CLOSING_CONNECTION",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_CONNECTED_TO_SERVER:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTED_TO_SERVER",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_CONNECTING_TO_SERVER:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTING_TO_SERVER",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_CONNECTION_CLOSED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTION_CLOSED",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_HANDLE_CLOSING:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s HANDLE_CLOSING",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_HANDLE_CREATED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s HANDLE_CREATED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_INTERMEDIATE_RESPONSE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s INTERMEDIATE_RESPONSE",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_NAME_RESOLVED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s NAME_RESOLVED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RECEIVING_RESPONSE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RECEIVING_RESPONSE",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RESPONSE_RECEIVED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RESPONSE_RECEIVED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_REDIRECT:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REDIRECT",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_REQUEST_COMPLETE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REQUEST_COMPLETE",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_REQUEST_SENT:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REQUEST_SENT",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RESOLVING_NAME:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RESOLVING_NAME",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_SENDING_REQUEST:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s SENDING_REQUEST",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_STATE_CHANGE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s STATE_CHANGE",
                                  cpContext->szMemo );
                break;
            default:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s Unknown Status %d Given",
                                  cpContext->szMemo,
                                  dwInternetStatus);
                break;
        }

        SendDlgItemMessage( cpContext->hWindow,
                          cpContext->nStatusList,
                          LB_ADDSTRING,
                          0, (LPARAM)szStatusText );

    }
    ```

    

4.  <span data-ttu-id="90a00-136">您可以使用 [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) 函式，在您要接收其狀態回呼的 [**HINTERNET**](appendix-a-hinternet-handles.md) 控制碼上設定狀態回呼函數。</span><span class="sxs-lookup"><span data-stu-id="90a00-136">Use the [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) function to set the status callback function on the [**HINTERNET**](appendix-a-hinternet-handles.md) handle for which you want to receive status callbacks.</span></span>

    <span data-ttu-id="90a00-137">下列範例示範如何設定狀態回呼函數。</span><span class="sxs-lookup"><span data-stu-id="90a00-137">The following example demonstrates how to set a status callback function.</span></span>

    ```C++
    HINTERNET hOpen;                       // Root HINTERNET handle
    INTERNET_STATUS_CALLBACK iscCallback;  // Holds the callback function

    // Create the root HINTERNET handle.
    hOpen = InternetOpen( TEXT("Test Application"),
                          INTERNET_OPEN_TYPE_PRECONFIG,
                          NULL, NULL, 0);

    // Set the status callback function.
    iscCallback = InternetSetStatusCallback( hOpen, (INTERNET_STATUS_CALLBACK)CallMaster );
    ```

    

> [!Note]  
> <span data-ttu-id="90a00-138">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="90a00-138">WinINet does not support server implementations.</span></span> <span data-ttu-id="90a00-139">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="90a00-139">In addition, it should not be used from a service.</span></span> <span data-ttu-id="90a00-140">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="90a00-140">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="90a00-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="90a00-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90a00-142">建立狀態回呼函數</span><span class="sxs-lookup"><span data-stu-id="90a00-142">Creating Status Callback Functions</span></span>](creating-status-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="90a00-143">**InternetSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="90a00-143">**InternetSetStatusCallback**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)
</dt> <dt>

[<span data-ttu-id="90a00-144">*InternetStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="90a00-144">*InternetStatusCallback*</span></span>](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback)
</dt> </dl>

 

 