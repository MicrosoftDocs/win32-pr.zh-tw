---
title: WinINet 中的 IDN 支援
description: 從 Windows Server 2008 和 Windows Vista 開始，Unicode URL 的主機部分會轉換成國際化功能變數名稱 (IDN) 。
ms.assetid: 7c56908e-f6d0-48dc-9ac1-73f888fb7b6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510b1bc8d2ab77534d7f5dac587f287d5e7095af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382590"
---
# <a name="idn-support-in-wininet"></a><span data-ttu-id="df132-103">WinINet 中的 IDN 支援</span><span class="sxs-lookup"><span data-stu-id="df132-103">IDN Support in WinINet</span></span>

<span data-ttu-id="df132-104">從 Windows Server 2008 和 Windows Vista 開始，Unicode URL 的主機部分會轉換成國際化功能變數名稱 (IDN) 。</span><span class="sxs-lookup"><span data-stu-id="df132-104">Starting in Windows Server 2008 and Windows Vista, the host portion of the Unicode URL is converted to the Internationalized Domain Name (IDN).</span></span> <span data-ttu-id="df132-105">個別的 Unicode URL 編碼部分也可以由應用程式設定的設定修改。</span><span class="sxs-lookup"><span data-stu-id="df132-105">Separate portions of the Unicode URL encoding can also be modified by configurations set by the application.</span></span> <span data-ttu-id="df132-106">ANSI 版本的 WinINet API 會繼續透過網路傳送 URL，如同應用程式所輸入的一樣，不過，WinINet Unicode 版本的 API 現在符合 IDN 標準 (RFC3490) 進行 URL 編碼。</span><span class="sxs-lookup"><span data-stu-id="df132-106">The ANSI versions of the WinINet API continue to send the URL over the wire as entered by the application, however the WinINet Unicode versions of the API now conform to the IDN standard (RFC3490) for URL encodings.</span></span>

<span data-ttu-id="df132-107">根據預設，當輸入 URL 作為 Unicode 參數時，會將 proxy 和直接連接的主機部分轉換成 IDN 格式。</span><span class="sxs-lookup"><span data-stu-id="df132-107">By default, when a URL is entered as a Unicode parameter, the host portion, for both proxy and direct connections, is converted to IDN format.</span></span> <span data-ttu-id="df132-108">應用程式可透過設定 **網際網路 \_ 選項 \_ IDN** 選項，選擇停用 IDN 主機格式。</span><span class="sxs-lookup"><span data-stu-id="df132-108">The application has the option to disable IDN host formatting by setting the **INTERNET\_OPTION\_IDN** option.</span></span> <span data-ttu-id="df132-109">您可以使用 **網際網路 \_ 旗標 \_ Idn \_ direct** 或 **網際網路 \_ 旗標 \_ idn \_ proxy** 旗標搭配 **網際網路 \_ 選項 \_ idn**，僅在直接或 proxy 連接上啟用 idn 主機轉換。</span><span class="sxs-lookup"><span data-stu-id="df132-109">IDN host conversion can be enabled on only the direct or proxy connections by using the **INTERNET\_FLAG\_IDN\_DIRECT** or **INTERNET\_FLAG\_IDN\_PROXY** flags with **INTERNET\_OPTION\_IDN**.</span></span>

<span data-ttu-id="df132-110">下列程式碼範例示範如何停用 proxy 和直接連接的 IDN 主機轉換。</span><span class="sxs-lookup"><span data-stu-id="df132-110">The following code example shows how to disable IDN host conversion for both the proxy and direct connections.</span></span>

``` syntax
DWORD IDN = 0; 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_IDN,
                   &IDN, 
                   sizeof(DWORD) ); 
```

<span data-ttu-id="df132-111">如果已停用 IDN 主機格式，則應用程式可以選擇使用 **網際網路 \_ 選項 \_ 字碼頁** 來指定所需的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="df132-111">If IDN host formatting is disabled, the application has the option to specify the desired codepage using **INTERNET\_OPTION\_CODEPAGE**.</span></span>

<span data-ttu-id="df132-112">下列程式碼範例顯示如何指定日文字碼頁。</span><span class="sxs-lookup"><span data-stu-id="df132-112">The following code example shows how to specify the Japanese code page.</span></span>

``` syntax
DWORD CP_SHIFT_JIS = 932;  // ANSI/OEM  Japanese, Shift-JIS
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE,
                   &CP_SHIFT_JIS, 
                   Sizeof(DWORD) ); 
```

<span data-ttu-id="df132-113">URL 的路徑部分預設為 UTF8 編碼，而 URL 的其餘區段（查詢或片段）會轉換成預設的系統字碼頁 (CP \_ ACP) 。</span><span class="sxs-lookup"><span data-stu-id="df132-113">The path portion of the URL is UTF8 encoded by default, and the remaining segments of the URL, the query or fragment, are converted to the default system code page (CP\_ACP).</span></span>

