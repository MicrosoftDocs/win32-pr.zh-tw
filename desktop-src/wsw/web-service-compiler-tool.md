---
title: Web 服務編譯器工具
description: 為了支援服務模型，wsutil.exe 會產生要用於用戶端和服務端的標頭。 它會視需要產生用戶端的 C proxy 檔案，以及服務端的 C 存根檔案。
ms.assetid: 1c73297d-0d3d-421c-9e19-44a6012a5c65
keywords:
- 適用于 Windows 的 web 服務編譯器工具 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9931f228a36832fc83d84d584a151de41f5868d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383337"
---
# <a name="web-service-compiler-tool"></a><span data-ttu-id="dda81-107">Web 服務編譯器工具</span><span class="sxs-lookup"><span data-stu-id="dda81-107">Web Service Compiler Tool</span></span>

<span data-ttu-id="dda81-108">為了支援服務模型，wsutil.exe 會產生要用於用戶端和服務端的標頭。</span><span class="sxs-lookup"><span data-stu-id="dda81-108">To support service model, wsutil.exe generates header to be used in both client and service side.</span></span> <span data-ttu-id="dda81-109">它會視需要產生用戶端的 C proxy 檔案，以及服務端的 C 存根檔案。</span><span class="sxs-lookup"><span data-stu-id="dda81-109">It generates C proxy file for client side, and C stub file for service side, as needed.</span></span>


<span data-ttu-id="dda81-110">為了支援 [序列化](serialization.md)，編譯器會針對全域專案定義產生專案描述的標頭，並針對序列化引擎使用 proxy 檔案中的所有類型定義資訊。</span><span class="sxs-lookup"><span data-stu-id="dda81-110">To support [serialization](serialization.md), the compiler generates headers for element descriptions for global element definitions, and all type definition information in proxy file to be consumed by the serialization engine.</span></span>

<span data-ttu-id="dda81-111">使用方式</span><span class="sxs-lookup"><span data-stu-id="dda81-111">Usage</span></span>

<span data-ttu-id="dda81-112">**WsUtil.exe \[ 命令列參數 \[ 參數-選項 \] ：\]<filename>**</span><span class="sxs-lookup"><span data-stu-id="dda81-112">**WsUtil.exe \[command-line-switches \[switch-options\]:\]<filename>**</span></span>

<span data-ttu-id="dda81-113">命令列參數</span><span class="sxs-lookup"><span data-stu-id="dda81-113">command-line-switches</span></span>

<span data-ttu-id="dda81-114">指定 WsUtil.exe 編譯器選項。</span><span class="sxs-lookup"><span data-stu-id="dda81-114">Specifies WsUtil.exe compiler options.</span></span> <span data-ttu-id="dda81-115">參數可以依任何順序顯示。</span><span class="sxs-lookup"><span data-stu-id="dda81-115">Switches can appear in any order.</span></span> <span data-ttu-id="dda81-116">虛線 ( '-' ) 和斜線 ( '/' ) 會視為相同。</span><span class="sxs-lookup"><span data-stu-id="dda81-116">Dash ('-') and slash ('/') are treated as the same.</span></span>

<span data-ttu-id="dda81-117">命令列選項清單</span><span class="sxs-lookup"><span data-stu-id="dda81-117">List of command line options</span></span>

