---
description: 本文提供控制 Flow 在 PE 映射中防護中繼資料的額外詳細資料。
title: PE 中繼資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2bce23a94629900f8610cf3cbc1e2ba0db1c4e6a079bd5f610be230df24ec6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994487"
---
# <a name="pe-metadata"></a>PE 中繼資料

本文提供控制 Flow 保護 PE 映射中的 (CFG) 中繼資料的其他詳細資料。 假設您熟悉 PE 映射中的 CFG 元資料結構。 請參閱 [Pe 格式](../debug/pe-format.md) 主題，以取得 pe 映射中 CFG 中繼資料的高階檔集。

- 有效間接呼叫目標的函式會列在附加至 load configuration 目錄的 **GuardCFFunctionTable** 中，有時也稱為 **GFIDS** 資料表，以求簡潔。 這是已排序的相對虛擬位址清單 (RVA) ，其中包含有效的 CFG 呼叫目標的相關資訊。 一般來說，這些都是定址的函式符號。 想要進行 CFG 強制的映射必須列舉其 **GFIDS** 資料表中的所有位址取得函式符號。 **GFIDS** 資料表中的 RVA 清單必須正確地排序，否則不會載入映射。 **GFIDS** 資料表是 4 + *n* 位元組的陣列，其中 *n* 是由 ( (GuardFlags & IMAGE_GUARD_CF_FUNCTION_TABLE_SIZE_MASK)  >> IMAGE_GUARD_CF_FUNCTION_TABLE_SIZE_SHIFT) 指定。 "GuardFlags" 是 load configuration 目錄的 GuardFlags 欄位。 這可讓您在未來將額外的中繼資料附加至 CFG 呼叫目標。 唯一定義的中繼資料是選擇性的1位元組額外旗標欄位 ( 「GFIDS 旗標」 ) 如果有任何呼叫目標具有中繼資料，則會附加至每個 **GFIDS** 專案。 已定義兩個 **GFIDS** 旗標：
  
  | &nbsp; | &nbsp; |
  | ---- |:---- |
  | IMAGE_GUARD_FLAG_FID_SUPPRESSED/0x1 | 明確地隱藏呼叫目標 (請勿將它視為適用于 CFG 的用途)  |
  | IMAGE_GUARD_FLAG_EXPORT_SUPPRESSED/0x2 | 已抑制匯出的呼叫目標。 如需詳細資料，請參閱 [匯出隱藏](#export-suppression) 專案 |
  
  基於未來的相容性，工具不應該設定尚未定義的 **GFIDS** 旗標，且不應包含超過目前定義之1位元組的額外 **GFIDS** 額外中繼資料位元組，因為其他旗標的意義或尚未指派其他中繼資料。 您可以藉由傾印二進位檔的 **GFIDS** 資料表（例如 Ntdll.dll 在新式 Windows 10 作業系統版本上，找到包含額外中繼資料位元組的映射範例。

  工具只能將函式符號宣告為有效的呼叫目標，可能會針對可能會取得標籤的組合程式碼考慮其他考慮。 基於歷史原因，組合器程式碼可能依賴 PROC 或. altentry 以外的程式碼標籤，而不是由連結器轉換成 CFG 呼叫目標。

  此外，基於歷史原因，程式碼可能會刻意將程式碼宣告為數據，以避免包含在 **GFIDS** 資料表中。 例如，一個物件檔案可能會將符號實作為程式碼，而另一個則會將它宣告為數據，以便取得符號的位址，而不會產生有效的 CFG 目標記錄。 為了提供相容性，建議工具組支援這種作法。

- 支援 CFG 以及需要或執行 CFG 檢查的映射應該設定 IMAGE_GUARD_CF_INSTRUMENTED 和 IMAGE_GUARD_CF_FUNCTION_TABLE_PRESENT GuardFlags 位，而且應該在映射標頭中設定 IMAGE_DLLCHARACTERISTICS_GUARD_CF DllCharacteristics 位。

- Load configuration 目錄會通告兩個函式指標： GuardCFCheckFunctionPointer 和 GuardCFDispatchFunctionPointer (後者僅支援 AMD64) 等特定架構。 這些函式指標應指向唯讀的記憶體，以使 CFG 安全性生效;作業系統的 DLL 載入器會在映射載入期間重新保護記憶體暫時，以儲存函式指標。 一般用法可能是將這些內容合併到包含匯入位址資料表的相同區段， (IAT) 。 GuardCFCheckFunctionPointer 會提供作業系統載入器所提供符號的位址，該符號可使用第一個整數引數暫存器中的函式指標來呼叫 (ECX 在 x86) 上會傳回成功，如果呼叫目標不是有效的 CFG 目標，則會中止進程。 GuardCFDispatchFunctionPointer 會提供作業系統載入器所提供符號的位址，此符號會接受 register RAX 中的呼叫目標，並執行結合的 CFG 檢查和對呼叫目標的尾分支優化呼叫 (登錄 R4-r10/R11 會保留供 GuardCFDispatchFunctionPointer 使用，而整數引數暫存器則保留供最終呼叫目標) 使用。 映射中 CFG 符號的預設位址應該指向一個函式，該函式只會傳回 (GuardCFCheckFunctionPointer) 或傳回防護隱藏符號 (或最好從執行 "jmp rax" 指令的 **GFIDS** 資料表符號) 完全省略。 針對 AMD64 GuardCFDispatchFunctionPointer，當映射在 CFG 感知的作業系統上載入，而 CFG 已啟用時，OS DLL 載入器會安裝適當的函式指標，進而提供回溯相容性。 如果映射不打算使用 CFG 分派設備，則映射可以為負載設定中的 GuardCFDispatchFunctionPointer 提供0。 這應該針對非 AMD64 架構進行，以供未來相容，以防這些架構最終以某種形式支援 CFG 分派機制。 請注意，Windows 8.1 AMD64 不支援 CFG 分派，而且會保留 GuardCFDispatchFunctionPointer 的預設函式指標。 只有 Windows 10 和更新版本的作業系統才支援 CFG 分派。

- 使用者模式 CFG 可能只會針對標示為位址空間配置隨機載入的影像強制執行 (ASLR) 相容 (由/DYNAMICBASE 選項指定為 Microsoft 連結器) 。 這是因為作業系統會在內部處理 CFG，其中基本上是連接到 ASLR 基礎結構。 一般而言，CFG 的使用者應該在第一個步驟中啟用其映射的 ASLR。 工具不應假設作業系統一律會忽略未設定 ASLR 的 CFG，但通常應該同時設定兩者。

## <a name="compiler-directives"></a>編譯器指示詞

- 您可以使用 __declspec (防護 (隱藏) ) 修飾詞，或使用適用于 asm 程式碼的/guardsym： symname，S 連結器指示詞 (（例如) ），將呼叫目標標示為明確隱藏。 這會導致呼叫目標包含在 **GFIDS** 資料表中，但會以作業系統將呼叫目標視為不正確方式進行標示。 某些非生產案例（例如，在某些較舊的作業系統上啟用特定的 application verifier instrumentation）可以讓隱藏的呼叫目標被視為有效，但在一般情況下，這些案例都不應該是生產案例。 這個指示詞適用于批註「危險」的函式，這些函式不應該視為有效的呼叫目標，即使一般的 CFG 規則會包含它們也一樣。

- 程式碼可以使用 __declspec (guard (nocf) ) 修飾詞來表示不需要 CFG 檢查。 這會指示編譯器不要插入整個函數的任何 CFG 檢查。 編譯器應該小心將這個指示詞傳播至內嵌函式所提供的任何程式碼，該函式會標示為不需要 CFG 檢查。 這種方法通常只會在程式設計師手動插入「CFG 相等」保護的特定情況下使用。 程式設計師知道這些函式是透過一些唯讀的函式資料表來呼叫，其位址是透過唯讀記憶體參考取得，而其索引已遮罩至函式資料表的限制。 這種方法也可以套用至不是內嵌的小型包裝函式，而不是透過函式指標進行呼叫。 由於這個指示詞的使用不正確可能會危及 CFG 的安全性，因此程式設計人員必須非常小心地使用指示詞。 一般來說，這種使用方式僅限於只呼叫一個函式的非常小函式。

## <a name="import-handling"></a>匯入處理

- 透過 IAT 的呼叫不應使用 CFG 保護。 此 IAT 在新式映射中是唯讀的 (假設 IAT 是在 PE 標頭中宣告的，在這種情況下，它必須在自己的頁面上) 。 IAT 可用來觸達防護隱藏的函式，因此這是正確性需求。 透過 IAT 的唯讀記憶體保護會取代 CFG，因為在解析映射匯入快照之後，呼叫目標系結是不可變的，且系結解析更精細。

- 受保護的延遲載入：透過延遲載入 IAT 的呼叫不應使用 CFG 保護，原因與標準 IAT 相同。 延遲載入 IAT 應該在它自己的區段中，而影像應設定 IMAGE_GUARD_CF_PROTECT_DELAYLOAD_IAT GuardFlags 位。 這表示如果使用作業系統的延遲負載支援 Windows 8 和更新版本的作業系統，作業系統的 DLL 載入器應該會在匯出解析期間變更延遲載入 IAT 的保護。 如果原生作業系統延遲負載支援正在使用中，則此步驟的同步處理是由作業系統 DLL 載入器所管理 (例如 ResolveDelayLoadedAPI) 因此，其他元件都不應該重新保護頁面跨越宣告的延遲載入 IAT。 為了與舊版預先配置的作業系統相容，工具可能會啟用將延遲載入 IAT 移至其專屬區段的選項 (標準方式 ". didat" ) 、在映射標頭中受保護為讀取/寫入，以及另外設定 IMAGE_GUARD_CF_DELAYLOAD_IAT_IN_ITS_OWN_SECTION 旗標。 這種設定會讓 CFG 感知作業系統 DLL 載入器重新保護包含 IMAGE_DIRECTORY_ENTRY_DELAY_IMPORT 資料表的整個區段，以在映射載入期間讀取記憶體。 如果您不在意在早 CFG 支援的作業系統上執行映射，但工具應根據映射所需的最低作業系統支援來進行決策，則可能不需要將延遲載入 IAT 放在其本身區段中的選項。

  如果映射未使用作業系統的原生延遲載入支援，它仍可設定受保護的延遲載入相關 GuardFlags 位。 在此設定中，作業系統載入器只會在執行時間提供支援來保護延遲載入 IAT 為唯讀（如果平臺支援），而且會成為映射內部延遲載入解析存根的責任，以同步處理和管理延遲載入 IAT 的保護。 如果載入設定資料表是儲存在唯讀記憶體中 (這是建議的) ，則在影像的 GuardFlags 欄位中，受保護的延遲載入 IAT 位是否存在，可能會很有用，因為它會作為影像內部延遲載入解析存根的內部提示，以指出它是否應該保護延遲載入 IAT。

  如果已啟用 CFG，建議您預設啟用受保護的延遲載入。 在較舊的作業系統版本上執行，且使用作業系統原生延遲負載支援的影像（如所述），可能會在其本身的區段支援中使用延遲載入 IAT，以提供回溯相容性。 這並不是將延遲載入 IAT 標示為唯讀，並將其與另一個區段合併，而這會在較舊的作業系統上中斷，而不了解受保護的延遲負載，並提供原生延遲載入解析支援。 所有 Windows 10 版本和第一個 Windows 8.1/Windows Server 2012 R2 會建立支援的 CFG (表示2014年11月更新) 引進作業系統中受保護延遲負載的支援。

## <a name="function-alignment"></a>函數對齊

- 如果有可能的話， **GFIDS** 資料表中所採用的函式，也應以16位元組對齊。 這可能並非永遠可行。 例如，如果非 COMDAT 函式是由非 CFG 感知工具組合成一個單位（某些組合器可能會產生），則產生檔案之工具的使用者必須適當地設定對齊。 在此情況下，工具可能會選擇發出診斷警告，讓使用者可以採取適當的更正動作。 這是因為 CFG 會將呼叫目標標示為有效，或在16位元組的界限上無效，以提升快速 CFG 檢查的效率。 如果函式不是16位元組對齊，則整個16位元組位置必須標記為有效，因為您無法在不是函式開頭的程式碼中進行呼叫，所以它不是安全的。 當您第一次為專案帶來 CFG 時，支援此案例以簡化互通性。 非 CFG 感知映射會同樣標示為適用于相容性的任何呼叫目標對齊。 同樣地，具有不當的呼叫目標可減少 CFG 的安全性優點，因此當映射需要 CFG 時，工具應該會針對 **GFIDS** 資料表中的任何事物，自動對齊16位元組的界限。 不在 **GFIDS** 資料表中的符號不需要針對 CFG 進行特定的對齊。

## <a name="export-suppression"></a>匯出隱藏專案

- CFG 匯出隱藏 (CFG ES) 是一種選擇性模式，可讓處理常式指出只因為它們是 dllexport 符號，而且尚未由 GetProcAddress 動態解決的呼叫目標，將會被視為不適用於 CFG 的用途。 這樣可減少系統 DLL 匯出的 CFG 介面區。 匯出隱藏專案牽涉到使用 IMAGE_GUARD_FLAG_EXPORT_SUPPRESSED **GFIDS** 旗標加以標記，以傳達合格的「匯出隱藏」 dllexport 呼叫目標。 Dllexport 符號和 PE 映射進入點應隱含地被視為產生 **GFIDS** 資料表所使用的工具所採用的位址。  如果匯出符號的對齊是16位元組，而不是使用 dllexport 的其他原因，則可以使用函式資料表中的「匯出隱藏的 **GFIDS** 旗標來標示。 未對齊16位元組的呼叫目標 **不** 能以 IMAGE_GUARD_FLAG_EXPORT_SUPPRESSED **GFIDS** 旗標標記，也無法限制為只在 GetProcAddress 時動態啟用為有效的呼叫目標。

  支援 CFG ES 的映射包含 GuardAddressTakenIatEntryTable，其計數會由 GuardAddressTakenIatEntryCount 提供作為其 load configuration 目錄的一部分。 此資料表的結構格式與 **GFIDS** 資料表相同。 它會使用相同的 GuardFlags IMAGE_GUARD_CF_FUNCTION_TABLE_SIZE_MASK 機制，將 address 所取得的額外選擇性中繼資料位元組編碼，但在取得 IAT 資料表的位址中，所有中繼資料位元組都必須是零，而且會保留。 取得的位址 IAT 資料表表示匯入 Thunk 的已排序陣列，其匯入為取得呼叫目標的符號位址。 此結構可支援存在於遠端模組中的位址符號，以及使用 CFG ES 的 dllexports。 這類程式碼結構的範例如下：

  ```
  mov rcx, [__imp_DefWindowProc]
  call foo ; where foo takes the actual address of DefWindowProc.
  ```

  所有採用匯入 Thunk 的位址都必須加以列舉，以便作業系統載入器可以找到它們，並且在載入影像和貼上其匯入時，讓適當的呼叫目標有效。 如果沒有所採取的匯入 Thunk，資料表和計數可以是0。

  模組會設定 IMAGE_GUARD_CF_EXPORT_SUPPRESSION_INFO_PRESENT GuardFlags 位，以指出它已列舉位址取得 IAT 資料表中的所有位址，並以 IMAGE_GUARD_FLAG_EXPORT_SUPPRESSED **GFIDS** 旗標標示符合 CFG ES 資格的所有匯出。 請注意，可能會有零個這類 Thunk，而且可能也有零個這類 dllexport 符號。 無法維護取得的位址 IAT 資料表可能是正確性問題，因為某些呼叫目標在載入 DLL 時可能無法有效。

  模組會設定 IMAGE_GUARD_CF_ENABLE_EXPORT_SUPPRESSION GuardFlags 位，表示它想要為進程啟用 CFG ES。 在實務上，這對目前只有 Exe 有意義。 啟用 CFG ES 的進程不應載入未使用 CFG ES 或執行時間失敗的 Dll，因為 undesignated 位址會取得 IAT 符號。 啟用 cfg ES 的支援應為啟用 CFG 的個別加入宣告選項。 根據預設，提供 CFG ES 中繼資料是安全的，且預設為使用 CFG，不過工具組必須小心確保它們會產生正確的中繼資料。 如果沒有，則其產生的映射可能無法在 CFG ES 進程中正確執行。 您應在強制執行 CFG ES 的測試程式中徹底測試這類支援。 作業系統內建的系統 dll 支援可瞭解 cfg es 之新式 Windows 10 作業系統版本的 CFG es 中繼資料。 這項支援之前的作業系統版本並不瞭解 CFG ES，而且會忽略映射中任何 CFG ES 相關的指示詞。 這類映射仍可回溯相容于較舊的作業系統版本。

  從工具組的角度來看，CFG ES 支援是選擇性的，但建議工具組至少包含列舉足夠的資訊，以便在需要 CFG ES 的進程中執行影像。 如前所述，工具組支援經過徹底測試，以確保它與 CFG ES 相容，因為大部分的處理常式尚未啟用 CFG ES。

## <a name="exception-handling-and-unwinding"></a>例外狀況處理和回溯

- .Pdata 註冊中的例外狀況處理常式資訊所指定的語言特定處理常式（例如 __C_specific_handler），不應該在 **GFIDS** 資料表中標示為有效的呼叫目標。 您可以藉由遍歷唯讀記憶體來查閱它們。 同樣地，Microsoft C 語言特定處理常式會使用唯讀記憶體搜尋來找出例外狀況處理常式的 funclets，因此不會在 **GFIDS** 資料表中將其 funclets 宣告為有效的呼叫目標。

- 長期跳躍處理 (針對非 x86 目標（例如 AMD64) ）：使用 CFG 編譯的工具組和支援的 setjmp () /longjmp () 應該將長跳躍的時間實作為「安全的長跳躍」，以與結構化例外狀況處理 (SEH) 互通。 這表示長跳躍會實作為呼叫 RtlUnwindEx，並以 STATUS_LONGJUMP 作為提供的例外狀況記錄中的狀態碼，以及 ExceptionInformation [0] 指向的標準 _JUMP_BUFFER。 跳躍回溯目標應該是回溯的 TargetIp。 跳躍緩衝區代表當長時間跳躍完成之後，作業系統還原的註冊內容。 RtlUnwind (例如，使用 STATUS_LONGJUMP 所呼叫的) 具有 CFG 特有的特殊意義。 長跳躍目標 (_JUMP_BUFFER。Rip 或 _JUMP_BUFFER。ARM64 上的 Lr) 是在作業系統于唯讀記憶體中維護的已載入模組清單中查閱。 如果跳躍目標的包含模組 (「目的模組」 ) 在其 GuardFlags 欄位中設定 IMAGE_GUARD_CF_LONGJUMP_TABLE_PRESENT 旗標，則 load configuration 目錄會有一個 GuardLongJumpTargetTable whith [load configuration GuardLongJumpTargetCount] 欄位所指定的元素計數。 此資料表的結構格式與 **GFIDS** 資料表相同，並使用相同的 GuardFlags IMAGE_GUARD_CF_FUNCTION_TABLE_SIZE_MASK 機制來編碼長跳躍資料表中選擇性的額外中繼資料位元組。 長跳躍表的所有中繼資料位元組都必須為零，而且是保留的。

  長跳躍資料表代表已排序的 Rva 陣列，這些是有效的長跳躍目標。 如果長跳躍目的模組在其 GuardFlags 欄位中設定 IMAGE_GUARD_CF_LONGJUMP_TABLE_PRESENT，則所有長的跳躍目標都必須在 LongJumpTargetTable 中列舉。 即使模組有零長的跳躍目標，如果工具組支援 CFG 的長期跳躍強化，它仍應設定 IMAGE_GUARD_CF_LONGJUMP_TABLE_PRESENT 旗標。 這表示映射沒有長跳躍目標，而且不是舊的映射，作業系統必須假設該映射在未標記的位置會有有效的長跳躍目標，無法執行長跳躍目標檢查。

  如果支援 CFG，建議您預設啟用長跳躍強化。 這是 Microsoft 編譯器的配置。 不了解長時間強化強化的作業系統 (預先 Windows 10 或較舊的 Windows 10 版本) 將不會執行長時間跳躍強化檢查，而且會忽略任何長時間跳躍強化的中繼資料，因此長期的快速強化可回溯相容于較舊的作業系統版本。

  若為核心模式映射，「臨界長跳躍」目標資料表不應該包含在 discardable 區段中。 「防護長跳躍」目標資料表應該一律儲存在唯讀的記憶體中，其安全性屬性才會生效。

## <a name="coff-information"></a>COFF 資訊

- 有目的檔標記可宣告物件檔案是否符合 CFG。 符合 CFG 的目的檔會列出它所產生的有效呼叫目標，以及取得 IAT 中繼資料的任何位址。 不符合 CFG 的目的檔必須藉由檢查 obj 檔案的 COFF 重新置放，以找出指向函式符號開頭的重新置放，來推斷呼叫目標。 這可能會 overapproximate 有效的 CFG 呼叫目標，因此在使用 CFG 進行編譯時，工具很希望工具標記其具有 CFG 感知的 obj 檔案，並包含 CFG obj 檔案中繼資料。

- 有個目的檔標記可宣告 CFG 強化的長跳躍目標，以進行 cfg 編譯模式。
