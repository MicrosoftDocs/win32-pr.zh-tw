---
title: 尋找伺服器主機系統
description: 藉由使用字串系結和查詢名稱服務資料庫來尋找伺服器程式的位置，來尋找伺服器主機系統。
ms.assetid: 4aadda88-2109-481f-aa4b-b1983d81dec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2357fcafa35d4f64cfb4f6841c0b56e1e94b7aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840183"
---
# <a name="finding-server-host-systems"></a><span data-ttu-id="99fce-103">尋找伺服器主機系統</span><span class="sxs-lookup"><span data-stu-id="99fce-103">Finding Server Host Systems</span></span>

<span data-ttu-id="99fce-104">伺服器主機系統是執行分散式應用程式之伺服器程式的電腦。</span><span class="sxs-lookup"><span data-stu-id="99fce-104">A server host system is the computer that executes the distributed application's server program.</span></span> <span data-ttu-id="99fce-105">網路上可能有一或多個伺服器主機系統。</span><span class="sxs-lookup"><span data-stu-id="99fce-105">There may be one or many server host systems on a network.</span></span> <span data-ttu-id="99fce-106">用戶端程式如何尋找要連接的伺服器，取決於您的程式需求。</span><span class="sxs-lookup"><span data-stu-id="99fce-106">How your client program finds a server to connect to depends on the needs of your program.</span></span>

<span data-ttu-id="99fce-107">有兩種方法可以尋找伺服器主機系統：</span><span class="sxs-lookup"><span data-stu-id="99fce-107">There are two methods of finding server host systems:</span></span>

-   <span data-ttu-id="99fce-108">使用儲存在用戶端原始程式碼、環境變數或應用程式特定設定檔中字串的資訊。</span><span class="sxs-lookup"><span data-stu-id="99fce-108">Using information stored in strings in the client source code, environment variables, or application-specific configuration files.</span></span> <span data-ttu-id="99fce-109">您的用戶端應用程式可以使用字串中的資料來撰寫用戶端與伺服器之間的系結。</span><span class="sxs-lookup"><span data-stu-id="99fce-109">Your client application can use the data in the string to compose a binding between the client and the server.</span></span>
-   <span data-ttu-id="99fce-110">查詢名稱服務資料庫是否有伺服器程式的位置。</span><span class="sxs-lookup"><span data-stu-id="99fce-110">Querying a name service database for the location of a server program.</span></span>

<span data-ttu-id="99fce-111">本節提供下列主題中這兩種技術的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="99fce-111">This section presents information on both of these techniques in the following topics:</span></span>