-   <span data-ttu-id="dda81-118">@filename 指定應將輸入檔視為回應檔。</span><span class="sxs-lookup"><span data-stu-id="dda81-118">@filename Specifies that the input file should be treated as a response file.</span></span> <span data-ttu-id="dda81-119">這個選項可以在引數清單中的任何位置使用多次。</span><span class="sxs-lookup"><span data-stu-id="dda81-119">This option can be used multiple times, in any places in the argument list.</span></span>
-   <span data-ttu-id="dda81-120">/wsdl： <filename> ： <選擇性 \_ Url> 指定應將輸入檔視為 wsdl 檔。</span><span class="sxs-lookup"><span data-stu-id="dda81-120">/wsdl:<filename>:<optional\_url> Specifies that the input file should be treated as a wsdl file.</span></span> <span data-ttu-id="dda81-121">允許多個 wsdl 輸入，並處理所有指定的 wsdl 檔案。</span><span class="sxs-lookup"><span data-stu-id="dda81-121">Multiple wsdl inputs are allowed and all specified wsdl files are processed.</span></span> <span data-ttu-id="dda81-122">選擇性 url 會指定從中抓取 \_ 中繼資料的位置。</span><span class="sxs-lookup"><span data-stu-id="dda81-122">The optional\_url specifies the location where the metadata was retrieved from.</span></span> <span data-ttu-id="dda81-123">如果未 \_ 指定選擇性的 url，Wsutil 會在內部產生唯一的 url。</span><span class="sxs-lookup"><span data-stu-id="dda81-123">If no optional\_url is specified, Wsutil generates a unique url internally.</span></span> <span data-ttu-id="dda81-124">另請參閱 [原則支援](policy-support.md)。</span><span class="sxs-lookup"><span data-stu-id="dda81-124">See also [Policy Support](policy-support.md).</span></span>
-   <span data-ttu-id="dda81-125">/xsd： <filename> 指定應將輸入檔案名視為架構檔。</span><span class="sxs-lookup"><span data-stu-id="dda81-125">/xsd:<filename> Specifies that the input filename should be treated as a schema file.</span></span> <span data-ttu-id="dda81-126">允許多個 xsd 輸入，並處理所有指定的架構檔案。</span><span class="sxs-lookup"><span data-stu-id="dda81-126">Multiple xsd inputs are allowed and all specified schema files are processed.</span></span>
-   <span data-ttu-id="dda81-127">/wsp： <filename> ： <選擇性 \_ Url> 指定應將輸入檔案名視為原則中繼資料。</span><span class="sxs-lookup"><span data-stu-id="dda81-127">/wsp:<filename>:<optional\_url> Specifies that the input filename should be treated as policy metadata.</span></span> <span data-ttu-id="dda81-128">允許多個 wsp 輸入，並處理所有指定的原則檔案。</span><span class="sxs-lookup"><span data-stu-id="dda81-128">Multiple wsp inputs are allowed and all specified policy files are processed.</span></span> <span data-ttu-id="dda81-129">選擇性 url 會指定從中抓取 \_ 中繼資料的位置。</span><span class="sxs-lookup"><span data-stu-id="dda81-129">The optional\_url specifies the location where the metadata was retrieved from.</span></span> <span data-ttu-id="dda81-130">如果未 \_ 指定選擇性的 url，Wsutil 會在內部產生唯一的 url。</span><span class="sxs-lookup"><span data-stu-id="dda81-130">If no optional\_url is specified, Wsutil generates a unique url internally.</span></span> <span data-ttu-id="dda81-131">如果指定了/nopolicy 旗標，則會忽略原則檔。</span><span class="sxs-lookup"><span data-stu-id="dda81-131">Policy files are ignored if /nopolicy flag is specified.</span></span> <span data-ttu-id="dda81-132">另請參閱 [原則支援](policy-support.md)。</span><span class="sxs-lookup"><span data-stu-id="dda81-132">See also [Policy Support](policy-support.md).</span></span>
-   <span data-ttu-id="dda81-133">/nopolicy 停用原則處理。</span><span class="sxs-lookup"><span data-stu-id="dda81-133">/nopolicy Disable policy processing.</span></span>
-   <span data-ttu-id="dda81-134">/out： <dirname> 指定輸出檔案的目錄名稱</span><span class="sxs-lookup"><span data-stu-id="dda81-134">/out:<dirname> Specifies directory name for output files</span></span>
-   <span data-ttu-id="dda81-135">/noclient 不會產生用戶端存根。</span><span class="sxs-lookup"><span data-stu-id="dda81-135">/noclient Do not generate the client side stub.</span></span>
-   <span data-ttu-id="dda81-136">/noservice 不會產生服務端存根。</span><span class="sxs-lookup"><span data-stu-id="dda81-136">/noservice Do not generate the service side stub.</span></span>
-   <span data-ttu-id="dda81-137">/prefix： <string> 在所有產生的識別碼前面加上指定的字串。</span><span class="sxs-lookup"><span data-stu-id="dda81-137">/prefix:<string> Prepend specified string to all generated identifiers.</span></span>
-   <span data-ttu-id="dda81-138">/fullname 在產生的識別碼前面加上正規化的檔案名。</span><span class="sxs-lookup"><span data-stu-id="dda81-138">/fullname Prepend normalized filename to generated identifiers.</span></span> <span data-ttu-id="dda81-139">依預設，只會使用 "name" 屬性中指定的名稱來產生相關描述的識別碼。</span><span class="sxs-lookup"><span data-stu-id="dda81-139">By default only name specified in "name" attribute will be used to generate identifiers for related descriptions.</span></span>
-   <span data-ttu-id="dda81-140">/string： <WS \_ 字串>\|<WCHAR \*> 根據預設，wsutil 會產生 \* xsd： string 類型的 WCHAR。</span><span class="sxs-lookup"><span data-stu-id="dda81-140">/string:<WS\_STRING>\|<WCHAR\*> By default, wsutil generates WCHAR\* for xsd:string type.</span></span> <span data-ttu-id="dda81-141">應用程式可以使用此旗標來覆寫該行為，並 \_ 改為產生 xsd： type 的 WS 字串。</span><span class="sxs-lookup"><span data-stu-id="dda81-141">Application can use this flag to overwrite that behavior, and generates WS\_STRING for xsd:type instead.</span></span>
-   <span data-ttu-id="dda81-142">/help 顯示說明訊息</span><span class="sxs-lookup"><span data-stu-id="dda81-142">/help Display help message</span></span>
-   <span data-ttu-id="dda81-143">/?</span><span class="sxs-lookup"><span data-stu-id="dda81-143">/?</span></span> <span data-ttu-id="dda81-144">與/help 相同</span><span class="sxs-lookup"><span data-stu-id="dda81-144">Same as /help</span></span>
-   <span data-ttu-id="dda81-145">/W： x 錯誤處理選項。</span><span class="sxs-lookup"><span data-stu-id="dda81-145">/W:x Error handling options.</span></span> <span data-ttu-id="dda81-146">可能是 W:0-W： 4 \| WX</span><span class="sxs-lookup"><span data-stu-id="dda81-146">Could be W:0-W:4 \| WX</span></span>
-   <span data-ttu-id="dda81-147">/nologo 不會產生主控台輸出的編譯器特定資訊。</span><span class="sxs-lookup"><span data-stu-id="dda81-147">/nologo Do not generate compiler specific information on console output.</span></span>
-   <span data-ttu-id="dda81-148">/nostamp 不會產生所產生檔案的編譯器特定資訊。</span><span class="sxs-lookup"><span data-stu-id="dda81-148">/nostamp Do not generate compiler specific information on generated files.</span></span>

