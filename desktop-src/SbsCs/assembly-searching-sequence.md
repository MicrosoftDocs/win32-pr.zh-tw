---
description: 如果隔離的應用程式指定元件相依性，並存會先在 WinSxS 資料夾的共用元件之間搜尋元件。
ms.assetid: 93496631-55cc-4dd9-9a51-b748c35fd477
title: 元件搜尋順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 983466954d6cb9619d3fb0595c96f81fed7c9b73a29bfbf2f609b3f14203a957
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127538"
---
# <a name="assembly-searching-sequence"></a>元件搜尋順序

如果隔離的應用程式指定元件相依性，並存會先在 WinSxS 資料夾的 [共用元件](/windows/desktop/Msi/shared-assemblies) 之間搜尋元件。 如果找不到必要的元件，請並存，然後搜尋安裝在應用程式目錄結構之資料夾中的私用元件。

[私用元件](/windows/desktop/Msi/private-assemblies) 可以部署在應用程式目錄結構中的下列位置：

-   在應用程式的資料夾中。 通常，這是包含應用程式可執行檔的資料夾。
-   在應用程式資料夾的子資料夾中。 子資料夾的名稱必須與元件相同。
-   在應用程式資料夾的特定語言子資料夾中。 子資料夾的名稱是用來表示語言文化特性或語言之 DHTML 語言代碼的字串。
-   在應用程式資料夾中語言特定子資料夾的子資料夾中。 較高的子資料夾名稱是以 DHTML 語言代碼表示語言文化特性或語言的字串。 較深層的子資料夾與元件具有相同的名稱。

第一次並存搜尋私用元件，它會判斷特定語言的子資料夾是否存在於應用程式的目錄結構中。 如果不存在任何特定語言的子資料夾，請使用下列順序並存搜尋下列位置中的私用元件。

1.  並存搜尋 WinSxS 資料夾。
2.  \\\\< > \\ appdir <*assemblyname* # C0.DLL
3.  \\\\< > \\ appdir <*assemblyname*>. 資訊清單
4.  \\\\< > \\ appdir < > \\ assemblyname <*assemblyname* # C0.DLL
5.  \\\\< > \\ appdir < > \\ assemblyname <*assemblyname*>. 資訊清單

如果特定語言的子資料夾存在，則應用程式的目錄結構可能會包含以多種語言當地語系化的私用元件。 並存搜尋特定語言的子資料夾，以確保應用程式使用指定的語言或最佳的可用語言。 特定語言的子資料夾會使用指定語言文化特性或語言的 DHTML 語言代碼字串來命名。 如果特定語言的子資料夾存在，則會使用下列順序，並存搜尋下列位置中的私用元件。

1.  並存搜尋 WinSxS 資料夾。
2.  \\\\< > \\ appdir <*語言* > \\ 文化 < 特性 *assemblyname* # C0.DLL
3.  \\\\< > \\ appdir <*語言* > \\ 文化 < 特性 *assemblyname*>. 資訊清單
4.  \\\\< > \\ appdir <*語言* > \\ 文化 < 特性 > \\ assemblyname <*assemblyname* # C0.DLL
5.  \\\\< > \\ appdir <*語言* > \\ 文化 < 特性 > \\ assemblyname <*assemblyname*>. 資訊清單

請注意，並存搜尋順序會尋找具有元件名稱的 DLL 檔，並在搜尋具有元件名稱的資訊清單檔之前停止。 處理 DLL 私用元件的建議方式是將元件資訊清單放在 DLL 檔案中做為資源。 資源識別碼必須等於1，而且私用元件的名稱可能與 DLL 的名稱相同。 例如，如果 DLL 的名稱是 MICROSOFT.WINDOWS.MYSAMPLE.DLL，則在元件資訊清單的 **assemblyIdentity** 元素中使用的 name 屬性值也可能是 Microsoft。Windows. mysample。 或者，您可以將組件資訊清單放在不同的檔案中，但是元件的名稱及其資訊清單必須和 DLL 的名稱不同。 例如，Microsoft。Windows mysampleAsm，Microsoft。Windows mysampleAsm 資訊清單，並 MICROSOFT.WINDOWS.MYSAMPLE.DLL。

例如，如果 myapp 安裝在磁片磁碟機 c：的根目錄，且需要法文-比利時的 myasm，則並存會使用下列順序來搜尋當地語系化的 myasm 實例的最近似。

