---
description: Pktextract.exe 是從憑證檔案中解壓縮 publicKeyToken 屬性的工具。
ms.assetid: 195ff5bd-bb60-4053-9308-ceacd29853c0
title: Pktextract.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd163efabd01d65969788aefc2386b2f49079729
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115185"
---
# <a name="pktextractexe"></a>Pktextract.exe

Pktextract.exe 是從憑證檔案中解壓縮 **publicKeyToken** 屬性的工具。 輸出是 **publicKeyToken**，也就是憑證中公開金鑰的唯一16個字元 (8 位元組) 識別碼，其格式可輕鬆地貼入元件身分識別語句中。 憑證檔案必須存在於 Pktextract.exe 的相同目錄中，才能使用公用程式。 Microsoft Windows 軟體開發套件 (SDK) 中提供 Pktextract.exe。

## <a name="syntax"></a>Syntax

**pktextract.exe** *<檔案名 .cer>* **\[ -quiet \] \[ -nologo \]**

## <a name="command-line-options"></a>命令列選項

Pktextract.exe 會使用下列不區分大小寫的命令列選項。



| 選項  | Description                                                          |
|---------|----------------------------------------------------------------------|
| -quiet  | 隱藏憑證資訊的完整顯示。 選擇性。        |
| -nologo | 在不顯示標準 Microsoft 著作權資料的情況下執行。 選擇性。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[並存元件開發工具](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 