<span data-ttu-id="dda81-149">根據預設，編譯器會為 WSDL 檔案或從中繼資料交換傳回的 WSDL 產生下列檔案：</span><span class="sxs-lookup"><span data-stu-id="dda81-149">By default, the compiler generates the following files for WSDL file, or WSDL returned from metadata exchange:</span></span>

-   <span data-ttu-id="dda81-150">用戶端 proxy ( {inputfilename} .c) </span><span class="sxs-lookup"><span data-stu-id="dda81-150">Client proxy ({inputfilename}.c)</span></span>
-   <span data-ttu-id="dda81-151">服務 Stub ( {inputfilename} .c) </span><span class="sxs-lookup"><span data-stu-id="dda81-151">Service Stub ({inputfilename}.c)</span></span>
-   <span data-ttu-id="dda81-152">標頭檔 ( {inputfilename} .h) </span><span class="sxs-lookup"><span data-stu-id="dda81-152">Header file ({inputfilename}.h)</span></span>

    <span data-ttu-id="dda81-153">所產生檔案名的根目錄是輸入檔名稱。</span><span class="sxs-lookup"><span data-stu-id="dda81-153">The root of the generated filename is the input file name.</span></span> <span data-ttu-id="dda81-154">保留原始輸入副檔名，以防止產生之檔案的檔案名衝突。</span><span class="sxs-lookup"><span data-stu-id="dda81-154">Original input file extensions are preserved to prevent file name collision for generated files.</span></span> <span data-ttu-id="dda81-155">依預設，會在相同的檔案中產生用戶端和服務存根，並在 proxy 程式碼之後產生服務 stub 程式碼。</span><span class="sxs-lookup"><span data-stu-id="dda81-155">By default client and service stubs are generated in the same file, with service stub code generated after the proxy code.</span></span>

    <span data-ttu-id="dda81-156">根據預設，編譯器會針對從中繼資料交換傳回的架構，為 XSD 檔案產生下列檔案：</span><span class="sxs-lookup"><span data-stu-id="dda81-156">By default, the compiler generates the following files for a XSD file for schema returned from metadata exchange:</span></span>

