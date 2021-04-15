---
title: MIDLRT.EXE 根據和 Windows 執行階段元件
description: 顯示如何建立中繼資料 ( winmd) 檔案，這些檔案代表自訂 Windows 執行階段元件的 API。
ms.assetid: 7830A5DB-9696-4A93-948B-51DA46A5143C
keywords:
- MIDL 編譯器 MIDL
- MIDL 編譯器 MIDL、MIDL 和 Windows 執行階段 winrt
- Windows 執行階段 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edf4d40b3fc5b0a5ed8eeb9b5fd47a3b87c4543
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104508200"
---
# <a name="midlrt-and-windows-runtime-components"></a>MIDLRT.EXE 根據和 Windows 執行階段元件

顯示如何建立中繼資料 ( winmd) 檔案，這些檔案代表自訂 Windows 執行階段元件的 API。


使用 MIDLRT.EXE 根據編譯器，針對您的自訂 Windows 執行階段元件 ( winmd) 檔案建立中繼資料。

產生中繼資料檔案時，您可以使用 MDMERGE 公用程式，將它們組成更有效率的封裝。 如需詳細資訊，請參閱 [MDMERGE 和中繼資料](mdmerge-and-metadata-files.md)檔案。


使用 MIDLRT.EXE 根據類似于使用 MIDL 編譯器。 使用下列命令，從命令列執行 MIDLRT.EXE 根據：

**midlrt.exe 根據**  *<***選項** _>_**檔案名 .idl**

其中 * < ***選項** _>_ 表示您想要使用的命令列選項，而 Filename 則是要編譯之 idl 檔案的名稱。


下列清單顯示 MIDLRT.EXE 使用的命令列參數。

<dl>

[**/enum \_ 類別**](-enum-class.md)  
[**/metadata \_ 目錄**](-metadata-dir.md)  
[**/nomidl**](-nomidl.md)  
[**/nomd**](-nomd.md)  
[**/ns \_ 前置詞**](-ns-prefix.md)  
[**/winmd**](-winmd.md)  
[**/winrt**](-winrt.md)  
</dl>

當您使用 MIDLRT.EXE 根據編譯器 [**/help**](-help-.md) 和/？時，可使用 midlrt.exe 根據編譯器參數和選項的完整清單。 開關。 這些參數是依類別目錄組織。 如需詳細資訊，請參閱 [MIDL Command-Line 參考](midl-command-line-reference.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MDMERGE 和中繼資料檔案](mdmerge-and-metadata-files.md)
</dt> </dl>

 

 




