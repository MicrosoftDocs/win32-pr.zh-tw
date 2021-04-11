---
description: NTFS 會以 Unicode 儲存檔案名。 相反地，較舊的 FAT12、FAT16 和 FAT32 檔案系統會使用 OEM 字元集。 如需詳細資訊，請參閱字碼頁。
ms.assetid: 4573dd3b-ad68-460c-bc0f-ff65d4b70860
title: 檔案名中使用的字元集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79394c92b2886f715299855aae27f15753dc86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849988"
---
# <a name="character-sets-used-in-file-names"></a>檔案名中使用的字元集

NTFS 會以 Unicode 儲存檔案名。 相反地，較舊的 FAT12、FAT16 和 FAT32 檔案系統會使用 OEM 字元集。 如需詳細資訊，請參閱[字碼頁](code-pages.md)。

建立 FAT 檔案的非 Unicode 應用程式有時必須使用標準的 C 執行時間程式庫轉換函式，在 Windows 字碼頁字元集和 OEM 字碼頁字元集之間轉譯。 使用檔案系統函式的 Unicode 實作為，就不需要執行這類的翻譯。

您的應用程式可以使用泛型字串類型，如 [Windows 資料類型中的字串](windows-data-types-for-strings.md)所述。 應用程式也可以使用函式 [原型慣例](conventions-for-function-prototypes.md)中所述的技術來使用泛型函數原型。 針對泛型字串類型或泛型函式原型，您的應用程式可以使用單一原始程式檔來編譯 Unicode 或非 Unicode 版本。 為了允許這樣做，應用程式會針對在編譯 Unicode 時未叫用的函式提供宏。

在 NTFS 和 FAT 檔案系統中，特殊檔案名字元是： ' \\ '、'/'、'. '、'？ ' 和 ' \* '。 在 OEM 字碼頁上，這些特殊字元是在字元的 ASCII 範圍內 (0x00 到 0x7F) 。 其 Unicode 對等專案是2位元組形式的相同值，0x0000 至0x007F。

> [!Caution]  
> 在日文版作業系統上使用的 Windows 字碼頁和 OEM 字碼頁字元集，包含日元符號 (¥) ，而不是反斜線 (\\) 。 因此，日元符號是 NTFS 和 FAT 檔案系統禁止使用的字元。 當將 Unicode 對應至日文語言字碼頁時， [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) 和其他轉換函式會將反斜線 (U + 005C) 和一般 Unicode 日元符號 (u + 00A5) 轉換成這個相同的字元。 基於安全性理由，您的應用程式通常不應該在可能轉換的 Unicode 字串中允許字元 U + 00A5，以做為 FAT 的檔案名。 如需詳細資訊，請參閱 [安全性考慮：國際化功能](security-considerations--international-features.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows API 中的 Unicode](unicode-in-the-windows-api.md)
</dt> <dt>

[安全性考慮：國際功能](security-considerations--international-features.md)
</dt> </dl>

 

 



