---
title: 遊戲計時與多核心處理器
description: 本文建議更準確、可靠的解決方案，以使用 Windows api QueryPerformanceCounter 和 QueryPerformanceFrequency 來取得高解析度的 CPU 時間。
ms.assetid: 1512324d-dffa-3681-be3f-f63a3b8f11db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed5e668e87a2645859838b1fdf9cfb35263381e9ce9c73fbe72232ad3d3a46cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649346"
---
# <a name="game-timing-and-multicore-processors"></a>遊戲計時與多核心處理器

由於電源管理技術在現今的電腦中變得越來越普遍，所以取得高解析度 CPU 時間的常用方法（RDTSC 指令）可能無法再如預期般運作。 本文建議更準確、可靠的解決方案，以使用 Windows api [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)和 [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)來取得高解析度的 CPU 時間。

-   [背景](#background)
-   [建議](#recommendations)
-   [應用程式相容性](#application-compatibility)

## <a name="background"></a>背景

自 x86 P5 指令集推出之後，許多遊戲開發人員都已使用讀取時間戳記計數器（RDTSC 指令）來執行高解析度的時機。 Windows 的多媒體計時器相當精確，可進行聲音和影片處理，但是在幀時間中，有數十毫秒或更短的時間，它們沒有足夠的解析度來提供差異時間資訊。 許多遊戲仍在啟動時使用多媒體計時器來建立 CPU 的頻率，並使用該頻率值調整 RDTSC 的結果，以取得準確的時間。 由於 RDTSC 的限制，Windows API 會透過 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)和 [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)的常式公開更正確的方式來存取這項功能。

此使用 RDTSC 來因應這些基本問題的時機：

-   不連續的值。 直接使用 RDTSC 會假設執行緒一律在相同處理器上執行。 多處理器和雙核心系統不保證會在核心之間同步處理其迴圈計數器。 相較于在不同時間的閒置和還原各核心的新式電源管理技術，這種技術會產生更多的功能，這會導致核心通常會不同步。 若為應用程式，這通常會導致問題或可能當機，因為執行緒會在處理器之間跳躍，並取得導致大型差異、負面差異或暫停時間的計時值。
-   專用硬體的可用性。 RDTSC 會鎖定應用程式要求給處理器迴圈計數器的計時資訊。 多年來，這是取得高精確度時間資訊的最佳方式，但較新的主機板現在包含專用的計時裝置，可提供高解析度的計時資訊，而不會有 RDTSC 的缺點。
-   CPU 頻率的變化性。 前提是，CPU 的頻率通常是在程式的存留期內固定的。 不過，有了新式電源管理技術，這是不正確的假設。 雖然一開始只能使用膝上型電腦和其他行動裝置，但在許多高階桌上型電腦中，變更 CPU 頻率的技術也是一樣的。使用者通常無法接受停用其功能以維持一致的頻率。

## <a name="recommendations"></a>建議

遊戲需要準確的計時資訊，但您也需要以避免使用 RDTSC 相關問題的方式來執行計時程式碼。 當您執行高解析度的時間時，請採取下列步驟：

1.  使用 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 和 [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) ，而不是 RDTSC。 這些 Api 可能會使用 RDTSC，但可能會使用主機板上的計時裝置，或可提供高品質高解析度計時資訊的一些其他系統服務。 雖然 RDTSC 的速度比 **QueryPerformanceCounter** 快許多，因為後者是 api 呼叫，它是一個 api，可在每個框架中呼叫數百次，而不會產生顯著的影響。  (不過，開發人員應該嘗試讓遊戲盡可能地呼叫 **QueryPerformanceCounter** ，以避免任何效能下降。 ) 
2.  計算差異時，應該壓制這些值，以確保時間值中的任何錯誤都不會造成當機或不穩定的時間相關計算。 此夾具範圍應為 0 (，以防止負面差異值) 為根據您預期的最小畫面播放速率的合理值。 固定在應用程式的任何偵錯工具中可能很有用，但如果在某些未優化的模式下進行效能分析或執行遊戲，請務必記住這點。
3.  計算單一線程上的所有時間。 計算多個執行緒（例如，每個與特定處理器相關聯的執行緒）的時間，可大幅降低多核心系統的效能。
4.  使用 Windows API [**SetThreadAffinityMask**](/windows/win32/api/winbase/nf-winbase-setthreadaffinitymask)，將單一線程設定為保留在單一處理器上。 一般來說，這是主要的遊戲執行緒。 雖然 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 和 [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) 通常會針對多個處理器進行調整，但 BIOS 或驅動程式中的錯誤可能會導致這些常式線上程從一個處理器移至另一個處理器時傳回不同的值。 因此，最好將執行緒保持在單處理器上。

    所有其他執行緒應該都能運作，而不需要收集自己的計時器資料。 我們不建議使用背景工作執行緒來計算時間，因為這會成為同步處理的瓶頸。 相反地，工作者執行緒應該從主執行緒讀取時間戳記，因為工作者執行緒只會讀取時間戳記，所以不需要使用重要區段。

5.  只呼叫 [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) 一次，因為當系統正在執行時，頻率不會變更。

## <a name="application-compatibility"></a>應用程式相容性

許多開發人員已經對 RDTSC 的行為進行了許多方面的假設，因此當時間執行時，某些現有的應用程式很有可能會在具有多個處理器或核心的系統上執行時出現問題。 這些問題通常會以瑕疵或緩慢移動的方式來表現。 對於不知道電源管理的應用程式並不容易，但有一個現有的填充碼可以強制應用程式一律在多處理器系統中的單一處理器上執行。

若要建立此填充碼，請從[Windows 應用程式相容性](/archive/blogs/yongrhee/download-application-compatibility-toolkit-act-for-windows-10)下載 Microsoft 應用程式相容性工具組。

使用工具組的 [相容性管理員]，建立應用程式的資料庫和相關聯的修正程式。 為此資料庫建立新的相容性模式，並選取相容性修正 **SingleProcAffinity** ，以強制應用程式的所有線程都在單一處理器/核心上執行。 藉由使用命令列工具 Fixpack.exe (也是工具組) 的一部分，您可以將此資料庫轉換成可安裝的套件以進行安裝、測試和散發。

如需使用相容性系統管理員的指示，請參閱工具組的檔。 如需使用 Fixpack.exe 的語法和範例，請參閱其命令列說明。

如需客戶導向的資訊，請參閱下列來自 Microsoft 說明及支援的知識庫文章：

-   [使用 QueryPerformanceCounter 函式的程式在 Windows Server 2003 和 Windows XP](https://support.microsoft.com/kb/895980) (文章895980中的執行效能可能不佳) 
-   在[使用雙核心處理器的 Windows XP 電腦上，遊戲效能可能不佳](https://support.microsoft.com/kb/909944) (文章 909944) 

 

 