<span data-ttu-id="df132-114">下列範例示範如何指定 URL 路徑部分的韓文語言字碼頁。</span><span class="sxs-lookup"><span data-stu-id="df132-114">The following example shows how to specify the Korean language code page for the path portion of the URL.</span></span>

``` syntax
DWORD CP_KOREAN = 949;   // ANSI/OEM Korean 
InternetSetOption( hRequest, 
                   INTERNET_OPTION_CODEPAGE_PATH,
                   &CP_KOREAN, 
                   sizeof(DWORD) );
```

<span data-ttu-id="df132-115">下表定義支援 IDN 的選項。</span><span class="sxs-lookup"><span data-stu-id="df132-115">The following table defines the options that support IDN.</span></span> <span data-ttu-id="df132-116">如需詳細資訊，請參閱 [選項旗標](option-flags.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="df132-116">For more information, see the [Option Flags](option-flags.md) topic.</span></span>



| <span data-ttu-id="df132-117">選項</span><span class="sxs-lookup"><span data-stu-id="df132-117">Option</span></span>                            | <span data-ttu-id="df132-118">Description</span><span class="sxs-lookup"><span data-stu-id="df132-118">Description</span></span>                                                                                                                                                                                                                     |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df132-119">網際網路 \_ 選項 \_ 字碼頁</span><span class="sxs-lookup"><span data-stu-id="df132-119">INTERNET\_OPTION\_CODEPAGE</span></span>        | <span data-ttu-id="df132-120">此選項設定于要求或連接控制碼上，以指定 URL 之主機部分的字碼頁編碼配置。</span><span class="sxs-lookup"><span data-stu-id="df132-120">This option is set on the request, or connection handle, to specify a code page encoding scheme for the host portion of the URL.</span></span> <span data-ttu-id="df132-121">如果已啟用 IDN，則會忽略此選項。</span><span class="sxs-lookup"><span data-stu-id="df132-121">This option is ignored if IDN is enabled.</span></span>                                                      |
| <span data-ttu-id="df132-122">網際網路 \_ 選項 \_ 字碼頁 \_ 路徑</span><span class="sxs-lookup"><span data-stu-id="df132-122">INTERNET\_OPTION\_CODEPAGE\_PATH</span></span>  | <span data-ttu-id="df132-123">此選項會在要求上設定，或連接控制碼會對 URL 的路徑部分啟用指定的編碼配置。</span><span class="sxs-lookup"><span data-stu-id="df132-123">This option is set on the request, or connection handle enables the specified encoding scheme for the path portion of the URL.</span></span> <span data-ttu-id="df132-124">根據預設，URL 的路徑部分為 UTF8 編碼。</span><span class="sxs-lookup"><span data-stu-id="df132-124">By default, the path portion of the URL is UTF8 encoded.</span></span>                                         |
| <span data-ttu-id="df132-125">網際網路 \_ 選項 \_ 字碼頁 \_ 額外</span><span class="sxs-lookup"><span data-stu-id="df132-125">INTERNET\_OPTION\_CODEPAGE\_EXTRA</span></span> | <span data-ttu-id="df132-126">在要求上設定此選項，或連接控制碼，可針對 URL 的額外部分啟用指定的編碼配置。</span><span class="sxs-lookup"><span data-stu-id="df132-126">Setting this option on the request, or connection handle enables the specified encoding scheme for the extra portion of the URL.</span></span> <span data-ttu-id="df132-127">根據預設，會在預設的系統字碼頁中，將 URL 的額外部分編碼 (CP \_ ACP) 。</span><span class="sxs-lookup"><span data-stu-id="df132-127">By default, the extra portion of the URL is encoded in the default system code page (CP\_ACP).</span></span> |
| <span data-ttu-id="df132-128">網際網路 \_ 選項 \_ IDN</span><span class="sxs-lookup"><span data-stu-id="df132-128">INTERNET\_OPTION\_IDN</span></span>             | <span data-ttu-id="df132-129">此選項可用於要求或連接控制碼，以啟用或停用 IDN 主機轉換。</span><span class="sxs-lookup"><span data-stu-id="df132-129">This option can be used on the request, or connection handle to enable or disable IDN host conversion.</span></span> <span data-ttu-id="df132-130">當 IDN 停用時，WinINet 會使用預設的系統字碼頁來編碼 URL 的主機或授權單位部分。</span><span class="sxs-lookup"><span data-stu-id="df132-130">When IDN is disabled, WinINet uses the default system codepage to encode the host or authority portion of the URL.</span></span>       |



 

> [!Note]  
> <span data-ttu-id="df132-131">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="df132-131">WinINet does not support server implementations.</span></span> <span data-ttu-id="df132-132">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="df132-132">In addition, it should not be used from a service.</span></span> <span data-ttu-id="df132-133">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="df132-133">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 