-   [<span data-ttu-id="99fce-112">使用字串系結</span><span class="sxs-lookup"><span data-stu-id="99fce-112">Using String Bindings</span></span>](#using-string-bindings)
-   [<span data-ttu-id="99fce-113">從名稱服務資料庫匯入</span><span class="sxs-lookup"><span data-stu-id="99fce-113">Importing from Name Service Databases</span></span>](#importing-from-name-service-databases)

## <a name="using-string-bindings"></a><span data-ttu-id="99fce-114">使用字串系結</span><span class="sxs-lookup"><span data-stu-id="99fce-114">Using String Bindings</span></span>

<span data-ttu-id="99fce-115">應用程式可以從儲存在字串中的資訊建立系結。</span><span class="sxs-lookup"><span data-stu-id="99fce-115">Applications can create bindings from information stored in strings.</span></span> <span data-ttu-id="99fce-116">您的用戶端應用程式會將此資訊撰寫為字串，然後呼叫 [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) 函數。</span><span class="sxs-lookup"><span data-stu-id="99fce-116">Your client application composes this information as a string, then calls the [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) function.</span></span> <span data-ttu-id="99fce-117">用戶端必須提供下列資訊來識別伺服器：</span><span class="sxs-lookup"><span data-stu-id="99fce-117">The client must supply the following information to identify the server:</span></span>

-   <span data-ttu-id="99fce-118">介面名稱、物件的全域唯一識別碼 (GUID) 或物件的 UUID。</span><span class="sxs-lookup"><span data-stu-id="99fce-118">The interface name, the globally unique identifier (GUID) of the object, or UUID of the object.</span></span> <span data-ttu-id="99fce-119">如需詳細資訊，請參閱 [產生介面 uuid](generating-interface-uuids.md) 和 [字串 UUID](string-uuid.md)。</span><span class="sxs-lookup"><span data-stu-id="99fce-119">For more information, see [Generating Interface UUIDs](generating-interface-uuids.md) and [String UUID](string-uuid.md).</span></span>
-   <span data-ttu-id="99fce-120">要進行通訊的傳輸類型，例如具名管道或 TCP/IP。</span><span class="sxs-lookup"><span data-stu-id="99fce-120">The transport type to communicate over, such as named pipes or TCP/IP.</span></span> <span data-ttu-id="99fce-121">如需詳細資訊，請參閱 [基本的 RPC](essential-rpc-binding-terminology.md) 系結術語和 [選取通訊協定順序](selecting-a-protocol-sequence.md)。</span><span class="sxs-lookup"><span data-stu-id="99fce-121">For details, see [Essential RPC Binding Terminology](essential-rpc-binding-terminology.md) and [Selecting a Protocol Sequence](selecting-a-protocol-sequence.md).</span></span>
-   <span data-ttu-id="99fce-122">伺服器主機電腦的網路位址或名稱。</span><span class="sxs-lookup"><span data-stu-id="99fce-122">The network address or the name of the server host computer.</span></span>
-   <span data-ttu-id="99fce-123">伺服器主機電腦上伺服器程式的端點。</span><span class="sxs-lookup"><span data-stu-id="99fce-123">The endpoint of the server program on the server host computer.</span></span> <span data-ttu-id="99fce-124">如需詳細資訊，請參閱 [尋找端點](finding-endpoints.md)和 [指定端點](specifying-endpoints.md)。</span><span class="sxs-lookup"><span data-stu-id="99fce-124">For more information, see [Finding Endpoints](finding-endpoints.md), and [Specifying Endpoints](specifying-endpoints.md).</span></span>

<span data-ttu-id="99fce-125"> (物件 UUID 和端點資訊是選擇性的。 ) </span><span class="sxs-lookup"><span data-stu-id="99fce-125">(The object UUID and the endpoint information are optional.)</span></span>

<span data-ttu-id="99fce-126">在下列範例中， *pszNetworkAddress* 參數和其他參數包含內嵌的反斜線。</span><span class="sxs-lookup"><span data-stu-id="99fce-126">In the following examples, the *pszNetworkAddress* parameter and other parameters include embedded backslashes.</span></span> <span data-ttu-id="99fce-127">反斜線是 C 程式設計語言中的一個 escape 字元。</span><span class="sxs-lookup"><span data-stu-id="99fce-127">The backslash is an escape character in the C programming language.</span></span> <span data-ttu-id="99fce-128">需要兩個反斜線來代表每個單一常值反斜線字元。</span><span class="sxs-lookup"><span data-stu-id="99fce-128">Two backslashes are needed to represent each single literal backslash character.</span></span> <span data-ttu-id="99fce-129">字串系結結構必須包含四個反斜線字元，以代表伺服器名稱前面的兩個常值反斜線字元。</span><span class="sxs-lookup"><span data-stu-id="99fce-129">The string-binding structure must contain four backslash characters to represent the two literal backslash characters that precede the server name.</span></span>

<span data-ttu-id="99fce-130">下列範例顯示伺服器名稱前面必須有八個反斜線，如此一來，在 **sprintf \_** 的函式處理字串之後，字串系結資料結構中就會出現四個常值反斜線字元。</span><span class="sxs-lookup"><span data-stu-id="99fce-130">The following example shows that the server name must be preceded by eight backslashes so that four literal backslash characters will appear in the string-binding data structure after the **sprintf\_s** function processes the string.</span></span>


```C++
/* client application */

char * pszUuid = "6B29FC40-CA47-1067-B31D-00DD010662DA";
char * pszProtocol = "ncacn_np";
char * pszNetworkAddress = "\\\\\\\\servername";
char * pszEndpoint = "\\\\pipe\\\\pipename";
char * pszString;
 
int len = 0;
 
len  = sprintf_s(pszString, strlen(pszUuid), "%s", pszUuid);
len += sprintf_s(pszString + len, strlen(pszProtocolSequence) + 2, "@%s:",
    pszProtocolSequence);
if (pszNetworkAddress != NULL)
    len += sprintf_s(pszString + len, strlen(pszNetworkAddress), "%s",
    pszNetworkAddress);
len += sprintf_s(pszString + len, strlen(pszEndpoint) + 2, "[%s]", pszEndpoint);
```



<span data-ttu-id="99fce-131">在下列範例中，字串系結會顯示為：</span><span class="sxs-lookup"><span data-stu-id="99fce-131">In the following example, the string binding appears as:</span></span>

<span data-ttu-id="99fce-132">6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_np： \\ \\ \\ \\ *servername* \[ \\ \\ 管道 \\ \\ *pipename*\]</span><span class="sxs-lookup"><span data-stu-id="99fce-132">6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_np:\\\\\\\\*servername*\[\\\\pipe\\\\*pipename*\]</span></span>

<span data-ttu-id="99fce-133">然後，用戶端會呼叫 [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) 以取得系結控制碼：</span><span class="sxs-lookup"><span data-stu-id="99fce-133">The client then calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to obtain the binding handle:</span></span>


```C++
RPC_BINDING_HANDLE hBinding;
 
status = RpcBindingFromStringBinding(pszString, &hBinding);
//...
```



<span data-ttu-id="99fce-134">方便的函式 [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) 會以正確的語法，將物件 UUID、通訊協定順序、網路位址和端點組合成 [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="99fce-134">A convenience function, [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) assembles the object UUID, protocol sequence, network address, and endpoint in the correct syntax for the call to [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).</span></span> <span data-ttu-id="99fce-135">您不必擔心如何在正確的位置放置每個通訊協定順序的連字號、冒號和各種元件;您只需提供字串做為函式的參數。</span><span class="sxs-lookup"><span data-stu-id="99fce-135">You do not have to worry about putting the ampersand, colon, and the various components for each protocol sequence in the right place; you just supply the strings as parameters to the function.</span></span> <span data-ttu-id="99fce-136">執行時間程式庫甚至會配置字串系結所需的記憶體。</span><span class="sxs-lookup"><span data-stu-id="99fce-136">The run-time library even allocates the memory needed for the string binding.</span></span>


```C++
char * pszNetworkAddress = "\\\\server";
char * pszEndpoint = "\\pipe\\pipename";
status = RpcStringBindingCompose(
            pszUuid,
            pszProtocolSequence,
            pszNetworkAddress,
            pszEndpoint,
            pszOptions,
            &pszString);
//...
status = RpcBindingFromStringBinding(
            pszString,
            &hBinding);
//...
```



<span data-ttu-id="99fce-137">另一個方便的函式 [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)會採用系結控制碼做為輸入，並產生對應的字串系結。</span><span class="sxs-lookup"><span data-stu-id="99fce-137">Another convenience function, [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding), takes a binding handle as input and produces the corresponding string binding.</span></span>

## <a name="importing-from-name-service-databases"></a><span data-ttu-id="99fce-138">從名稱服務資料庫匯入</span><span class="sxs-lookup"><span data-stu-id="99fce-138">Importing from Name Service Databases</span></span>

<span data-ttu-id="99fce-139">命名服務資料庫儲存區，以及其他專案、系結控制碼和 Uuid。</span><span class="sxs-lookup"><span data-stu-id="99fce-139">Name service databases store, among other things, binding handles and UUIDs.</span></span> <span data-ttu-id="99fce-140">您的用戶端應用程式可以在需要系結至伺服器時，搜尋其中一個或兩個。</span><span class="sxs-lookup"><span data-stu-id="99fce-140">Your client application can search for either or both of these when it needs to bind to the server.</span></span> <span data-ttu-id="99fce-141">如需名稱服務儲存的資訊以及儲存格式的討論，請參閱 [RPC 名稱服務資料庫](the-rpc-name-service-database.md)。</span><span class="sxs-lookup"><span data-stu-id="99fce-141">For a discussion of the information that a name service stores, and the storage format, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

<span data-ttu-id="99fce-142">RPC 程式庫提供兩組功能，讓您的用戶端程式可用來搜尋名稱服務資料庫。</span><span class="sxs-lookup"><span data-stu-id="99fce-142">The RPC library provides two sets of functions that your client program can use to search the name service database.</span></span> <span data-ttu-id="99fce-143">其中一個集合的名稱開頭為 RpcNsBindingImport。</span><span class="sxs-lookup"><span data-stu-id="99fce-143">The names of one set begin with RpcNsBindingImport.</span></span> <span data-ttu-id="99fce-144">另一個集合的名稱開頭為 RpcNsBindingLookup。</span><span class="sxs-lookup"><span data-stu-id="99fce-144">The names of the other set begin with RpcNsBindingLookup.</span></span> <span data-ttu-id="99fce-145">這兩個函數群組之間的差異在於 RpcNsBindingImport 函式會傳回每個呼叫的單一系結控制碼，而 RpcNsBindingLookup 函式會傳回每個呼叫的控制碼群組。</span><span class="sxs-lookup"><span data-stu-id="99fce-145">The difference between the two groups of functions is that the RpcNsBindingImport functions return a single binding handle per call and the RpcNsBindingLookup functions return groups of handles per call.</span></span>

<span data-ttu-id="99fce-146">若要開始使用 RpcNsBindingImport 函數進行搜尋，請先呼叫 [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)，如下列程式碼片段所示。</span><span class="sxs-lookup"><span data-stu-id="99fce-146">To begin a search with the RpcNsBindingImport functions, first call [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), as shown in the following code fragment.</span></span>


```C++
RPC_STATUS status;
RPC_NS_HANDLE hNameServiceHandle;
 
status = RpcNsBindingImportBegin(
    RPC_C_NS_SYNTAX_DEFAULT,
    NULL,
    MyInterface_v1_0_c_ifspec,
    NULL,
    &hNameServiceHandle);
```



<span data-ttu-id="99fce-147">當 RPC 函數搜尋名稱服務資料庫時，他們需要一個位置來開始搜尋。</span><span class="sxs-lookup"><span data-stu-id="99fce-147">When the RPC functions search the name service database, they need a place to begin the search.</span></span> <span data-ttu-id="99fce-148">在 RPC 詞彙中，這稱為專案名稱。</span><span class="sxs-lookup"><span data-stu-id="99fce-148">In RPC terminology, this is called the entry name.</span></span> <span data-ttu-id="99fce-149">用戶端程式會將專案名稱做為第二個參數傳遞至 [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)。</span><span class="sxs-lookup"><span data-stu-id="99fce-149">Your client program passes the entry name as the second parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="99fce-150">如果您想要搜尋整個名稱服務資料庫，這個參數可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="99fce-150">This parameter can be **NULL** if you want to search the entire name service database.</span></span> <span data-ttu-id="99fce-151">或者，您可以傳遞伺服器專案名稱，或藉由傳遞群組專案名稱來搜尋群組專案，以搜尋伺服器專案。</span><span class="sxs-lookup"><span data-stu-id="99fce-151">Alternatively, you can search the server entry by passing a server-entry name or search the group entry by passing a group-entry name.</span></span> <span data-ttu-id="99fce-152">傳遞專案名稱會將搜尋限制為該專案的內容。</span><span class="sxs-lookup"><span data-stu-id="99fce-152">Passing an entry name restricts the search to the contents of that entry.</span></span>

<span data-ttu-id="99fce-153">在上述範例中，RPC \_ C \_ NS \_ 語法預設值 \_ 會以第一個參數的形式傳遞至 [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)。</span><span class="sxs-lookup"><span data-stu-id="99fce-153">In the preceding example, the value RPC\_C\_NS\_SYNTAX\_DEFAULT is passed as the first parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="99fce-154">這會選取預設的專案名稱語法。</span><span class="sxs-lookup"><span data-stu-id="99fce-154">This selects the default entry name syntax.</span></span> <span data-ttu-id="99fce-155">目前，這是唯一支援的專案名稱語法。</span><span class="sxs-lookup"><span data-stu-id="99fce-155">Currently, this is the only supported entry-name syntax.</span></span>

<span data-ttu-id="99fce-156">您的用戶端應用程式可以搜尋名稱服務資料庫中的介面名稱、UUID 或兩者。</span><span class="sxs-lookup"><span data-stu-id="99fce-156">Your client application can search the name service database for an interface name, a UUID, or both.</span></span> <span data-ttu-id="99fce-157">如果您想要讓它依名稱搜尋介面，請傳遞 MIDL 編譯器從 IDL 檔案產生的全域介面變數，做為 [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)的第三個參數。</span><span class="sxs-lookup"><span data-stu-id="99fce-157">If you want to have it search for an interface by name, pass the global interface variable that the MIDL compiler generates from your IDL file as the third parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="99fce-158">您會在 MIDL 編譯器產生用戶端 stub 時產生的標頭檔中，找到其宣告。</span><span class="sxs-lookup"><span data-stu-id="99fce-158">You'll find its declaration in the header file that the MIDL compiler generated when it generated the client stub.</span></span> <span data-ttu-id="99fce-159">如果您想要讓用戶端程式依 UUID 搜尋，請將第三個參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="99fce-159">If you want your client program to search by UUID only, set the third parameter to **NULL**.</span></span>

<span data-ttu-id="99fce-160">針對 UUID 搜尋名稱服務資料庫時，請將 [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) 的第四個參數設定為您想要搜尋的 uuid。</span><span class="sxs-lookup"><span data-stu-id="99fce-160">When searching the name service database for a UUID, set the fourth parameter of [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) to the UUID that you want to search for.</span></span> <span data-ttu-id="99fce-161">如果您未搜尋 UUID，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="99fce-161">If you are not searching for a UUID, set this parameter to **NULL**.</span></span>

<span data-ttu-id="99fce-162">[**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)函式會透過其第五個參數傳遞名稱服務的位址–搜尋內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="99fce-162">The [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) function passes the address of a name service–search context handle through its fifth parameter.</span></span> <span data-ttu-id="99fce-163">您會將此參數傳遞給其他 RpcNsBindingImport 函數。</span><span class="sxs-lookup"><span data-stu-id="99fce-163">You pass this parameter to other RpcNsBindingImport functions.</span></span>

<span data-ttu-id="99fce-164">尤其是，您用戶端應用程式會呼叫的下一個函式是 [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)。</span><span class="sxs-lookup"><span data-stu-id="99fce-164">In particular, the next function your client application would call is [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span></span> <span data-ttu-id="99fce-165">用戶端程式會使用此函式，從名稱服務資料庫中取出相容的系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="99fce-165">Client programs use this function to retrieve compatible binding handles from the name service database.</span></span> <span data-ttu-id="99fce-166">下列程式碼片段會示範如何呼叫此函數：</span><span class="sxs-lookup"><span data-stu-id="99fce-166">The following code fragment demonstrates how this function might be called:</span></span>


```C++
RPC_STATUS status;
RPC_BINDING_HANDLE hBindingHandle;
// The variable hNameServiceHandle is a valid name service search 
// context handle obtained from the RpcNsBindingBegin function.
 
status = RpcNsBindingImportNext(hNameServiceHandle, &hBindingHandle);
```



<span data-ttu-id="99fce-167">一旦呼叫 [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) 函式來取得系結控制碼之後，您的用戶端應用程式就可以判斷它所收到的控制碼是否可接受。</span><span class="sxs-lookup"><span data-stu-id="99fce-167">Once it has called the [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) function to obtain a binding handle, your client application can determine if the handle it received is acceptable.</span></span> <span data-ttu-id="99fce-168">如果沒有，您的用戶端程式可以執行迴圈，並再次呼叫 **RpcNsBindingImportNext** ，以查看名稱服務是否包含更適當的控制碼。</span><span class="sxs-lookup"><span data-stu-id="99fce-168">If not, your client program can execute a loop and call **RpcNsBindingImportNext** again to see if the name service contains a more appropriate handle.</span></span> <span data-ttu-id="99fce-169">對於 **RpcNsBindingImportNext** 的每個呼叫，都必須有對應的 RpcNsBindingFree 呼叫。</span><span class="sxs-lookup"><span data-stu-id="99fce-169">For each call to **RpcNsBindingImportNext**, there must be a corresponding call to RpcNsBindingFree.</span></span> <span data-ttu-id="99fce-170">當您的搜尋完成時，請呼叫 [**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) 函式來釋放查閱內容。</span><span class="sxs-lookup"><span data-stu-id="99fce-170">When your search is complete, call the [**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) function to free the lookup context.</span></span>

<span data-ttu-id="99fce-171">當您的用戶端應用程式具有可接受的系結控制碼之後，它應該檢查以確定伺服器應用程式正在執行。</span><span class="sxs-lookup"><span data-stu-id="99fce-171">After your client application has an acceptable binding handle, it should check to ensure that the server application is running.</span></span> <span data-ttu-id="99fce-172">用戶端可以使用兩種方法來執行此驗證。</span><span class="sxs-lookup"><span data-stu-id="99fce-172">There are two methods your client can use to perform this verification.</span></span> <span data-ttu-id="99fce-173">第一個是在用戶端介面中呼叫函數。</span><span class="sxs-lookup"><span data-stu-id="99fce-173">The first is to call a function in the client interface.</span></span> <span data-ttu-id="99fce-174">如果伺服器程式正在執行，則會完成呼叫。</span><span class="sxs-lookup"><span data-stu-id="99fce-174">If the server program is running, the call will complete.</span></span> <span data-ttu-id="99fce-175">如果沒有，則呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="99fce-175">If not, the call will fail.</span></span> <span data-ttu-id="99fce-176">若要確認伺服器是否正在執行，更好的方法是叫用 [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding)，然後呼叫 [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening)。</span><span class="sxs-lookup"><span data-stu-id="99fce-176">A better way to verify that the server is running is to invoke [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding), followed by a call to [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening).</span></span> <span data-ttu-id="99fce-177">如需名稱服務資料庫的詳細資訊，請參閱 [RPC 名稱服務資料庫](the-rpc-name-service-database.md)。</span><span class="sxs-lookup"><span data-stu-id="99fce-177">For more information on the name service database, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

 

 




