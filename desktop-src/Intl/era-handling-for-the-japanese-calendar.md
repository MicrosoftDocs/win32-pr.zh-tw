---
description: 日本曆的紀元處理方式
ms.assetid: a1dabf7c-6521-492e-bdc0-27cfb07cfc20
title: 日本曆的紀元處理方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eba757745bf0d90d119c821772c7fc23f3f8694b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851811"
---
# <a name="era-handling-for-the-japanese-calendar"></a>日本曆的紀元處理方式

許多行事曆都有紀元，例如 AD/BC 或 CE/BCE。 在日文日曆中，年份會以 nengō（年份數目和紀元名稱的組合）來描述。 例如，2009是 Heisei 21。 在過去，日文紀元名稱經常變更，但現在日文的紀元只會在每個英制上變更。 在過去，Windows 和 Microsoft .NET 在此原則下支援四個新式的紀元： Meiji、Taishō、Shōwa 和 Heisei。

有了 Windows 7、Windows Server 2008 R2 和 .NET Framework 4，Microsoft 就能辨識未來可能會加入額外的紀元。 在這些版本的 Windows 上，紀中繼資料會儲存在登錄中的機碼底下：<dl> HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ Nls 行事 \\ 曆 \\ 日文 \\ 紀元  
</dl>

如有必要，您可以透過一般的 Windows Update 程式，將額外的紀元新增至該索引鍵。 您可以使用登錄編輯程式 (Regedit.exe) 來查看此機碼。 Windows 7 隨附的金鑰和值的範例如下：

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"1868 01 01"="明治_明_Meiji_M"
"1912 07 30"="大正_大_Taisho_T"
"1926 12 25"="昭和_昭_Showa_S"
"1989 01 08"="平成_平_Heisei_H"
```

每個紀元值的名稱都是紀元開始于西曆的日期。 值包含日文的紀元名稱、日文的縮寫名稱、英文的名稱，以及英文的縮寫名稱：<dl> "YYYY MM DD" = "JE \_ AJE \_ EE \_ AEE"  
</dl>where

-   "YYYY MM DD" 是年、月、日、年是4位數、日是2位數，且月份也是2位數的紀元開始日期。 以空格分隔日期的每個部分。
-   「JE」是紀元的日文名稱，後面接著底線。
-   "AJE" 是紀元的縮寫名稱，以日文為開頭，後面接著底線。
-   "EE" 是日文紀元的英文名稱，後面接著底線。
-   "AEE" 是日文紀元的縮寫英文名稱。

應用程式開發人員的其中一個考慮是，Windows Update 或其他方式將額外的紀元新增至其他紀元的可能性。 在這種情況下，應用程式可能會遇到日文行事曆預期的四個紀元。 針對測試用途，測試人員可能會在登錄中加入額外的紀元;不過，這應該限制為僅測試電腦，因為它會影響整部電腦的行為。

以下是可用於測試的這類金鑰範例。 您可以使用登錄編輯程式來進行這種變更。  (此範例僅供測試使用，且不適合用來預測未來的任何新增專案。 ) 

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"2020 09 01"="仮名_仮_Test Era_X"
```

請注意，這只會影響執行 Windows 7 和更新版本或 .NET Framework 4 和更新版本的機器。 應用程式開發人員可以使用這類額外的測試紀元來測試其應用程式，以確保其應用程式在未來的時間加入額外的紀元時仍能繼續運作。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[正在抓取時間和日期資訊](retrieving-time-and-date-information.md)
</dt> <dt>

[行事曆識別碼](calendar-identifiers.md)
</dt> </dl>

 

 



