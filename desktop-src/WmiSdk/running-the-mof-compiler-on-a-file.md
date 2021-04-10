---
description: 在編譯 MOF 檔案時，您有兩個選擇：使用命令列公用程式或使用程式設計介面。
ms.assetid: 1760f1bd-7027-4201-97a2-ca902f945b52
ms.tgt_platform: multiple
title: 在檔案上執行 MOF 編譯器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad1605544e05f59670f9e6fd73fcd8c01862b46c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192080"
---
# <a name="running-the-mof-compiler-on-a-file"></a>在檔案上執行 MOF 編譯器

在編譯 MOF 檔案時，您有兩個選擇：使用命令列公用程式或使用程式設計介面。

在您執行 MOF 編譯器之前 [**Mofcomp.exe**](mofcomp.md)，未向 wmi 註冊提供者，且在 MOF 檔案中建立的類別在 [*wmi 存放庫*](gloss-w.md)中無法使用。 下列程式說明如何編譯 MOF 檔案。

**從命令列執行 MOF 編譯器 on file**

1.  使用下列語法，從命令列呼叫 MOF 編譯器。

    **Mofcomp.exe** *MOFfile * * *. mof**

    MOF 編譯器支援各種不同的參數來控制特殊的處理情況。 所有參數都是選擇性的，且允許任何參數組合。 不過，將某些參數與其他參數搭配使用並不合理。 例如，若要結合 **-class： updateonly** 和 **-class：以** 參數會導致編譯器無法執行任何動作。

    根據預設，Mofcomp.exe 會將編譯的類別儲存在根 \\ 預設 WMI 命名空間中。 請注意，Mofcomp.exe 的預設命名空間與腳本的預設命名空間不同。 腳本的預設命名空間是在 [Advanced （Advanced）] 索引標籤的 WMI 控制項中指定的。如需詳細資訊，請參閱 [使用 WMI 控制項設定命名空間安全性](setting-namespace-security-with-the-wmi-control.md)。

    您可以透過兩種方式來變更接收類別的命名空間。

    1.  針對 **mofcomp.exe** 命令使用 **-N** 參數。
    2.  在 MOF 檔案中插入預處理器命令 \# [**pragma 命名空間**](pragma-namespace.md)。

2.  （選擇性）您可以用程式設計的方式編譯 MOF 檔案。 如需詳細資訊，請參閱 [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[編譯 MOF 檔案](compiling-mof-files.md)
</dt> <dt>

[**mofcomp.exe**](mofcomp.md)
</dt> <dt>

[預處理器命令](preprocessor-commands.md)
</dt> </dl>

 

 