-   <span data-ttu-id="dda81-157">序列化描述 ( {inputfilename} .c) </span><span class="sxs-lookup"><span data-stu-id="dda81-157">serialization descriptions ({inputfilename}.c)</span></span>
-   <span data-ttu-id="dda81-158">標頭檔 ( {inputfilename} .h) </span><span class="sxs-lookup"><span data-stu-id="dda81-158">Header file ({inputfilename}.h)</span></span>

    <span data-ttu-id="dda81-159">檔案名的根目錄是服務名稱。</span><span class="sxs-lookup"><span data-stu-id="dda81-159">The root of the filename is the service name.</span></span>

<span data-ttu-id="dda81-160">Wsutil.exe 會在所有產生的檔案開頭產生「戳記」區段，指出編譯器選項、工具版本、適用的命令列選項等。您可以使用/nostamp 選項來關閉此區段，以避免在比較產生的檔案時產生干擾。</span><span class="sxs-lookup"><span data-stu-id="dda81-160">Wsutil.exe generates a "stamp" section at the beginning of all the generated files, indicating the compiler option, tool version, command line option applicable, etc. This section can be turned off by using /nostamp option to avoid noise with comparing generated files.</span></span>

<span data-ttu-id="dda81-161">Wsutil 不支援下載中繼資料</span><span class="sxs-lookup"><span data-stu-id="dda81-161">Wsutil does not support downloading metadata</span></span>

<span data-ttu-id="dda81-162">Wsutil 編譯器只適用于本機中繼資料檔案。</span><span class="sxs-lookup"><span data-stu-id="dda81-162">Wsutil compiler works from local metadata file only.</span></span> <span data-ttu-id="dda81-163">此工具不支援從執行中的 web 服務下載中繼資料。</span><span class="sxs-lookup"><span data-stu-id="dda81-163">The tool does not support downloading metadata from running web services.</span></span> <span data-ttu-id="dda81-164">開發人員可以使用其他支援的 webservice 工具（例如 svcutil），將中繼資料下載至本機電腦、檢查儲存的檔案，並將這些檔案傳遞至 wsutil.exe 進行編譯。</span><span class="sxs-lookup"><span data-stu-id="dda81-164">Developers can use other supported webservice tools, like svcutil, to download metadata to local machine, inspect the saved files, and pass those files to wsutil.exe for compilation.</span></span>

<span data-ttu-id="dda81-165">多個輸入/輸出檔案支援</span><span class="sxs-lookup"><span data-stu-id="dda81-165">Multiple input/output file support</span></span>

<span data-ttu-id="dda81-166">WSDL 和 XML 架構可讓您從其他位置/檔案中指定的其他命名空間包含/匯入定義。</span><span class="sxs-lookup"><span data-stu-id="dda81-166">WSDL and XML schema allows including/importing definitions from other name spaces specified in other location/files.</span></span> <span data-ttu-id="dda81-167">Wsutil 支援多個架構/wsdl/原則輸入，並為每個輸入檔產生一組存根/標頭。</span><span class="sxs-lookup"><span data-stu-id="dda81-167">Wsutil supports multiple schema/wsdl/policy input, and generate one set of stub/header for each input files.</span></span> <span data-ttu-id="dda81-168">Wsutil 不會遵循 include 和 import 語句。</span><span class="sxs-lookup"><span data-stu-id="dda81-168">Wsutil does not follow through the include and import statements.</span></span> <span data-ttu-id="dda81-169">相反地，應用程式應該將包含所有必要命名空間的檔案傳入 wsutil，如此一來，工具就可以在編譯期間解析所有相依性。</span><span class="sxs-lookup"><span data-stu-id="dda81-169">Instead, application should pass in files containing all necessary namespaces to wsutil such that the tool can resolve all dependencies during compilation.</span></span>

