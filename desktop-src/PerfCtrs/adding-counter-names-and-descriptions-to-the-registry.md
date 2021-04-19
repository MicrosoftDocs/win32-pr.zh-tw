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
# <a name="adding-counter-names-and-descriptions-to-the-registry"></a>將計數器名稱和描述新增至登錄

> [!IMPORTANT]
> 由於有顯著的效能和可靠性限制，提供本主題所描述的效能計數器資料的方法，可能會在未來變更或無法使用。 相反地，Microsoft 建議您使用使用 [2.0 版提供計數器資料](providing-counter-data-using-version-2-0.md) 來建立新的效能計數器，以及遷移現有的效能計數器來使用該方法所述的方法。

所有 V1 效能物件及其計數器的名稱和描述都必須安裝在系統上。 若要從 [V1 提供者](providing-counter-data.md)儲存物件和計數器的名稱和描述：

- [建立 .h 標頭檔](#creating-a-symbolic-constants-h-file) ，其中包含物件和計數器之位移的符號常數。
- [建立初始化 (。](#creating-an-initialization-ini-file) 包含字串的 INI) 檔案。
- 安裝元件時，請 [執行 **lodctr** 工具](#running-the-lodctr-tool) ，將名稱和描述安裝到登錄中。
- 卸載元件時，請執行 unlodctr 工具，以從登錄中移除名稱和描述。

## <a name="creating-a-symbolic-constants-h-file"></a> ( .h) 檔案建立符號常數

建立 .h 標頭檔，以定義提供者所提供之物件和計數器位移的常數 (宏) 。 在安裝提供者期間，會使用 .h 標頭作為 **lodctr** 的輸入，而且也可供提供者的 C/c + + 程式碼使用。

常數值必須是連續的，甚至是開頭為零的數位。 依物件將常數分組 (亦即，以物件位移開始每個群組，然後遵循該物件的計數器位移) 。

標頭中的常數會決定計數器新增至登錄中的名稱和解說文字的順序。 提供者會使用位移來判斷要查詢的物件，以及傳回資料時要使用的索引值。 如需詳細資訊，請參閱 [執行 OpenPerformanceData](implementing-openperformancedata.md)。

以下顯示的是名為 CounterOffsets 的符號常數檔案範例，用於 [建立效能延伸模組 DLL](creating-a-performance-extension-dll.md) 範例。

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

## <a name="creating-an-initialization-ini-file"></a>建立初始化 (。INI) 檔案

初始化 (。INI) 檔案包含符號檔中所定義之每個物件和計數器的名稱和說明字串。 ，.在安裝提供者期間，使用 INI 檔案作為 **lodctr** 的輸入。

，.INI 檔案應編碼為 UTF-16LE (，並以位元組順序標記) ，而且應該具有下列區段和索引鍵：

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

### <a name="info-section"></a>[資訊] 區段

此 `[info]` 區段包含關於提供者的一般資訊。 區段索引鍵的定義如下：

|Key|描述
|---|-----------
|**DriverName**| 在登錄中，指定位於登錄機碼下的提供者效能金鑰的名稱 `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` 。 如需建立此金鑰的詳細資訊，請參閱 [建立應用程式的效能金鑰](creating-the-applications-performance-key.md)。
|**SymbolFile**| 指定 .h 標頭檔，其中包含提供者物件和計數器的符號值。 在安裝期間 (叫用 **lodctr**) 時，標頭檔必須與相同的目錄。INI 檔案。
|**信任**| 如果您在一節中包含此金鑰 `[info]` ， **lodctr** 會將程式庫驗證程式代碼登錄值新增至您的效能金鑰，以及效能 DLL 的二進位簽章。 當 PERFLIB 呼叫您的 DLL 時，它會比較簽章與您的 DLL，以判斷 DLL 是否已修改。 **受信任** 金鑰的值會被忽略。

`DriverName`和索引 `SymbolFile` 鍵是必要的。

### <a name="objects-section"></a>[物件] 區段

`[objects]`區段提供提供者所支援的效能物件清單。 這是用來判斷區段中的每個符號是否 `[text]` 參考物件或計數器。

針對您的提供者支援的每個物件 (counterset) ，將一個名為的索引鍵加入 `<symbol>_<langid>_NAME=` `[objects]` 區段中，其中 `<symbol>` 是物件的名稱，而 `<langid>` 是其中一個支援語言的語言識別項。 值會被忽略。

> [!IMPORTANT]
> `[objects]`區段可改善系統的效能。 雖然 objects 區段是選擇性的，但您應該一律將此區段包含在中。INI 檔案。 如果您包含此區段，只有當您支援要求的物件時，才會呼叫您的效能 DLL。 如果您未包含物件區段，則會針對每個查詢呼叫您的 DLL，因為系統不知道您的提供者所支援的物件。 如果未包含物件區段， **lodctr** 會在應用程式事件記錄檔中產生訊息，指出。INI 檔案未包含物件區段。 此訊息的事件識別碼為2000。

### <a name="languages-section"></a>[語言] 區段

`[languages]`本節提供您的提供者提供其名稱和說明字串之每種語言的語言識別項清單。 所有提供者都應該支援 `009` (英文) 。

針對每個支援的語言，新增一個名為的金鑰 `<langid>=` 。 此值會被忽略，但針對檔用途，此值通常會設定為對應語言的名稱，例如 `009=English` 。

針對大部分的語言，您應該使用主要語言識別項。 語言識別項的完整清單位於 Winnt 標頭檔中的 [主要語言識別項] 標題下方。 將 Winnt 中找到的值轉換成3個十六進位數位的序列，方法是移除前置詞 `0x` 並加上前置 `0` 位數，直到序列的長度為3位數。 例如，若要指定 (0x9) 的英文字串，請使用009。 若要指定 (0x10) 的義大利字串，請使用010。

中文和葡萄牙文都需要主要和次要語言識別項。 使用404、804、416或816，而不是004或016。

### <a name="text-section"></a>[文字] 區段

`[text]`區段提供物件和計數器的名稱和說明字串。

針對每個物件或計數器，以及針對每個支援的語言，您必須提供名稱索引鍵 (，其中包含物件或計數器) 的名稱或標題字串，您也可以選擇性地提供說明索引鍵 (，其中包含物件或計數器) 的描述或說明字串。 索引鍵應該命名為 `<symbol>_<langid>_NAME` 和 `<symbol>_<langid>_HELP` ，其中 `<symbol>` 是物件或計數器的符號常數 (如符號常數 .h 檔) 中所定義，而且 `<langid>` 是用於此字串的語言識別項。

例如，具有符號之計數器的英文字串會 `MY_COUNTER` 指定為：

```ini
MY_COUNTER_009_NAME=My Counter
MY_COUNTER_009_HELP=Description for My Counter.
```

文字索引鍵可以依任何順序顯示。 文字字串不應包含格式化字元，例如 tab。

### <a name="example-ini-file"></a>範例 INI 檔案

以下是用來 [建立效能延伸模組 DLL](creating-a-performance-extension-dll.md) 範例的初始化檔範例。

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

## <a name="running-the-lodctr-tool"></a>執行 Lodctr 工具

載入中定義的名稱和說明字串。INI 檔案 (在提供者安裝期間) ，請從包含的資料夾執行 **lodctr** 工具。INI 檔案和標頭檔。 此工具組含在電腦中。 您必須以較高的許可權執行 **lodctr** 。 **Lodctr** 的參數是的路徑。INI 檔案。 例如： `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"` 。

若要在卸載) 期間卸載名稱和協助字串 (，請執行 **unlodctr** 工具。 您必須以較高的許可權執行 **unlodctr** 。 **Unlodctr** 的參數是提供者的 DriverName， (提供者的效能金鑰) 的名稱。 例如： `unlodctr "MyProvider"` 。

執行 **lodctr** 之前，請確定您的應用程式在 [ **服務** ] 索引鍵底下有一個專案。 如需詳細資訊，請參閱 [建立應用程式的效能金鑰](creating-the-applications-performance-key.md)。 如果機碼不存在，則 **lodctr** 不會以您的名稱和描述更新登錄。

除了執行 **lodctr** 之外，您還可以從安裝程式呼叫) Loadperf 中定義的 [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (，以載入您的計數器名稱描述。 然後，您可以在卸載期間呼叫 [**UnloadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) 。

**Lodctr** 公用程式會複製中的字串。將 INI 檔案寫入 **計數器**，**並在** 適當的語言子機碼下說明登錄值。 如果對應的語言子機碼不存在，則不會複製該語言的字串。 此公用程式也會更新 **最後一個計數器** 和 **最後一個** 說明值。 效能計數器名稱和描述會儲存在登錄中的下列位置。

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

除了在 **PerfLib** 索引鍵下新增值之外， **lodctr** 工具也會將下列值加入至應用程式的 [ **服務** ] 節點。 在大部分的情況下，應用程式和提供者將會有一對一的關係;但是，提供者可能會提供多個應用程式的計數器資料，這就是為何金鑰是以應用程式為基礎，而不是以提供者為基礎的原因。

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
