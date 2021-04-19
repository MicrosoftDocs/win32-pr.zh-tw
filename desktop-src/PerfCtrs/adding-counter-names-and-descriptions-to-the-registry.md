---
description: 所有效能物件及其計數器的名稱和描述都會儲存在登錄中。
ms.assetid: 6fdaccb0-45bc-48f2-8f63-3df0bdf1dca4
title: 將計數器名稱和描述新增至登錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d2c97ebe80a8ef2a8396ca42583cbad874859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992044"
---
# <a name="adding-counter-names-and-descriptions-to-the-registry"></a><span data-ttu-id="c3779-103">將計數器名稱和描述新增至登錄</span><span class="sxs-lookup"><span data-stu-id="c3779-103">Adding Counter Names and Descriptions to the Registry</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c3779-104">由於有顯著的效能和可靠性限制，提供本主題所描述的效能計數器資料的方法，可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="c3779-104">Due to significant performance and reliability limitations, the method for providing performance counter data that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="c3779-105">相反地，Microsoft 建議您使用使用 [2.0 版提供計數器資料](providing-counter-data-using-version-2-0.md) 來建立新的效能計數器，以及遷移現有的效能計數器來使用該方法所述的方法。</span><span class="sxs-lookup"><span data-stu-id="c3779-105">Instead, Microsoft recommends that you use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md) for creating new performance counters and that you migrate existing performance counters to use that method.</span></span>

<span data-ttu-id="c3779-106">所有 V1 效能物件及其計數器的名稱和描述都必須安裝在系統上。</span><span class="sxs-lookup"><span data-stu-id="c3779-106">The names and descriptions of all V1 performance objects and their counters must be installed the system.</span></span> <span data-ttu-id="c3779-107">若要從 [V1 提供者](providing-counter-data.md)儲存物件和計數器的名稱和描述：</span><span class="sxs-lookup"><span data-stu-id="c3779-107">To store names and descriptions for the objects and counters from your [V1 provider](providing-counter-data.md):</span></span>

