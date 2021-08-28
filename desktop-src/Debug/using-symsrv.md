---
description: 使用 SymSrv
ms.assetid: d400f222-c50c-4c7b-8f8a-0c3ed3bba3b9
title: 使用 SymSrv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f0abcbd76b710e6a9429baa1ceff6d3a53a0df
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886497"
---
# <a name="using-symsrv"></a>使用 SymSrv

SymSrv 會從集中式符號存放區傳遞符號檔。 這些存放區可包含任意數目的符號檔案，對應至任意數目的程式或作業系統。 存放區也可以包含二進位檔案，這在對小型傾印檔案進行調試時特別有用。

存放區可以包含實際的符號和二進位檔案，或只包含符號檔的指標。 如果存放區包含指標，SymSrv 會直接從其來源取得實際的檔案。

SymSrv 也可以將大型符號存放區分成較小的子集，以供特殊的偵錯工具使用。

最後，SymSrv 可以使用作業系統所提供的登入資訊，從 HTTP 或 HTTPS 來源取得符號檔。 SymSrv 支援以智慧卡、憑證和一般登入和密碼保護的 HTTPS 網站。

## <a name="setting-the-symbol-path"></a>設定符號路徑

如 [符號](symbol-paths.md)路徑中所述，符號路徑 (\_ NT \_ 符號 \_ 路徑環境變數) 可由數個以分號分隔的路徑元素組成。 如果其中一或多個路徑元素的開頭是 "srv" 文字 \* ，則元素是符號伺服器，並會使用 SymSrv 來尋找符號檔。

> [!Note]  
> 如果 \* 未指定 "srv" 文字，但實際的 path 元素是符號伺服器存放區，則符號處理常式將會如同指定了 "srv \* " 一樣。 符號處理常式會搜尋指定路徑的根目錄中名為 "pingme.txt" 的檔案是否存在，以進行這項判斷。

 

如同符號路徑是由以分號分隔的符號路徑元素組成，符號伺服器是由以星號分隔的符號存放區元素所組成。 "Srv" 前置詞之後最多可以有10個符號存放區 \* 。 列在清單左邊的商店稱為 *下游* 存放區，右邊的商店稱為 *上游* 存放區。

<dl> srv \* *SymbolStore*  
srv \* *SymbolStore1* \* *SymbolStoreN*  
</dl>

如果路徑中只包含一個符號存放區元素，則 SymSrv 將會嘗試直接從該存放區使用任何要求的檔案。

如果路徑中有兩個符號存放區，SymSrv 會在最左邊的符號存放區中尋找符號檔。 如果檔案存在，就會使用它。 如果不存在，SymSrv 就會在右邊的符號存放區中尋找。 如果檔案存在，則會將它複製到左側存放區，並從該處開啟。

如果有兩個以上的商店，此行為會繼續向右，直到找到檔案或清單中沒有其他存放區為止。

永遠不會從任何存放區開啟檔案，而是從最左邊的存放區開啟。 如果在鏈中的其他位置找到該檔案，它就會複製到它左邊的每個存放區。 這項複製程式稱為「串聯」，並提供將在本檔稍後 clarfied 的一些優點。

## <a name="types-of-symbol-stores"></a>符號存放區的類型

下表顯示支援的符號存放區類型範例。

|  符號存放區類型       |  說明 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \\\\伺服器 \\ 共用          | 遠端伺服器上共用的完整 UNC 路徑。                                                                                                                                                                                                                                                                                                 |
| c： \\ LocalCache             | 用戶端電腦上目錄的路徑。                                                                                                                                                                                                                                                                                                             |
| https://InternetSite        | 裝載符號之網站的 URL。 必須是清單中最右邊的存放區，而且不可以是清單中的唯一存放區。                                                                                                                                                                                                                          |
| https://SecureInternetSite | 裝載符號之安全網站的 URL。 這可支援密碼、Windows 登入認證、憑證和智慧卡。 必須是清單中最右邊的存放區，而且不可以是清單中的唯一存放區。                                                                                                                              |
| 空白&lt;&gt;              | 如果兩個星號之間沒有文字，這表示預設的 *下游存放區*。 您可以藉由呼叫 [**SymSetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory)來設定位置。 預設值是名為 "sym" 的目錄，緊接在呼叫應用程式的程式目錄正下方。 這有時稱為 *預設本機* 快取。 |



 