<span data-ttu-id="dda81-170">**WsUtil.exe/xsd： stockquote .xsd/wsdl： stockquote .wsdl/wsdl： stockquoteservice .wsdl**</span><span class="sxs-lookup"><span data-stu-id="dda81-170">**WsUtil.exe /xsd:stockquote.xsd /wsdl:stockquote.wsdl /wsdl:stockquoteservice.wsdl**</span></span>

<span data-ttu-id="dda81-171">wsutil 會產生三組輸出檔案：</span><span class="sxs-lookup"><span data-stu-id="dda81-171">wsutil generates three sets of output files:</span></span>

-   <span data-ttu-id="dda81-172">stockquote .xsd stockquote .xsd</span><span class="sxs-lookup"><span data-stu-id="dda81-172">stockquote.xsd.c stockquote.xsd.h</span></span>
-   <span data-ttu-id="dda81-173">stockquote .wsdl stockquote。h</span><span class="sxs-lookup"><span data-stu-id="dda81-173">stockquote.wsdl.c stockquote.wsdl.h</span></span>
-   <span data-ttu-id="dda81-174">stockquoteservice .wsdl stockquoteservices .wsdl</span><span class="sxs-lookup"><span data-stu-id="dda81-174">stockquoteservice.wsdl.h stockquoteservices.wsdl.c</span></span>

<span data-ttu-id="dda81-175">輸出檔案格式</span><span class="sxs-lookup"><span data-stu-id="dda81-175">Output file format</span></span>

<span data-ttu-id="dda81-176">針對每個輸出檔案，wsutil 會在標頭檔中產生外部可用的定義。</span><span class="sxs-lookup"><span data-stu-id="dda81-176">For each output file, wsutil generates externally available definitions in the header file.</span></span> <span data-ttu-id="dda81-177">除了 C 結構定義和存根函式原型之外，所有其他的 web 服務相關定義都會封裝在名為 with 正規化檔案名的全域結構中。</span><span class="sxs-lookup"><span data-stu-id="dda81-177">Other than C structure definitions and stub function prototypes, all the other web services related definitions are encapsulated in a global structure named with normalized filename.</span></span>

``` syntax
typedef struct _stockquote_wsdl {
  struct {
  ... // list of WS_STRUCT_DESCRIPTION for all global complex types.
  } globalTypes;
  struct {
  ... // WS_ELEMENT_DESCRIPTION for all global elements.
  } globalElements;
  struct {
  ...
  } messages;
  struct {
  ...
  } contracts;
} _stockquote_wsdl;

EXTERN_C _stockquote_wsdl stockquote_wsdl;
```

<span data-ttu-id="dda81-178">請注意，並非所有欄位都是針對全域結構產生的。</span><span class="sxs-lookup"><span data-stu-id="dda81-178">Notice that not all the fields are generated for the global structure.</span></span> <span data-ttu-id="dda81-179">只有在輸入檔案中指定相關定義時，才會產生最上層欄位。</span><span class="sxs-lookup"><span data-stu-id="dda81-179">A top level field is generated only when the related definitions are specified in the input file.</span></span> <span data-ttu-id="dda81-180">例如，xsd 檔案不會產生任何訊息、作業和合約欄位。</span><span class="sxs-lookup"><span data-stu-id="dda81-180">For example, no message, operations, and contracts fields are generated for xsd files.</span></span>

<span data-ttu-id="dda81-181">警告層級和錯誤層級</span><span class="sxs-lookup"><span data-stu-id="dda81-181">Warning Levels and error level</span></span>

<span data-ttu-id="dda81-182">類似于 C 編譯器，WsUtil.exe 支援四個警告層級和一個錯誤層級：</span><span class="sxs-lookup"><span data-stu-id="dda81-182">Similar to C compiler, WsUtil.exe supports four warning levels and one error level:</span></span>