1.  並列搜尋是否為 fr-fr 版本的並列搜尋。
2.  c： \\ myapp \\ fr \\myasm.dll
3.  c： \\ myapp \\ fr- \\ myasm。資訊清單
4.  c： \\ myapp \\ fr \\ myasm \\myasm.dll
5.  c： \\ myapp \\ fr- \\ myasm \\ myasm。資訊清單
6.  針對 fr 版本的並列搜尋。
7.  c： \\ myapp \\ fr \\myasm.dll
8.  c： \\ myapp \\ fr \\ myasm 資訊清單
9.  c： \\ myapp \\ fr \\ myasm \\myasm.dll
10. c： \\ myapp \\ fr \\ myasm \\ myasm。資訊清單
11. 針對 en-us 版本的並列搜尋。
12. c： \\ myapp \\ en-us \\myasm.dll
13. c： \\ myapp \\ en-us \\ myasm 資訊清單
14. c： \\ myapp \\ en-us \\ myasm \\myasm.dll
15. c： \\ myapp \\ en-us \\ myasm \\ myasm. 資訊清單
16. 並列搜尋是否為 en 版。
17. c： \\ myapp \\ en \\myasm.dll
18. c： \\ myapp \\ en \\ myasm 資訊清單
19. c： \\ myapp \\ en \\ myasm \\myasm.dll
20. c： \\ myapp \\ en \\ myasm \\ myasm. 資訊清單
21. 並列搜尋不是語言版本。
22. c： \\ myapp \\myasm.dll
23. c： \\ myapp \\ myasm 資訊清單
24. c： \\ myapp \\ myasm \\myasm.dll
25. c： \\ myapp \\ myasm \\ myasm。資訊清單

如果並存搜尋到達元件的語言中性版本，而且系統上有 [多語系消費者介面 (MUI)](/windows/desktop/Intl/multilingual-user-interface)版本的 Windows，則會並存嘗試系結至 <*assemblyname*> 的 mui。 如果搜尋到達元件的當地語系化版本，並存就不會嘗試系結至 <*assemblyname*>. mui。 非語言相關元件的 [組件資訊清單](assembly-manifests.md) 不會在其 **assemblyIdentity** 元素中具有 language 屬性。 如果並存到達非語言相關元件，並安裝了 MUI，則會使用下列 <*assemblyname*> 的順序來搜尋下列位置： mui。 如果元件是文化特性中立的，則並存會使用相同的搜尋順序，但 <不會搜尋 *任何語言*>。

1.  並存搜尋 WinSxS 資料夾中的 <*assemblyname*> mui。
2.  \\\\<*使用者的語言-文化特性* > \\ <*assemblyname*> mui
3.  \\\\<*使用者的語言* > \\ <*assemblyname*> mui
4.  \\\\<*系統的語言-文化特性* > \\ <*assemblyname*> mui
5.  \\\\<*系統的語言* > \\ <*assemblyname*> mui
6.  \\\\<*沒有* > \\ 語言 <*assemblyname*> mui

例如，如果並存搜尋在 c： myapp myasm myasm 找到私用元件 \\ \\ \\ ，而 myasm 是語言中立的元件，則為。 並列接著會使用下列順序來搜尋 myasm。 請注意，並存不會搜尋非語言相關的 MUI 元件。

1.  並列的搜尋會被 WinSxS 的 MUI 元件的 fr 版本。
2.  c： \\ myapp \\ fr \\myasm.mui.dll
3.  c： \\ myapp \\ fr- \\ myasm
4.  c： \\ myapp \\ fr \\ myasm \\myasm.mui.dll
5.  c： \\ myapp \\ fr- \\ myasm \\ myasm。資訊清單
6.  並列的 MUI 元件的搜尋會被 WinSxS。
7.  c： \\ myapp \\ fr \\myasm.mui.dll
8.  c： \\ myapp \\ fr \\ myasm。資訊清單
9.  c： \\ myapp \\ fr \\ myasm \\myasm.mui.dll
10. c： \\ myapp \\ fr \\ myasm \\ myasm。資訊清單
11. 並列的搜尋會被 WinSxS 的 MUI 元件的 en-us 版本。
12. c： \\ myapp \\ en-us \\myasm.mui.dll
13. c： \\ myapp \\ en-us \\ myasm
14. c： \\ myapp \\ en-us \\ myasm \\myasm.mui.dll
15. c： \\ myapp \\ en-us \\ myasm \\ myasm
16. 並列搜尋是以該版本的 MUI 元件為 en。
17. c： \\ myapp \\ en \\myasm.mui.dll
18. c： \\ myapp \\ en \\ myasm
19. c： \\ myapp \\ en \\ myasm \\myasm.mui.dll
20. c： \\ myapp \\ en \\ myasm \\ myasm

 

 