因為無法寫入 HTTP 型的符號存放區，所以它必須是清單中最右邊的存放區。 如果以 HTTP 為基礎的符號存放區位於商店清單的中間或左邊，則無法將任何找到的檔案複製到其中，且鏈會中斷。 此外，由於符號處理常式無法從網站開啟檔案，因此以 HTTP 為基礎的存放區不能是最左邊的或只有清單中的存放區。 如果使用此符號路徑來呈現 SymSrv，它將會嘗試將檔案複製到預設下游存放區，並從該處開啟它，而不考慮預設下游存放區是否在符號路徑中指出。

## <a name="examples"></a>範例

若要在 mybuilds mysymbols 上使用 SymSrv 搭配符號存放區 \\ \\ \\ ，請設定下列符號路徑：

**設定 \_ NT \_ 符號 \_ 路徑 = srv \* \\ \\ mybuilds \\ mysymbols**

若要設定符號路徑，讓偵錯工具將符號檔從 mybuilds mysymbols 上的符號存放區複製 \\ \\ \\ 到本機目錄 c： \\ localsymbols，請使用：

**設定 \_ NT \_ 符號 \_ 路徑 = srv \* c： \\ localsymbols \* \\ \\ mybuilds \\ mysymbols**

若要設定符號路徑，讓偵錯工具將符號檔從 mybuilds mysymbols 上的符號存放區複製 \\ \\ \\ 到預設下游存放區 (通常是 c： \\ 偵錯工具 \\ sym) ，請使用：

**設定 \_ NT \_ 符號 \_ 路徑 = srv \* \* \\ \\ mybuilds \\ mysymbols**

若要使用串聯存放區，請設定下列符號路徑：

**設定 \_ NT \_ 符號 \_ 路徑 = srv \* c： \\ localsymbols \* \\ \\ NearbyServer \\ store\*https://DistantServer**

在此範例中，SymSrv 會先在 c： localsymbols 中尋找檔案 \\ 。 如果找到，它會傳回檔案的路徑。 否則，SymSrv 會在 \\ \\ NearbyServer 存放區中尋找檔案 \\ 。 如果找到該檔案，SymSrv 會將檔案複製到 c： \\ localsymbols，並傳回該檔案的路徑; 如果找不到檔案，SymSrv 會在中尋找檔案， https://DistantServer 如果找到的話，SymSrv 會將檔案複製到 \\ \\ NearbyServer \\ 存放區，然後再複製到 c： \\ localsymbols。

最後一個範例顯示如何使用符號路徑的合理設計，將符號的下載優化。 如果您有一個具有偵錯工具群組的工作網站，而且它們都需要從遙遠的位置取得符號，您可以在所有偵錯工具附近設定具有符號存放區的泛型服務器。 然後使用上述的符號路徑來設定每個偵錯工具。 第一個需要特定版本 foo .pdb 的偵錯工具會將它從下載 https://DistantServer 到 \\ \\ NearbyServer \\ 存放區，然後從它自己的電腦載入 c： \\ localsymbols。 需要相同檔案的下一個偵錯工具將能夠從 \\ \\ NearbyServer 存放區下載， \\ 因為先前的偵錯工具已經將它下載到該位置。 此多層快取可節省大量時間和網路頻寬。

## <a name="microsoft-symbol-store"></a>Microsoft 符號存放區

Microsoft 會提供網際網路符號伺服器的存取權，該伺服器包含許多版本的 Windows 作業系統的符號檔。 此符號目錄不保證已完成，但很廣泛。 其他 Microsoft 產品也會呈現。

網際網路符號伺服器已填入 Microsoft Windows 作業系統的各種 Windows 符號，包括熱修正、Service pack、安全性匯總套件和零售版。 您也可以在伺服器上取得 Windows 產品的目前搶鮮版和候選版的符號，以及各種不同的 microsoft 產品，例如 microsoft Internet Explorer。

如果您在進行偵錯工具時可以存取網際網路，您可以設定偵錯工具在偵錯工具期間視需要下載符號，而不是在偵錯工具會話之前個別下載符號檔。 符號會下載至您指定的目錄位置，然後偵錯工具會從該處載入這些符號。

