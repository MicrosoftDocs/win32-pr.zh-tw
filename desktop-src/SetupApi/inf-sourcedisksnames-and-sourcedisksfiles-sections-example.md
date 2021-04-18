---
description: INF 檔案的 SourceDisksNames 區段會識別包含要安裝之原始程式檔的磁片。
ms.assetid: af4bc466-f0a3-4f83-adb7-6bfc276f7764
title: INF SourceDisksNames 和 SourceDisksFiles 章節範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f991727a8a2ca9cce2bd2d7161dfbf27b62ce74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978058"
---
# <a name="inf-sourcedisksnames-and-sourcedisksfiles-sections-example"></a>INF SourceDisksNames 和 SourceDisksFiles 章節範例

INF 檔案的 **SourceDisksNames** 區段會識別包含要安裝之原始程式檔的磁片。 **SourceDisksFiles** 區段會識別來源檔案和包含它們的來源磁片。 請注意，Windows 2000 或 Windows XP 不支援 MIPS、Alpha 和 PPC 平臺。

從 Windows XP 開始， **SourceDisksNames** 區段可能會指定標記和封包檔。 例如，下列 **SourceDisksNames** 區段可以搭配可移動或固定媒體使用。 如果使用卸載式媒體，範例區段會先檢查標記是否存在，以確認媒體是否存在。 如果使用固定媒體，範例區段會先檢查是否有封包，以確認媒體是否存在。 確認封包存在之後，系統會嘗試將檔案從封包中複製出來，並提示您提供無法複製的檔案。

``` syntax
[SourceDisksNames]
1="Dajava" , "Dajava.cab",,, 0x10,"Dajava.tag"
```

如需 **SourceDisksNames** 或 **SourceDisksFiles** 的詳細資訊，請參閱 Microsoft Windows 2000 驅動程式開發工具組的「Inf 檔案的一般指導方針」和「inf 檔案區段和指示詞」章節。

 

 



