---
description: 將符號檔載入至符號處理常式之後，應用程式可以使用符號定位器函式來傳回指定位址的符號資訊。
ms.assetid: bfc068e1-eced-4ab2-80a3-acc2ed07c841
title: 尋找符號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a90aae9d2894ca8abc7470b2068b508655a50bcb76e1a122f2307f81273abec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912697"
---
# <a name="finding-symbols"></a>尋找符號

將符號檔載入至符號處理常式之後，應用程式可以使用符號定位器函式來傳回指定位址的符號資訊。 這些函數也可以找到位址的原始程式碼檔案名和行號位置。

## <a name="enumerating-symbol-files"></a>列舉符號檔

若要取得由模組名稱載入的所有符號檔清單，請呼叫 [**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) 函式。 如需範例，請參閱 [列舉符號模組](enumerating-symbol-modules.md)。 若要取得指定模組的符號清單，請呼叫 [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) 函數。 如需範例，請參閱 [列舉符號](enumerating-symbols.md)。

## <a name="retrieving-symbols-by-address"></a>依位址抓取符號

若要取得特定位址的符號資訊，請使用 [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) 函數。 此函式會抓取資訊，並將其儲存在 [**符號 \_ 資訊**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) 結構中。 由於符號名稱的長度是變數，因此您必須在 **符號 \_ 資訊** 結構宣告之後提供其他緩衝區空間。 如需範例，請參閱 [依位址抓取符號資訊](retrieving-symbol-information-by-address.md)。

請注意，位址不需要位於符號界限上。 如果位址出現在符號開頭之後，但符號的開頭 (符號的開頭加上符號大小) ，則函式會尋找符號。

## <a name="retrieving-symbols-by-symbol-name"></a>依符號名稱抓取符號

若要在符號資訊結構中取出特定模組和符號名稱的符號資訊，請使用 [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname)函數。 [**\_**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) 如果已設定延遲的符號載入， **SymFromName** 會嘗試載入尚未載入之模組的符號檔。 若要指定模組名稱以及符號名稱，請使用語法 *模組*！*SymName*。 "！" 字元會從符號名稱分隔模組名稱。 如需範例，請參閱 [依名稱抓取符號資訊](retrieving-symbol-information-by-name.md)。

## <a name="retrieving-line-numbers-by-address"></a>依位址取出行號

若要取得特定位址的原始程式碼位置，請使用 [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) 函數。 此函式會填入 [**Imagehlp.dll \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) 結構，其中包含指定位址所參考的原始程式檔名稱和行號位置。 如需範例，請參閱 [依位址抓取符號資訊](retrieving-symbol-information-by-address.md)。

## <a name="retrieving-line-numbers-by-symbol-name"></a>依符號名稱來取出行號

若要取得特定符號名稱的原始程式碼位置，請使用 [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) 函數。 此函式類似于 [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)，但會抓取 [**imagehlp.dll \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) 結構。 若要使用 [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)或 **SymGetLineFromName64**，您必須使用 SymSetOptions 函式，將載入行選項 (SYMOPT \_ 載入 \_ 行) 。 [](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) 如需範例，請參閱 [依名稱抓取符號資訊](retrieving-symbol-information-by-name.md)。

 

 



