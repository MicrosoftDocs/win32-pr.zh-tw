---
title: 登錄重新導向程式
description: 登錄重新導向程式會在 WOW64 上提供登錄某些部分的個別邏輯視圖，以隔離32位和64位應用程式。
ms.assetid: b3989f79-0439-485a-96c1-4f2227d48653
keywords:
- 64位 Windows 程式設計指南64位 Windows 程式設計，登錄重新導向程式
- 登錄重新導向程式 64-位 Windows 程式設計
- 重新導向64位 Windows 程式設計
- WOW64 64 位 Windows 程式設計，登錄重新導向程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac810a6ce2dba049f7b7e5b9d28386cda89712f2833eb7bf4f7892df59b34ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561504"
---
# <a name="registry-redirector"></a>登錄重新導向程式

登錄重新導向程式會在 WOW64 上提供登錄某些部分的個別邏輯視圖，以隔離32位和64位應用程式。 登錄重新導向程式會攔截其各自邏輯登錄視圖的32位和64位登錄，並將它們對應至對應的實體登錄位置。 重新導向程式對應用程式而言是透明的。 因此，32位應用程式可以存取登錄資料（如同在32位 Windows 上執行），即使資料儲存在64位 Windows 的不同位置也一樣。

**ARM 上的 Windows 10：** 除了 x86 應用程式的32位邏輯視圖之外，ARM 上的 Windows 10 也包含32位 ARM 應用程式的個別邏輯視圖。

在重新導向的登錄路徑下，會共用索引鍵的子集。 對共用金鑰的32位登錄呼叫不會重新導向。 相反地，會將金鑰的一個實體複本對應到登錄的每個邏輯視圖。 如需重新導向的金鑰和共用金鑰清單，請參閱 [受 WOW64 影響](shared-registry-keys.md)的登錄機碼。

**Windows server 2008、Windows Vista Windows server 2003 和 Windows XP：** 若要透過 COM 和其他機制來啟用應用程式互通性，重新導向的登錄機碼子集也會 *反映出來*。 登錄反映程式會複製登錄機碼和兩個登錄視圖之間的值，讓它們保持同步。 從 Windows 7 和 Windows Server 2008 R2 開始，已移除登錄反映。 如需詳細資訊，請參閱登錄 [反映](registry-reflection.md)。

下列案例說明如何使用這些邏輯視圖：

-   32位 x86 應用程式會檢查下列登錄機碼是否存在： **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Hello**。 如果機碼不存在，則應用程式會建立其預設值 "Hello 32-bit x86 world";否則，它會讀取並顯示值。
-   相同的應用程式已修改為寫入 "Hello 64-bit world"，而不是 "Hello 32 位 x86 world"，並重新編譯為64位 x64 或 ARM64 應用程式。
-   **ARM 上的 Windows 10：** 相同的應用程式會經過修改，以撰寫 "Hello 32 位 ARM world"，並重新編譯為32位 ARM 應用程式。
-   當32位 x86 應用程式在64位 Windows 上執行時，它會顯示 "Hello 32 位 x86 world"。 當64位應用程式執行時，它會顯示 "Hello 64-bit world"。 **ARM 上的 Windows 10：** 當32位 ARM 應用程式在64位 ARM64 Windows 上執行時，它會顯示 "Hello 32 位 arm world"。 所有應用程式都會使用相同的預先定義控制碼和相同的索引鍵名稱來呼叫相同的登錄函式;差別在於每個應用程式都是在其登錄的邏輯視圖上操作，而且每個視圖都會對應到不同的登錄實體位置，以保持字串的所有版本保持不變。

重新導向的索引鍵會對應至 **Wow6432Node** 下的實體位置。 例如， **HKEY \_ 本機 \_ 電腦 \\ 軟體** 會重新導向至 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Wow6432Node**。 不過，重新導向金鑰的實體位置應該視為系統所保留。 應用程式不應該直接存取金鑰的實體位置，因為這個位置可能會變更。 如需詳細資訊，請參閱 [存取替代登錄視圖](accessing-an-alternate-registry-view.md)。

**ARM 上的 Windows 10：** 重新導向的32位 ARM 金鑰會對應至 WowAA32Node 下的實體位置。

為了協助32位的應用程式撰寫 **REG \_ SZ** 或 REG，將包含% ProgramFiles% 或% commonprogramfiles% 的 **\_ \_ SZ 資料展開** 至登錄，WOW64 會攔截這些寫入作業，並將其取代為 "% ProgramFiles (x86) %" 和 "% commonprogramfiles (x86) %"。 例如，如果 [Program Files] 目錄位於 C 磁片磁碟機上，則 "% ProgramFiles (x86) %" 會展開為 "C： \\ Program Files (x86) "。 只有在符合下列條件時，才會發生取代：

-   字串的開頭必須是% ProgramFiles% 或% commonprogramfiles%。 如果字串開頭為空格或任何字元以外的任何字元，則不會被取代。
-   % ProgramFiles% 或% commonprogramfiles% 的案例必須完全如下所示，因為字串比較會區分大小寫。 例如，如果字串的開頭是% CommonProgramFiles% 而不是% CommonProgramFiles%，就不會被取代。
-   字串不能超過最大 \_ 路徑 \* 2 + 15 個字元。 如果超過此長度，則不會被取代。
-   金鑰無法以 KEY \_ WOW64 \_ 64KEY 開啟。 此旗標指定應在64位登錄視圖上執行機碼上的作業，因此不會被取代。 如需詳細資訊，請參閱 [存取替代登錄視圖](accessing-an-alternate-registry-view.md)。

**Windows server 2008、Windows Vista Windows server 2003 和 Windows XP：** KEY \_ WOW \_ 64 64KEY 旗標不 \_ 會影響是否已取代金鑰。 此旗標會影響從 Windows 7 和 Windows Server 2008 R2 開始的取代。

此外，REG \_ sz 或 reg \_ 會展開 \_ 包含 system32 的 SZ 索引鍵，並以 syswow64 取代。 字串的開頭必須是指向或低於% windir% system32 的路徑 \\ 。 字串比較不區分大小寫。 環境變數會在比對路徑之前展開，所以會取代下列所有路徑：% windir% \\ system32、% SystemRoot% \\ System32 和 C： \\ windows \\ system32。 此修補程式只適用于 Windows 7 之前所反映的金鑰。

如需詳細資訊，請參閱下列主題：

-   [登錄反映](registry-reflection.md)
-   [受 WOW64 影響的登錄機碼](shared-registry-keys.md)
-   [存取替代登錄視圖](accessing-an-alternate-registry-view.md)
-   [WOW64 上的登錄重新導向範例](example-of-registry-reflection-and-redirection-on-wow64.md)
-   [64位 Windows 中的遠端登入存取](remote-registry-access-in-64-bit-windows.md)

 

 




