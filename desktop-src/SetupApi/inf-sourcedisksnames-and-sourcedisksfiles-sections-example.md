---
description: INF 檔案的 SourceDisksNames 區段會識別包含要安裝之原始程式檔的磁片。
ms.assetid: af4bc466-f0a3-4f83-adb7-6bfc276f7764
title: INF SourceDisksNames 和 SourceDisksFiles 章節範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00eb8241b8e290f5460cc41b233d3b199df35e709d6e32f2c5a39925a79f851d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739408"
---
# <a name="inf-sourcedisksnames-and-sourcedisksfiles-sections-example"></a>INF SourceDisksNames 和 SourceDisksFiles 章節範例

INF 檔案的 **SourceDisksNames** 區段會識別包含要安裝之原始程式檔的磁片。 **SourceDisksFiles** 區段會識別來源檔案和包含它們的來源磁片。 請注意，Windows 2000 或 Windows XP 不支援 MIPS、Alpha 和 PPC 平臺。

從 Windows XP 開始， **SourceDisksNames** 區段可能會指定標記和封包檔。 例如，下列 **SourceDisksNames** 區段可以搭配可移動或固定媒體使用。 如果使用卸載式媒體，範例區段會先檢查標記是否存在，以確認媒體是否存在。 如果使用固定媒體，範例區段會先檢查是否有封包，以確認媒體是否存在。 確認封包存在之後，系統會嘗試將檔案從封包中複製出來，並提示您提供無法複製的檔案。

``` syntax
[SourceDisksNames]
1="Dajava" , "Dajava.cab",,, 0x10,"Dajava.tag"
```

如需有關 **SourceDisksNames** 或 **SourceDisksFiles** 的詳細資訊，請參閱 Microsoft Windows 2000 驅動程式開發工具組的「inf 檔案的一般指導方針」和「inf 檔案區段和指示詞」章節。

 

 