-   <span data-ttu-id="dda81-183">WsUtil.exe 會產生無法復原失敗的錯誤，例如不正確 wsdl 檔案、不正確編譯器選項等。</span><span class="sxs-lookup"><span data-stu-id="dda81-183">WsUtil.exe generates errors with unrecoverable failures, like invalid wsdl file, invalid compiler options etc.</span></span>
-   <span data-ttu-id="dda81-184">WsUtil 會產生具有嚴重可復原問題的 W1 警告。</span><span class="sxs-lookup"><span data-stu-id="dda81-184">WsUtil generates W1 warnings with serious recoverable issues.</span></span> <span data-ttu-id="dda81-185">編譯器可以繼續進行，但使用者應該留意問題。</span><span class="sxs-lookup"><span data-stu-id="dda81-185">The compiler can go on but user should be aware of the issue.</span></span> <span data-ttu-id="dda81-186">例如，在不會影響程式碼產生的 wsdl 中有不支援的屬性時，將會產生 W1 警告。</span><span class="sxs-lookup"><span data-stu-id="dda81-186">For example, a W1 warning will be generated if there are unsupported attributes, like some WSDL facets, in wsdl that does not affect code generation.</span></span>
-   <span data-ttu-id="dda81-187">WsUtil 會產生較不嚴重問題的 W2 警告。</span><span class="sxs-lookup"><span data-stu-id="dda81-187">WsUtil generates W2 warnings with less serious problems.</span></span> <span data-ttu-id="dda81-188">功能沒有遺失，但應用程式開發人員可能會想要知道。</span><span class="sxs-lookup"><span data-stu-id="dda81-188">There is no lost of functionality, but application developer might want to know that.</span></span> <span data-ttu-id="dda81-189">與其他平臺可能不同的行為。</span><span class="sxs-lookup"><span data-stu-id="dda81-189">Like behaviors that might be different from other platforms.</span></span>
-   <span data-ttu-id="dda81-190">WsUtil 會產生與產生的程式碼不會影響極低的 W3 警告。</span><span class="sxs-lookup"><span data-stu-id="dda81-190">WsUtil generates W3 warnings with minimal impact on generated code.</span></span> <span data-ttu-id="dda81-191">例如，當正規化字串與原始字串不同時，wsutil.exe 會產生 W3 警告。</span><span class="sxs-lookup"><span data-stu-id="dda81-191">For example, wsutil.exe generates a W3 warning when normalized string is different from original string.</span></span>
-   <span data-ttu-id="dda81-192">W4 警告比較像是「資訊」警告，以及 WsUtil 在 WSDL 中忽略檔案屬性等情況下 W4 的問題。</span><span class="sxs-lookup"><span data-stu-id="dda81-192">W4 warning is more like "informational" warnings, and WsUtil issue W4 in cases like ignoring documentation attribute in WSDL.</span></span>
-   <span data-ttu-id="dda81-193">WX 指出編譯器將警告視為錯誤。</span><span class="sxs-lookup"><span data-stu-id="dda81-193">WX indicates the compiler treats warning as error.</span></span> <span data-ttu-id="dda81-194">例如，如果指定了/W： 1/WX，wsutil 就會針對所有 W1 警告產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="dda81-194">For example, wsutil generates error for all W1 warnings if /W:1 /WX is specified.</span></span>

<span data-ttu-id="dda81-195">/W： {N} 指定應產生的警告訊息層級。</span><span class="sxs-lookup"><span data-stu-id="dda81-195">/W:{N} specify which level of warning message should be generated.</span></span> <span data-ttu-id="dda81-196">/W：1表示應產生警告層級1警告，而且警告層級2和以下警告應遮罩，而不是由工具產生。</span><span class="sxs-lookup"><span data-stu-id="dda81-196">/W:1 means warning level 1 warnings should be generated, and warnings of warning level 2 and below should be masked and not generated by the tool.</span></span>

## <a name="fullname"></a><span data-ttu-id="dda81-197">/fullname</span><span class="sxs-lookup"><span data-stu-id="dda81-197">/fullname</span></span>