- <span data-ttu-id="c3779-108">[建立 .h 標頭檔](#creating-a-symbolic-constants-h-file) ，其中包含物件和計數器之位移的符號常數。</span><span class="sxs-lookup"><span data-stu-id="c3779-108">[Create a .h header file](#creating-a-symbolic-constants-h-file) that contains the symbolic constants for the offsets to your objects and counters.</span></span>
- <span data-ttu-id="c3779-109">[建立初始化 (。](#creating-an-initialization-ini-file) 包含字串的 INI) 檔案。</span><span class="sxs-lookup"><span data-stu-id="c3779-109">[Create an initialization (.INI) file](#creating-an-initialization-ini-file) that contains the strings.</span></span>
- <span data-ttu-id="c3779-110">安裝元件時，請 [執行 **lodctr** 工具](#running-the-lodctr-tool) ，將名稱和描述安裝到登錄中。</span><span class="sxs-lookup"><span data-stu-id="c3779-110">When installing your component, [run the **lodctr** tool](#running-the-lodctr-tool) to install the names and descriptions into the registry.</span></span>
- <span data-ttu-id="c3779-111">卸載元件時，請執行 unlodctr 工具，以從登錄中移除名稱和描述。</span><span class="sxs-lookup"><span data-stu-id="c3779-111">When uninstalling your component, run the unlodctr tool to remove the names and descriptions from the registry.</span></span>

## <a name="creating-a-symbolic-constants-h-file"></a><span data-ttu-id="c3779-112"> ( .h) 檔案建立符號常數</span><span class="sxs-lookup"><span data-stu-id="c3779-112">Creating a symbolic constants (.h) file</span></span>

<span data-ttu-id="c3779-113">建立 .h 標頭檔，以定義提供者所提供之物件和計數器位移的常數 (宏) 。</span><span class="sxs-lookup"><span data-stu-id="c3779-113">Create a .h header file that defines constants (macros) for the offsets to the objects and counters that your provider provides.</span></span> <span data-ttu-id="c3779-114">在安裝提供者期間，會使用 .h 標頭作為 **lodctr** 的輸入，而且也可供提供者的 C/c + + 程式碼使用。</span><span class="sxs-lookup"><span data-stu-id="c3779-114">The .h header is used as input to **lodctr** during installation of your provider, and may also be used by the C/C++ code of your provider.</span></span>

<span data-ttu-id="c3779-115">常數值必須是連續的，甚至是開頭為零的數位。</span><span class="sxs-lookup"><span data-stu-id="c3779-115">The constant values must be consecutive, even numbers beginning with zero.</span></span> <span data-ttu-id="c3779-116">依物件將常數分組 (亦即，以物件位移開始每個群組，然後遵循該物件的計數器位移) 。</span><span class="sxs-lookup"><span data-stu-id="c3779-116">Group the constants by objects (i.e. start each group with the object offset, then follow with the offsets of the counters for that object).</span></span>

<span data-ttu-id="c3779-117">標頭中的常數會決定計數器新增至登錄中的名稱和解說文字的順序。</span><span class="sxs-lookup"><span data-stu-id="c3779-117">The constants in the header determine the order in which the counters are added to the name and help text in the registry.</span></span> <span data-ttu-id="c3779-118">提供者會使用位移來判斷要查詢的物件，以及傳回資料時要使用的索引值。</span><span class="sxs-lookup"><span data-stu-id="c3779-118">The provider uses the offsets to determine which object is being queried and the index values to use when returning the data.</span></span> <span data-ttu-id="c3779-119">如需詳細資訊，請參閱 [執行 OpenPerformanceData](implementing-openperformancedata.md)。</span><span class="sxs-lookup"><span data-stu-id="c3779-119">For details, see [Implementing OpenPerformanceData](implementing-openperformancedata.md).</span></span>

<span data-ttu-id="c3779-120">以下顯示的是名為 CounterOffsets 的符號常數檔案範例，用於 [建立效能延伸模組 DLL](creating-a-performance-extension-dll.md) 範例。</span><span class="sxs-lookup"><span data-stu-id="c3779-120">The following shows an example of a symbolic constant file, named CounterOffsets.h, that is used in the [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md) example.</span></span>

```C++
#ifndef OFFSETS_H
#define OFFSETS_H

// Symbol file that defines constant values for the objects
// and counters that the provider provides. The counters should be
// grouped by object.

#define TRANSFER_OBJECT      0 // First object must be at offset 0.
#define BYTES_SENT           2 // Counters for the object follow.
#define AVAILABLE_BANDWIDTH  4 // Offsets must be even numbers.

// Not required, but for convenience in implementing the Open function:
#define LAST_TRANSFER_OBJECT_COUNTER_OFFSET  AVAILABLE_BANDWIDTH

#define PEER_OBJECT          6 // Second object must be at the next offset.
#define BYTES_SERVED         8 // Counter for the second object.

// Not required, but for convenience in implementing the Open function:
#define LAST_PEER_OBJECT_COUNTER_OFFSET  BYTES_SERVED

#endif // OFFSETS_H
```

## <a name="creating-an-initialization-ini-file"></a><span data-ttu-id="c3779-121">建立初始化 (。INI) 檔案</span><span class="sxs-lookup"><span data-stu-id="c3779-121">Creating an initialization (.INI) file</span></span>

<span data-ttu-id="c3779-122">初始化 (。INI) 檔案包含符號檔中所定義之每個物件和計數器的名稱和說明字串。</span><span class="sxs-lookup"><span data-stu-id="c3779-122">The initialization (.INI) file contains the name and help strings for each object and counter defined in your symbol file.</span></span> <span data-ttu-id="c3779-123">，.在安裝提供者期間，使用 INI 檔案作為 **lodctr** 的輸入。</span><span class="sxs-lookup"><span data-stu-id="c3779-123">The .INI file is used as input to **lodctr** during installation of your provider.</span></span>

<span data-ttu-id="c3779-124">，.INI 檔案應編碼為 UTF-16LE (，並以位元組順序標記) ，而且應該具有下列區段和索引鍵：</span><span class="sxs-lookup"><span data-stu-id="c3779-124">The .INI file should be encoded as UTF-16LE (with byte order mark) and should have the following sections and keys:</span></span>

```ini
[info]
drivername=ServiceKeyName
symbolfile=SymbolFile.h
trusted=(Unused)

[objects]
<symbol>_<langid>_NAME=(Unused)

[languages]
<langid>=(Unused)

[text]
<symbol>_<langid>_NAME=Name
<symbol>_<langid>_HELP=Description
```

### <a name="info-section"></a><span data-ttu-id="c3779-125">[資訊] 區段</span><span class="sxs-lookup"><span data-stu-id="c3779-125">[info] section</span></span>

<span data-ttu-id="c3779-126">此 `[info]` 區段包含關於提供者的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="c3779-126">The `[info]` section contains general information about the provider.</span></span> <span data-ttu-id="c3779-127">區段索引鍵的定義如下：</span><span class="sxs-lookup"><span data-stu-id="c3779-127">The section keys are defined as follows:</span></span>

|<span data-ttu-id="c3779-128">Key</span><span class="sxs-lookup"><span data-stu-id="c3779-128">Key</span></span>|<span data-ttu-id="c3779-129">描述</span><span class="sxs-lookup"><span data-stu-id="c3779-129">Description</span></span>
|---|-----------
|<span data-ttu-id="c3779-130">**DriverName**</span><span class="sxs-lookup"><span data-stu-id="c3779-130">**DriverName**</span></span>| <span data-ttu-id="c3779-131">在登錄中，指定位於登錄機碼下的提供者效能金鑰的名稱 `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` 。</span><span class="sxs-lookup"><span data-stu-id="c3779-131">Specify the name of the provider's performance key located in the registry under the `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` key.</span></span> <span data-ttu-id="c3779-132">如需建立此金鑰的詳細資訊，請參閱 [建立應用程式的效能金鑰](creating-the-applications-performance-key.md)。</span><span class="sxs-lookup"><span data-stu-id="c3779-132">For information on creating this key, see [Creating the Application's Performance Key](creating-the-applications-performance-key.md).</span></span>
|<span data-ttu-id="c3779-133">**SymbolFile**</span><span class="sxs-lookup"><span data-stu-id="c3779-133">**SymbolFile**</span></span>| <span data-ttu-id="c3779-134">指定 .h 標頭檔，其中包含提供者物件和計數器的符號值。</span><span class="sxs-lookup"><span data-stu-id="c3779-134">Specify the .h header file that contains symbolic values of your provider's objects and counters.</span></span> <span data-ttu-id="c3779-135">在安裝期間 (叫用 **lodctr**) 時，標頭檔必須與相同的目錄。INI 檔案。</span><span class="sxs-lookup"><span data-stu-id="c3779-135">During installation (when invoking **lodctr**), the header file must be in the same directory as the .INI file.</span></span>
|<span data-ttu-id="c3779-136">**信任**</span><span class="sxs-lookup"><span data-stu-id="c3779-136">**Trusted**</span></span>| <span data-ttu-id="c3779-137">如果您在一節中包含此金鑰 `[info]` ， **lodctr** 會將程式庫驗證程式代碼登錄值新增至您的效能金鑰，以及效能 DLL 的二進位簽章。</span><span class="sxs-lookup"><span data-stu-id="c3779-137">If you include this key in the `[info]` section, **lodctr** will add a Library Validation Code registry value to your performance key with a binary signature of your performance DLL.</span></span> <span data-ttu-id="c3779-138">當 PERFLIB 呼叫您的 DLL 時，它會比較簽章與您的 DLL，以判斷 DLL 是否已修改。</span><span class="sxs-lookup"><span data-stu-id="c3779-138">When PERFLIB calls your DLL it compares the signature with your DLL to determine if the DLL has been modified.</span></span> <span data-ttu-id="c3779-139">**受信任** 金鑰的值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="c3779-139">The value of the **Trusted** key is ignored.</span></span>

<span data-ttu-id="c3779-140">`DriverName`和索引 `SymbolFile` 鍵是必要的。</span><span class="sxs-lookup"><span data-stu-id="c3779-140">The `DriverName` and `SymbolFile` keys are required.</span></span>

### <a name="objects-section"></a><span data-ttu-id="c3779-141">[物件] 區段</span><span class="sxs-lookup"><span data-stu-id="c3779-141">[objects] section</span></span>

<span data-ttu-id="c3779-142">`[objects]`區段提供提供者所支援的效能物件清單。</span><span class="sxs-lookup"><span data-stu-id="c3779-142">The `[objects]` section provides a list of the performance objects that the provider supports.</span></span> <span data-ttu-id="c3779-143">這是用來判斷區段中的每個符號是否 `[text]` 參考物件或計數器。</span><span class="sxs-lookup"><span data-stu-id="c3779-143">This is used to determine whether each symbol from the `[text]` section refers an object or a counter.</span></span>

<span data-ttu-id="c3779-144">針對您的提供者支援的每個物件 (counterset) ，將一個名為的索引鍵加入 `<symbol>_<langid>_NAME=` `[objects]` 區段中，其中 `<symbol>` 是物件的名稱，而 `<langid>` 是其中一個支援語言的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="c3779-144">For each object (counterset) supported by your provider, add one key named `<symbol>_<langid>_NAME=` to the `[objects]` section, where `<symbol>` is the name of the object and `<langid>` is the language id of one of the supported languages.</span></span> <span data-ttu-id="c3779-145">值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="c3779-145">The value is ignored.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c3779-146">`[objects]`區段可改善系統的效能。</span><span class="sxs-lookup"><span data-stu-id="c3779-146">The `[objects]` section improves the performance of the system.</span></span> <span data-ttu-id="c3779-147">雖然 objects 區段是選擇性的，但您應該一律將此區段包含在中。INI 檔案。</span><span class="sxs-lookup"><span data-stu-id="c3779-147">Although the objects section is optional, you should always include this section in your .INI file.</span></span> <span data-ttu-id="c3779-148">如果您包含此區段，只有當您支援要求的物件時，才會呼叫您的效能 DLL。</span><span class="sxs-lookup"><span data-stu-id="c3779-148">If you include this section, your performance DLL is called only if you support the requested object.</span></span> <span data-ttu-id="c3779-149">如果您未包含物件區段，則會針對每個查詢呼叫您的 DLL，因為系統不知道您的提供者所支援的物件。</span><span class="sxs-lookup"><span data-stu-id="c3779-149">If you do not include the objects section, your DLL is called for every query because the system does not know which objects your provider supports.</span></span> <span data-ttu-id="c3779-150">如果未包含物件區段， **lodctr** 會在應用程式事件記錄檔中產生訊息，指出。INI 檔案未包含物件區段。</span><span class="sxs-lookup"><span data-stu-id="c3779-150">If the object section is not included, **lodctr** generates a message in the application event log stating that the .INI file did not contain an objects section.</span></span> <span data-ttu-id="c3779-151">此訊息的事件識別碼為2000。</span><span class="sxs-lookup"><span data-stu-id="c3779-151">The event identifier of this message is 2000.</span></span>

### <a name="languages-section"></a><span data-ttu-id="c3779-152">[語言] 區段</span><span class="sxs-lookup"><span data-stu-id="c3779-152">[languages] section</span></span>

<span data-ttu-id="c3779-153">`[languages]`本節提供您的提供者提供其名稱和說明字串之每種語言的語言識別項清單。</span><span class="sxs-lookup"><span data-stu-id="c3779-153">The `[languages]` section provides a list of the language identifiers of each language for which your provider supplies name and help strings.</span></span> <span data-ttu-id="c3779-154">所有提供者都應該支援 `009` (英文) 。</span><span class="sxs-lookup"><span data-stu-id="c3779-154">All providers should support `009` (English).</span></span>

<span data-ttu-id="c3779-155">針對每個支援的語言，新增一個名為的金鑰 `<langid>=` 。</span><span class="sxs-lookup"><span data-stu-id="c3779-155">For each supported language, add one key named `<langid>=`.</span></span> <span data-ttu-id="c3779-156">此值會被忽略，但針對檔用途，此值通常會設定為對應語言的名稱，例如 `009=English` 。</span><span class="sxs-lookup"><span data-stu-id="c3779-156">The value is ignored, but for documentation purposes the value is normally set to the name of the corresponding language, e.g. `009=English`.</span></span>

<span data-ttu-id="c3779-157">針對大部分的語言，您應該使用主要語言識別項。</span><span class="sxs-lookup"><span data-stu-id="c3779-157">For most languages, you should use the primary language identifier.</span></span> <span data-ttu-id="c3779-158">語言識別項的完整清單位於 Winnt 標頭檔中的 [主要語言識別項] 標題下方。</span><span class="sxs-lookup"><span data-stu-id="c3779-158">The complete list of language identifiers is in the Winnt.h header file, under the heading "Primary Language Ids."</span></span> <span data-ttu-id="c3779-159">將 Winnt 中找到的值轉換成3個十六進位數位的序列，方法是移除前置詞 `0x` 並加上前置 `0` 位數，直到序列的長度為3位數。</span><span class="sxs-lookup"><span data-stu-id="c3779-159">Convert the value found in Winnt.h into a sequence of 3 hexadecimal digits by removing the `0x` prefix and adding leading `0` digits until the sequence is 3 digits long.</span></span> <span data-ttu-id="c3779-160">例如，若要指定 (0x9) 的英文字串，請使用009。</span><span class="sxs-lookup"><span data-stu-id="c3779-160">For example, to specify English strings (0x9), use 009.</span></span> <span data-ttu-id="c3779-161">若要指定 (0x10) 的義大利字串，請使用010。</span><span class="sxs-lookup"><span data-stu-id="c3779-161">To specify Italian strings (0x10), use 010.</span></span>

<span data-ttu-id="c3779-162">中文和葡萄牙文都需要主要和次要語言識別項。</span><span class="sxs-lookup"><span data-stu-id="c3779-162">Chinese and Portuguese languages require both the primary and sublanguage identifiers.</span></span> <span data-ttu-id="c3779-163">使用404、804、416或816，而不是004或016。</span><span class="sxs-lookup"><span data-stu-id="c3779-163">Use 404, 804, 416, or 816 instead of 004 or 016.</span></span>

### <a name="text-section"></a><span data-ttu-id="c3779-164">[文字] 區段</span><span class="sxs-lookup"><span data-stu-id="c3779-164">[text] section</span></span>

<span data-ttu-id="c3779-165">`[text]`區段提供物件和計數器的名稱和說明字串。</span><span class="sxs-lookup"><span data-stu-id="c3779-165">The `[text]` section provides the name and help strings for your objects and counters.</span></span>

<span data-ttu-id="c3779-166">針對每個物件或計數器，以及針對每個支援的語言，您必須提供名稱索引鍵 (，其中包含物件或計數器) 的名稱或標題字串，您也可以選擇性地提供說明索引鍵 (，其中包含物件或計數器) 的描述或說明字串。</span><span class="sxs-lookup"><span data-stu-id="c3779-166">For each object or counter, and for each supported language, you must provide a NAME key (containing the name or title string for your object or counter) and you may optionally provide a HELP key (containing the description or explanation string for your object or counter).</span></span> <span data-ttu-id="c3779-167">索引鍵應該命名為 `<symbol>_<langid>_NAME` 和 `<symbol>_<langid>_HELP` ，其中 `<symbol>` 是物件或計數器的符號常數 (如符號常數 .h 檔) 中所定義，而且 `<langid>` 是用於此字串的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="c3779-167">The keys should be named `<symbol>_<langid>_NAME` and `<symbol>_<langid>_HELP`, where `<symbol>` is the symbolic constant for the object or counter (as defined in the symbolic constant .h file), and `<langid>` is the language identifier used for this string.</span></span>

<span data-ttu-id="c3779-168">例如，具有符號之計數器的英文字串會 `MY_COUNTER` 指定為：</span><span class="sxs-lookup"><span data-stu-id="c3779-168">For example, the English strings for a counter with symbol `MY_COUNTER` would be specified as:</span></span>

```ini
MY_COUNTER_009_NAME=My Counter
MY_COUNTER_009_HELP=Description for My Counter.
```

<span data-ttu-id="c3779-169">文字索引鍵可以依任何順序顯示。</span><span class="sxs-lookup"><span data-stu-id="c3779-169">The text keys can appear in any order.</span></span> <span data-ttu-id="c3779-170">文字字串不應包含格式化字元，例如 tab。</span><span class="sxs-lookup"><span data-stu-id="c3779-170">The text strings should not contain formatting characters such as tabs.</span></span>

### <a name="example-ini-file"></a><span data-ttu-id="c3779-171">範例 INI 檔案</span><span class="sxs-lookup"><span data-stu-id="c3779-171">Example INI file</span></span>

<span data-ttu-id="c3779-172">以下是用來 [建立效能延伸模組 DLL](creating-a-performance-extension-dll.md) 範例的初始化檔範例。</span><span class="sxs-lookup"><span data-stu-id="c3779-172">The following is an example of an initialization file that is used in the [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md) sample.</span></span>

```ini
[info]
drivername=MyApplication
symbolfile=CounterOffsets.h
trusted=

[objects]
TRANSFER_OBJECT_009_NAME=
PEER_OBJECT_009_NAME=

[languages]
009=English
00C=French

[text]

// English strings

TRANSFER_OBJECT_009_NAME=Transfer
TRANSFER_OBJECT_009_HELP=Provides information related to transferring files.

BYTES_SENT_009_NAME=Bytes Sent
BYTES_SENT_009_HELP=Number of bytes sent in the last transfer.

AVAILABLE_BANDWIDTH_009_NAME=Available Bandwidth
AVAILABLE_BANDWIDTH_009_HELP=Available bandwidth on the network, in bytes.

PEER_OBJECT_009_NAME=Peer
PEER_OBJECT_009_HELP=Provides information related to peer-caching.

BYTES_SERVED_009_NAME=Bytes Served
BYTES_SERVED_009_HELP=Number of bytes served from the cache.

// French strings

TRANSFER_OBJECT_00C_NAME=Transfert
TRANSFER_OBJECT_00C_HELP=Fournit des informations liées aux transferts de fichiers.

BYTES_SENT_00C_NAME=Octets Envoyés
BYTES_SENT_00C_HELP=Nombre d'octets envoyés dans le dernier transfert.

AVAILABLE_BANDWIDTH_00C_NAME=Bande Passante Disponible
AVAILABLE_BANDWIDTH_00C_HELP=Bande passante disponible sur le réseau, en octets.

PEER_OBJECT_00C_NAME=Pair
PEER_OBJECT_00C_HELP=Fournit des informations liées é mise en cache homologue.

BYTES_SERVED_00C_NAME=Octets Servis
BYTES_SERVED_00C_HELP=Le nombre d'octets servis du cache.
```

## <a name="running-the-lodctr-tool"></a><span data-ttu-id="c3779-173">執行 Lodctr 工具</span><span class="sxs-lookup"><span data-stu-id="c3779-173">Running the Lodctr tool</span></span>

<span data-ttu-id="c3779-174">載入中定義的名稱和說明字串。INI 檔案 (在提供者安裝期間) ，請從包含的資料夾執行 **lodctr** 工具。INI 檔案和標頭檔。</span><span class="sxs-lookup"><span data-stu-id="c3779-174">To load the names and help strings defined in your .INI file (during the installation of your provider), run the **lodctr** tool from the folder that contains your .INI file and header file.</span></span> <span data-ttu-id="c3779-175">此工具組含在電腦中。</span><span class="sxs-lookup"><span data-stu-id="c3779-175">The tool is included with the computer.</span></span> <span data-ttu-id="c3779-176">您必須以較高的許可權執行 **lodctr** 。</span><span class="sxs-lookup"><span data-stu-id="c3779-176">You must run **lodctr** with elevated privileges.</span></span> <span data-ttu-id="c3779-177">**Lodctr** 的參數是的路徑。INI 檔案。</span><span class="sxs-lookup"><span data-stu-id="c3779-177">The parameter to **lodctr** is the path to your .INI file.</span></span> <span data-ttu-id="c3779-178">例如： `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"` 。</span><span class="sxs-lookup"><span data-stu-id="c3779-178">For example, `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.</span></span>

<span data-ttu-id="c3779-179">若要在卸載) 期間卸載名稱和協助字串 (，請執行 **unlodctr** 工具。</span><span class="sxs-lookup"><span data-stu-id="c3779-179">To unload the names and help strings (during uninstall), run the **unlodctr** tool.</span></span> <span data-ttu-id="c3779-180">您必須以較高的許可權執行 **unlodctr** 。</span><span class="sxs-lookup"><span data-stu-id="c3779-180">You must run **unlodctr** with elevated privileges.</span></span> <span data-ttu-id="c3779-181">**Unlodctr** 的參數是提供者的 DriverName， (提供者的效能金鑰) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3779-181">The parameter to **unlodctr** is the DriverName of your provider (the name of the provider's performance key).</span></span> <span data-ttu-id="c3779-182">例如： `unlodctr "MyProvider"` 。</span><span class="sxs-lookup"><span data-stu-id="c3779-182">For example, `unlodctr "MyProvider"`.</span></span>

<span data-ttu-id="c3779-183">執行 **lodctr** 之前，請確定您的應用程式在 [ **服務** ] 索引鍵底下有一個專案。</span><span class="sxs-lookup"><span data-stu-id="c3779-183">Before running **lodctr**, be sure that your application has an entry under the **Services** key.</span></span> <span data-ttu-id="c3779-184">如需詳細資訊，請參閱 [建立應用程式的效能金鑰](creating-the-applications-performance-key.md)。</span><span class="sxs-lookup"><span data-stu-id="c3779-184">For details, see [Creating the Application's Performance Key](creating-the-applications-performance-key.md).</span></span> <span data-ttu-id="c3779-185">如果機碼不存在，則 **lodctr** 不會以您的名稱和描述更新登錄。</span><span class="sxs-lookup"><span data-stu-id="c3779-185">If the key does not exist, **lodctr** will not update the registry with your names and descriptions.</span></span>

<span data-ttu-id="c3779-186">除了執行 **lodctr** 之外，您還可以從安裝程式呼叫) Loadperf 中定義的 [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (，以載入您的計數器名稱描述。</span><span class="sxs-lookup"><span data-stu-id="c3779-186">As an alternative to running **lodctr**, you can call [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (defined in Loadperf.h) from your installation program to load your counter names descriptions.</span></span> <span data-ttu-id="c3779-187">然後，您可以在卸載期間呼叫 [**UnloadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) 。</span><span class="sxs-lookup"><span data-stu-id="c3779-187">You can then call [**UnloadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) during uninstall.</span></span>

<span data-ttu-id="c3779-188">**Lodctr** 公用程式會複製中的字串。將 INI 檔案寫入 **計數器**，**並在** 適當的語言子機碼下說明登錄值。</span><span class="sxs-lookup"><span data-stu-id="c3779-188">The **lodctr** utility copies the strings from the .INI file to the **Counters** and **Help** registry values under the appropriate language subkeys.</span></span> <span data-ttu-id="c3779-189">如果對應的語言子機碼不存在，則不會複製該語言的字串。</span><span class="sxs-lookup"><span data-stu-id="c3779-189">If the corresponding language subkey does not exist, the strings for that language are not copied.</span></span> <span data-ttu-id="c3779-190">此公用程式也會更新 **最後一個計數器** 和 **最後一個** 說明值。</span><span class="sxs-lookup"><span data-stu-id="c3779-190">The utility also updates the **Last Counter** and **Last Help** value.</span></span> <span data-ttu-id="c3779-191">效能計數器名稱和描述會儲存在登錄中的下列位置。</span><span class="sxs-lookup"><span data-stu-id="c3779-191">The performance counter names and descriptions are stored in the following location in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   \SOFTWARE
      \Microsoft
         \Windows NT
            \CurrentVersion
               \Perflib
                  Last Counter = highest counter index
                  Last Help = highest help index
                  \009
                     Counters = 2 System 4 Memory...
                     Help = 3 The System Object Type...
                  \supported language, other than English
                     Counters = ...
                     Help = ...
```

<span data-ttu-id="c3779-192">除了在 **PerfLib** 索引鍵下新增值之外， **lodctr** 工具也會將下列值加入至應用程式的 [ **服務** ] 節點。</span><span class="sxs-lookup"><span data-stu-id="c3779-192">In addition to adding values under the **PerfLib** key, the **lodctr** tool also adds the following values to the **Services** node for the application.</span></span> <span data-ttu-id="c3779-193">在大部分的情況下，應用程式和提供者將會有一對一的關係;但是，提供者可能會提供多個應用程式的計數器資料，這就是為何金鑰是以應用程式為基礎，而不是以提供者為基礎的原因。</span><span class="sxs-lookup"><span data-stu-id="c3779-193">In most cases, the application and provider will have a one-to-one relationship; however, it is possible for a provider to provide counter data for multiple applications, which is why the key is based on the application and not the provider.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \MyApplication
               \Performance
                  First Counter = lowest counter index assigned to provider
                  First Help = lowest help index assigned to provider
                  Last Counter = highest counter index assigned to provider
                  Last Help = highest help index assigned to provider
                  Object List = list of object index values if the .INI includes the [objects] section
                  Library Validation Code = if the [info] section contains a "trusted" key
```
