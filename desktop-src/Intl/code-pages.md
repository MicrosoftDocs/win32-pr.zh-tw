---
description: 現今撰寫的大部分應用程式都是使用 UTF-16 編碼，以 Unicode 來處理字元資料。
ms.assetid: 866f09f4-629e-4097-a974-fbda9389d077
title: 字碼頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28528ba13e3db3f0c72dd7c071eb8b7886ab003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983670"
---
# <a name="code-pages"></a>字碼頁

現今撰寫的大部分應用程式都是使用 UTF-16 編碼，以 [Unicode](unicode.md)來處理字元資料。 不過，許多繼承應用程式會根據字碼頁繼續使用字元集。 即使是新的應用程式有時也需要使用字碼頁，但通常是下列其中一個原因：

-   與繼承應用程式進行通訊。
-   若要與較舊的郵件和新聞伺服器通訊，可能不一定會支援 Unicode。
-   與 Windows 主控台進行通訊。

> [!Note]  
> 新的 Windows 應用程式應該使用 [Unicode](unicode.md) 來避免不同的程式字碼頁不一致，並方便當地語系化。

 

每個字碼頁都會以字碼頁識別碼表示，例如1252，並由 Unicode 和字元集 API 函式處理。 如需支援的字碼頁識別碼清單，請參閱 [字碼頁識別碼](code-page-identifiers.md)。 Microsoft [Go 全球開發人員中心](https://msdn.microsoft.com/goglobal) 的「字碼頁」參考提供許多字碼頁的完整說明。

Windows 字碼頁（通常稱為「ANSI 字碼頁」）是不是 (值大於 127) 代表國際字元之非 ASCII 值的字碼頁。 這些字碼頁在 Windows Me 中是以原生方式使用，也可以在 Windows NT 和更新版本上取得。

> [!Note]  
> 最初，Windows 字碼頁1252（一般用於英文和其他西歐語言的字碼頁）是以美國國家標準局 (ANSI) draft 為基礎。 該草稿最終變成 ISO 8859-1，但是 Windows 字碼頁1252是在標準變成最終之前實，而且與 ISO 8859-1 不完全相同。

 

許多 Windows API 函數都有 "A" (ANSI) 和 "W" (寬 Unicode) 版本。 "A" 版本會根據 Windows 字碼頁處理文字，而 "W" 版本則會處理 Unicode 文字。 請參閱[Windows 資料類型，以取得](windows-data-types-for-strings.md)[函數原型的](conventions-for-function-prototypes.md)字串和慣例。

Windows 字碼頁有時也稱為「使用中的字碼頁」或「系統使用中的字碼頁」。 Windows 作業系統一律會有一個目前作用中的 Windows 字碼頁。 所有 [ANSI 版本的 API](conventions-for-function-prototypes.md) 函式都會使用目前作用中的字碼頁。

原始設備製造商 (OEM) 字碼頁為非 ASCII 值代表線條繪圖和標點符號字元的字碼頁。 這些字碼頁原本是用於 MS-DOS，仍用於主控台應用程式。 它們也可用於 FAT12、FAT16 和 FAT32 檔案系統中的非延伸檔案名，如 [檔案名中使用的字元集](character-sets-used-in-file-names.md)所述。 英文版的一般 OEM 字碼頁是字碼頁437。

針對 Windows 字碼頁和 OEM 字碼頁，0x00 至0x7F 的代碼值會對應至7位 ASCII 字元集。 透過0x19 和0x7F 的代碼值0x00 一律代表標準化的控制字元，而0x20 到0x7E 則代表標準化的可顯示字元。 其餘程式碼所代表的字元（0x80 到0xff）會因字元集而異。 每個字元集都包含不同的特殊字元，通常會針對語言或語言群組進行自訂。 Windows 字碼頁1252和 OEM 字碼頁437通常用於美國。

除了 Windows 和 OEM 字碼頁之外，您的應用程式也可以使用非原生字碼頁。 範例包括 EBCDIC 和 Macintosh 字碼頁。

Unicode (UTF-8 和 UTF-8) 的兩種編碼會實作為字碼頁。 如同其他字碼頁，每個頁面都是由數值識別碼所知道，而且可以使用許多相同的 Unicode 和字元集 API 函式來處理。

字碼頁可以是 [單一位元組字元集](single-byte-character-sets.md) (SBCS) 頁或 [雙位元組字集](double-byte-character-sets.md) (DBCS) 頁面。 在 SBCS 頁面中，每個位元組都會直接將單一字元編碼，如此一來，就可以精確呈現256的相異字元 (包括控制字元、字母、數位、標點符號、符號和 like) 。 DBCS 字碼頁用於日文和中文等語言。 在這類字碼頁中，某些字元具有具有特定位元組值的兩位元組編碼 (永遠值大於 127) 做為「前置位元組」。 前導位元組只能與 "軌跡 byte" 一起對應到一個字元，而不是在自己的許可權中編碼字元。

有些舊版通訊協定需要使用 SBCS 和 DBCS 字碼頁。 每個 SBCS/DBCS 字碼頁支援不同的字元，但沒有任何字碼頁支援 Unicode 提供的完整字元範圍。 每個 SBCS/DBCS 字碼頁支援不同的子集，以不同方式編碼。

> [!Note]  
> 從一個 SBCS 或 DBCS 字碼頁轉換成另一個資料頁的資料可能會損毀，因為不同字碼頁上的相同資料值可以編碼不同的字元。 從 Unicode 轉換成 SBCS 或 DBCS 的資料會受到資料遺失的影響，因為指定的字碼頁可能無法表示該特定 Unicode 資料中使用的每個字元。

 

除了 SBCS 和 DBCS 字碼頁，您的應用程式還可以使用多位元組字元集字碼頁52936、54936、51949和5022x，其使用的方法類似于 DBCS。 但是，多位元組字元集字碼頁超過了兩位元組編碼的部分字元。 UTF-7 和 UTF-8 使用類似的方法，分別以7位和8位位元組為基礎來編碼 Unicode。 如需詳細資訊，請參閱 [Unicode](unicode.md)。

數個 Unicode 和字元集函數可讓您的應用程式處理字碼頁。 應用程式可以使用 [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) 和 [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) 函數來取得字碼頁的相關資訊。 這項資訊包括在轉換的字串中的字元沒有對應的字碼頁專案時，所使用的預設字元。

應用程式可以使用 [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) 和 [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) 函式，根據 Windows 字碼頁和 Unicode 字串在字串之間進行轉換。 雖然它們的名稱是指「多位元組」，但這些函式同樣適用于 SBCS、DBCS 和多位元組字元集字碼頁。

> [!Note]  
> 如果提供的字碼頁無法代表 Unicode 字串中的所有字元， [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)可能會遺失部分資料。

 

您的應用程式可以使用標準 C 執行時間程式庫函式，在 Windows 字碼頁和 OEM 字碼頁之間進行轉換。 不過，使用這些函式會造成資料遺失的風險，因為每個字碼頁可以表示的字元不完全相符。

您的應用程式也可以呼叫 [**GetACP**](/windows/desktop/api/Winnls/nf-winnls-getacp) 函數。 此函式會抓取目前 Windows (ANSI) 字碼頁的識別碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[字元集](character-sets.md)
</dt> </dl>

 

 