<span data-ttu-id="dda81-198">此選項指出 WsUtil.exe 會產生識別碼的完整名稱，以避免潛在的名稱衝突。</span><span class="sxs-lookup"><span data-stu-id="dda81-198">This option indicates that WsUtil.exe generates full name for identifiers to avoid potential name collision.</span></span> <span data-ttu-id="dda81-199">例如，在範例中，我們有：</span><span class="sxs-lookup"><span data-stu-id="dda81-199">For example, in example.xsd we have:</span></span>

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:element name="SimpleStruct">
   <xs:complexType>
    <xs:sequence>
     <xs:element name="a" type="xs:int" />
     <xs:element name="b" type="xs:int" />
    </xs:sequence>
   </xs:complexType>
  </xs:element>
 </wsdl:types>
</wsdl:definitions>
```

<span data-ttu-id="dda81-200">根據預設，WsUtil.exe 會產生：</span><span class="sxs-lookup"><span data-stu-id="dda81-200">By default WsUtil.exe generates:</span></span>

``` syntax
typedef struct SimpleStruct {
  int a;
  int b;
};
```

<span data-ttu-id="dda81-201">但是，如果指定了/fullname 命令列選項，WsUtil.exe 會改為產生下列結構定義：</span><span class="sxs-lookup"><span data-stu-id="dda81-201">But if /fullname command line option is specified, WsUtil.exe generates the following structure definition instead:</span></span>

``` syntax
typedef struct exmaple_xsd_SimpleStruct {
  int a;
  int b;
};
```

## <a name="globalization"></a><span data-ttu-id="dda81-202">全球化</span><span class="sxs-lookup"><span data-stu-id="dda81-202">Globalization</span></span>

<span data-ttu-id="dda81-203">此工具是中性語言，可以當地語系化成不同的語言。</span><span class="sxs-lookup"><span data-stu-id="dda81-203">The tool is language neutral and can be localized to different languages.</span></span> <span data-ttu-id="dda81-204">所有錯誤訊息/主控台輸出都可以當地語系化。</span><span class="sxs-lookup"><span data-stu-id="dda81-204">All error messages / console output can be localized.</span></span> <span data-ttu-id="dda81-205">不過，命令列選項仍會保留英文。</span><span class="sxs-lookup"><span data-stu-id="dda81-205">However, the command line options remain in English.</span></span>

## <a name="environment-variable"></a><span data-ttu-id="dda81-206">環境變數</span><span class="sxs-lookup"><span data-stu-id="dda81-206">Environment Variable</span></span>

<span data-ttu-id="dda81-207">WsUtil.exe 不會使用任何環境變數。</span><span class="sxs-lookup"><span data-stu-id="dda81-207">WsUtil.exe does not use any environment variables.</span></span>

## <a name="platform-independent"></a><span data-ttu-id="dda81-208">平台獨立</span><span class="sxs-lookup"><span data-stu-id="dda81-208">Platform independent</span></span>

<span data-ttu-id="dda81-209">WsUtil.exe 的輸出檔案與平臺無關。</span><span class="sxs-lookup"><span data-stu-id="dda81-209">Output files from WsUtil.exe are platform independent.</span></span> <span data-ttu-id="dda81-210">存根未產生任何架構相依程式碼;任何特定的架構都將由 C 編譯器負責處理。</span><span class="sxs-lookup"><span data-stu-id="dda81-210">There is no architecture dependent code generated in the stub; anything architecture specific will be taken care of by the C compiler.</span></span> <span data-ttu-id="dda81-211">存根可以在我們支援的所有平臺中使用。</span><span class="sxs-lookup"><span data-stu-id="dda81-211">The stub can be used in all the platforms we support.</span></span>

<span data-ttu-id="dda81-212">您可以在 [WSDL 支援](wsdl-support.md) 和 [架構支援](schema-support.md) 部分找到 wsutil.exe 輸出的描述。</span><span class="sxs-lookup"><span data-stu-id="dda81-212">Description for wsutil.exe output can be found at [WSDL support](wsdl-support.md) and [Schema support](schema-support.md) part.</span></span>

 

 




