---
description: 搭配使用 .NET Framework 4 與舊版的應用程式
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: 搭配使用 .NET Framework 4 與舊版的應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30eb8f4be1c50904b8d5760f456f3fe20bdd3da
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314941"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a>搭配使用 .NET Framework 4 與舊版的應用程式

## <a name="platform"></a>平台

 **客戶** 端-windows XP、windows Vista、windows 7  
**伺服器** -windows server 2003、windows server 2008、windows Server 2008 R2  


## <a name="feature-impact"></a>功能影響

 **嚴重性** -低  
**頻率** -高  






## <a name="description"></a>描述

.NET Framework 4 與使用先前的 .NET Framework 版本所建立的應用程式具有高度相容性。 .NET Framework 4 的主要變更是改善安全性、標準合規性、正確性、可靠性和效能。

不過，.NET Framework 4 不會自動使用它的 common language runtime 版本 (CLR) 來執行使用舊版 .NET Framework 所建立的應用程式。

## <a name="manifestation"></a>表現

如果您使用較早的 .NET Framework 建立應用程式，而且使用者在已安裝 .NET Framework 4 和舊版 .NET Framework 的電腦上開啟該應用程式，則應用程式會使用較早的 CLR 版本。

但是，如果 .NET Framework 4 是安裝在電腦上的唯一執行階段版本，則應用程式會擲回例外狀況，並要求使用者安裝您為應用程式建立的執行階段版本。

## <a name="solution"></a>解決方法

若要執行使用 .NET Framework 4 .NET Framework 版本所建立的應用程式，您必須將應用程式編譯為以 .NET Framework 4 版本為目標，方法是在 Microsoft Visual Studio 的專案屬性中指定該應用程式，或者您可以在應用程式佈建檔的 [**<supportedRuntime> 元素**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))中指定 .NET Framework 4。

如需如何遷移至 .NET Framework 4 的詳細資訊，請參閱 .NET Framework 中 .NET Framework 4 和[版本相容性](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))的[遷移指南](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))。

## <a name="compatibility-tests"></a>相容性測試

進行變更之後，請測試您的應用程式，以確定它會正確執行。 您可以如 [.NET Framework 4 應用程式相容性](/previous-versions/dd889541(v=msdn.10)) 主題所述，測試相容性。

如果您的應用程式或元件在安裝 .NET Framework 4 之後無法運作，請透過 [Microsoft Connect](https://connect.microsoft.com/visualstudio) 網站提交 bug。

## <a name="links-to-other-resources"></a>其他資源的連結

-   [**<supportedRuntime> 元素**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))
-   [.NET Framework 4 移轉手冊](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))
-   [.NET Framework 的版本相容性](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))
-   **.NET Framework 4 RTM 應用程式相容性逐步解說：**<https://msdn.microsoft.com/library/dd889541.aspx>
-   [Microsoft Connect](https://connect.microsoft.com/)

 

 
