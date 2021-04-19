---
description: .
ms.assetid: fe19e337-3109-42d6-a704-70662ac7c684
title: 啟用 Intel AVX 的 Windows 7 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440c71c5fd6aa65b5e56b8dfb0b6eab134418192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987804"
---
# <a name="enable-windows-7-support-for-intel-avx"></a>啟用 Intel AVX 的 Windows 7 支援

## <a name="affected-platforms"></a>受影響的平臺

 **客戶** 端-WINDOWS 7 SP1  
**伺服器** -Windows Server 2008 R2 SP1  


## <a name="feature-impact"></a>功能影響

 **嚴重性** -低  
**頻率** -低  





## <a name="description"></a>Description

Intel<sup>？</sup> Advanced Vector Extensions (AVX) <sup>？</sup> 是 Intel 架構的256位 SIMD 浮點數向量延伸。 它包含指令和註冊集合的延伸。

Microsoft 開發了一些 API 增強功能（例如 XState 函式），可讓應用程式存取和操作擴充的處理器功能資訊和狀態，包括 AVX。

## <a name="usage-scenarios"></a>使用案例

有三個一般層級的潛在影響。

**層級1：** 即使應用程式呼叫程式庫，或使用間接使用或產生 Intel AVX 擴充功能的編譯器，未直接使用 Intel AVX 的應用程式也不會看到其功能的任何影響。 這代表大部分的應用程式。

**層級2：** 明確使用 Intel AVX 指令集的 Advanced 應用程式將能夠在發生硬體例外狀況時存取及變更 AVX 暫存器內容。 許多應用程式都屬於此類別，因為它表示在例外狀況發生時所執行之指令資料流程的相關知識，例如以組合語言撰寫的應用程式，或是在執行時間產生電腦程式代碼的應用程式 (例如，具有即時編譯) 的 managed 程式碼執行時間。

**層級3：** 偵錯工具應用程式將能夠在所要進行的應用程式中存取和操作 AVX 狀態。

## <a name="how-to-leverage-feature-capabilities"></a>如何運用功能功能

**層級1：** 應用程式不需要採取任何動作，就能使用 Intel AVX。

**層級2：** 此類別中的應用程式可以選擇在例外狀況發生時，從例外狀況篩選準則中存取和操作 AVX 狀態。 透過 GetExceptionInformation 取得基底處理器內容之後，篩選準則應：

 **1.** 檢查 **內容 \_ XSTATE** 旗標的值。 此旗標表示內容中至少存在一個 XState 功能。  
**2.** 如果是這種情況，請呼叫 **GetXStateFeaturesMask** ，然後在傳回的遮罩中測試 **XSTATE \_ AVX** 旗標的值。 這表示內容中的 AVX 狀態是否存在。  
**3.** 呼叫 **LocateXStateFeature** 來取出儲存 AVX 狀態的實際位置。  

**層級3：** 除非您想要存取 Intel AVX 註冊，否則不需要更新現有的偵錯工具應用程式：

**1.** 若要判斷是否已啟用 AVX，偵錯工具應該使用：

-   GetEnabledXStateFeatures 在 x86 或 x64 處理器上取得啟用的 XState 功能遮罩，以在使用 XState 處理器功能或嘗試操作 XState 內容之前，判斷系統上存在和啟用的功能

  
**2.** 如果有 AVX，而且您想要從正在進行調試的應用程式取出並操作 AVX 狀態 (例如 GetThreadCoNtext 和 SetThreadCoNtext) ，偵錯工具應該使用：

-   InitializeCoNtext 函式，可在緩衝區內以所需的大小和對齊方式初始化內容結構
-   CopyCoNtext 函式，用來複製來源內容結構 (包括任何 XState) 至初始化的目的地內容結構

  
**3.** 若要測試、設定及找出處理器內容中的 AVX 狀態，偵錯工具應該使用：

-   LocateXStateFeature，以取得內容結構內個別 XState 功能的處理器狀態指標
-   GetXStateFeaturesMask，以傳回在內容結構內設定之 XState 功能的遮罩
-   SetXStateFeaturesMask，以設定在內容結構內設定之 XState 功能的遮罩

  


## <a name="links-to-other-resources"></a>其他資源的連結

-   如需 Windows SDK 中 XState 函式的詳細資訊，請參閱 [偵錯工具功能](../debug/debugging-functions.md)。
-   如需 Intel AVX 的指示和功能概述，請參閱 [INTEL AVX：效能改進和能源效率的新新領域](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/)。

 

 
