---
description: DbgHelp API 的符號處理功能已演變多年。
ms.assetid: 6dc41682-6104-418b-b045-7afe8c2b11e9
title: Public、Global 和 Local 符號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ecaa40549b091af204f2e318aefef8a256408e5f81b461e63a54c333719dd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406098"
---
# <a name="public-global-and-local-symbols"></a>Public、Global 和 Local 符號

DbgHelp API 的符號處理功能已演變多年。 為了確保您的程式碼可在各種案例中運作，並提供符號的完整詳細資料，請盡可能使用最新的函式。 例如， [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) 會取代 [**SymEnumerateSymbols64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)、 [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) 取代 [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)， [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) 會取代 [**SymGetSymFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)。

## <a name="public-symbols"></a>公用符號

DbgHelp.dll 的初始版本僅支援檢查公用符號。 您必須在不同的原始程式檔之間公開的程式碼中的任何專案，都會產生這些符號。 它們也包含從模組中匯出的所有專案。

這些符號可能內嵌于影像中，或個別儲存在 dbg 或 .pdb 檔案中。 唯一儲存的資訊是符號名稱和位址。 這些名稱會以裝飾名稱的形式提供。 若要查看未修飾的名稱，請使用 SYMOPT Undname.exe 呼叫 [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) 函式 \_ ，或使用 [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) 函數。

請注意，DbgHelp API 一開始不是設計來支援模組內相同符號的多個實例。 這是因為公用符號會限制為模組內的唯一名稱。 因此， [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname) 只會傳回符合的第一個符號。 若要取出所有符合的符號，請呼叫 [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols)。

## <a name="global-and-local-symbols"></a>全域和區域符號

較新版本的 DbgHelp.dll 在使用 .pdb 檔案時，支援 global 和 local 符號。 這些新版本包括靜態函式、範圍在原始檔中的函式、函式參數，以及本機變數。 當 DbgHelp 搜尋符號時，會先檢查全域和區域符號表，再檢查公用符號表。 這是因為這些類型的符號有更多可用的資訊，而不是公用符號的可用資訊。

全域和區域符號會以未修飾的名稱儲存。 因此，SYMOPT \_ undname.exe 旗標沒有任何作用。 若要取得裝飾符號名稱，您必須使用 \_ \_ 僅限 SYMOPT PUBLICS 旗標。 這會導致 DbgHelp 只搜尋公用符號。

若要查看本機符號或函式參數，請呼叫 [**SymSetCoNtext**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetcontext)函數，並將 [**imagehlp.dll \_ 堆疊 \_ 框架**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_stack_frame)結構的 **InstructionOffset** 成員設為任何函式符號的位址。 後續對 [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) 和 [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) 的呼叫，都可以在此位址的內容中運作。 若要這樣做，請將 *BaseOfDll* 參數設定為 **Null** ，並省略 *Name* 或 *Mask* 參數中的模組規範。 這會強制 DbgHelp 在 **SymSetCoNtext** 所指示的範圍內搜尋相符的符號。

若要判斷符號是否為參數，請檢查 [**符號 \_ 資訊**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info)結構的 **旗標** 成員。 如果符號是參數，則成員包含 SYMFLAG \_ 參數。 如果是本機符號，則成員會包含 SYMFLAG \_ local。

 

 