Microsoft 符號存放區的 URL 為 https://msdl.microsoft.com/download/symbols 。 下列範例會示範如何設定偵錯工具符號路徑， (以您的下游存放區路徑取代 *c： \\ DownstreamStore*) ：

``` syntax
srv*c:\DownstreamStore*https://msdl.microsoft.com/download/symbols
```

## <a name="compressed-files"></a>壓縮檔案

SymSrv 與包含壓縮檔案的符號存放區相容，只要已使用 Windows Server 2003 資源套件所散發的 compress.exe 工具來執行壓縮即可。 壓縮檔案副檔名中的最後一個字元應該有底線 (例如， \_ module2 \_) 。 如需詳細資訊，請參閱 [使用 SymStore](using-symstore.md)。

當串聯時，除非目標存放區是路徑中最左邊的存放區，否則不會將檔案解壓縮。 如果路徑中只有一個存放區，且其中包含一個壓縮的檔案，則 SymSrv 會將該檔案複製到預設的下游存放區，並從該處開啟它，即使它們的符號路徑中並未指出預設的下游存放區也一樣。

**DbgHelp 6.1 及更早版本。：** 如果主要存放區中的檔案已壓縮，您必須使用下游存放區。 SymSrv 會先解壓縮所有檔案，再將它們複製到下游存放區。

## <a name="deleting-the-cache"></a>刪除快取

如果您使用下游存放區做為快取，您隨時都可以刪除這個目錄來儲存磁碟空間。

您可以有大量的符號存放區，其中包含許多不同程式或 Windows 版本的符號檔。 如果您升級目的電腦上所使用的 Windows 版本，則快取的符號檔全都會符合先前的版本。 這些快取的檔案不會進一步使用，因此這可能是刪除快取的好時機。

Windows 的偵錯工具隨附一個稱為 agestore.exe 的公用程式，它會選擇性地移除目錄樹狀結構中的檔案，並保留最近使用的檔案。 此工具的設計目的是要從符號伺服器存放區中剪除未使用的檔案。 它可讓您控制許多選項，包括「剪下日期」和「目錄大小」演算法。

## <a name="flat-cache-directory"></a>一般快取目錄

您可以將預設下游存放區宣告為一般目錄，而不是標準符號樹狀結構。 若要這樣做，請使用 SYMOPT 的 **一般 \_ \_ 目錄** 來呼叫 [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions)函式 (這也會在 SymSrv) 中設定 **SSRVOPT 一般 \_ \_ 預設 \_ 存放區** 選項。 在這麼做之前，請務必先呼叫 [**SymSetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory) ;否則，您可以將符號檔寫入至程式目錄。

## <a name="pointer-files"></a>指標檔

SymStore 可以建立及使用指向目標檔案的檔案，而不是目標檔案本身。 如果符號存放區包含這類指標檔案，則預設會將檔案從指標檔案中指出的位置複製到存放區。 若要設定存放區，以複製指標檔案，而不是它所指向的檔案，請在目標存放區的根目錄中建立名為 wantsptr.txt 的檔案。 wantsptr.txt 的內容並不重要，只有檔案存在。

## <a name="excluding-files-from-symbols-list"></a>從符號清單中排除檔案

若要從符號搜尋中排除檔案，您可以在 symsrv.ini 或登錄中指定其名稱。 若要在 symsrv.ini 中指定檔案，請建立名為排除的區段，並列出檔案。 檔案名可以包含萬用字元，如下列範例所示：

``` syntax
[Exclusions]
dbghelp.pdb
symsrv.*
mso*
```

Symsrv.ini 應該位於 symsrv.dll 所在的相同目錄中。 在大部分的安裝中，檔案不存在，您將需要建立一個新的檔案。

或者，您可以儲存要在登錄中排除的檔案。 建立下列登錄機碼： **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 符號伺服器 \\ 排除** 專案。 將每個檔案名儲存為字串值， (REG \_ SZ) 在此機碼中。 字串值的名稱指定要排除的檔案名。 您可以使用字串值的內容來儲存批註，以說明檔案的排除原因。

## <a name="installation"></a>安裝

SymSrv (symsrv.dll) 符號伺服器包含在 Windows 封裝的偵錯工具中。 它必須安裝在您要載入的 dbghelp.dll 複本所在的相同目錄中。 如需詳細資訊，請參閱 [呼叫 DbgHelp 程式庫](calling-the-dbghelp-library.md)。

 

 



