---
description: 下列程式描述如何啟用偵錯工具追蹤和記錄。
ms.assetid: 52381397-df75-4d81-a048-f0ed408ac6b8
title: 如何啟用衍生 Msp 的偵錯工具追蹤/記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3883d12c050f245cc58595c9a52586c4f01ba27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974145"
---
# <a name="how-to-enable-debug-tracinglogging-for-derived-msps"></a><span data-ttu-id="80574-103">如何啟用衍生 Msp 的偵錯工具追蹤/記錄</span><span class="sxs-lookup"><span data-stu-id="80574-103">How to Enable Debug Tracing/Logging for Derived MSPs</span></span>

<span data-ttu-id="80574-104">首先，請確定衍生的 MSP 採用上一節中的指導方針，包括偵錯工具追蹤 (定義預處理器符號 MSPLOG、在 DllMain 期間註冊追蹤，以及使用記錄宏追蹤) 。</span><span class="sxs-lookup"><span data-stu-id="80574-104">First, make sure that the implementation of the derived MSP has followed the guidelines in the previous section with regard to debug tracing (defining the preprocessor symbol MSPLOG, registering for tracing during DllMain, and using the LOG macro for tracing).</span></span> <span data-ttu-id="80574-105">找出 MSP 在註冊追蹤時所使用的名稱 (這通常應該是 DLL 的名稱;以下是「 &lt; dll 名稱」 ) 的參考 &gt; 。</span><span class="sxs-lookup"><span data-stu-id="80574-105">Find out what name the MSP uses when registering for tracing (this should usually be the DLL's name; it is referred to below as "&lt;dll name&gt;").</span></span> <span data-ttu-id="80574-106">若要啟用追蹤，請使用登錄編輯程式 ( "Regedit.exe" 或 "Regedt32.exe" ) 找出「HKEY \_ 本機 \_ 電腦軟體 Microsoft 追蹤」機碼 \\ \\ \\ ，並執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="80574-106">To enable tracing, use a registry editor ("Regedit.exe" or "Regedt32.exe") to locate the key "HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Tracing" and do the following.</span></span> <span data-ttu-id="80574-107">請注意，以下所述的所有值（EnableDebuggerTracing 值除外）都應該在您第一次執行 MSP 之後自動建立。</span><span class="sxs-lookup"><span data-stu-id="80574-107">Note that all of the values mentioned below, except the EnableDebuggerTracing value, should be created automatically after running your MSP for the first time.</span></span>

-   <span data-ttu-id="80574-108">若要啟用使用者和核心模式偵錯工具的追蹤，請將 **DWORD** 值 <dll name> \\ EnableDebuggerTracing 設定為1。</span><span class="sxs-lookup"><span data-stu-id="80574-108">To enable tracing to user and kernel mode debuggers, set the **DWORD** value <dll name>\\EnableDebuggerTracing to 1.</span></span> <span data-ttu-id="80574-109">您也可以選擇使用 **DWORD** 值 <dll name> \\ ConsoleTracing Mask 來啟用或停用不同層級的追蹤輸出 (預設為0xFFFF0000，這會讓所有的追蹤層級都) 。</span><span class="sxs-lookup"><span data-stu-id="80574-109">Optionally, use the **DWORD** value <dll name>\\ConsoleTracing Mask to enable or disable various levels of trace output (the default is 0xFFFF0000, which enables all trace levels).</span></span>
-   <span data-ttu-id="80574-110">若要啟用檔案的追蹤，請將 **DWORD** 值 <dll name> \\ EnableFileTracing 設定為1。</span><span class="sxs-lookup"><span data-stu-id="80574-110">To enable tracing to a file, set the **DWORD** value <dll name>\\EnableFileTracing to 1.</span></span> <span data-ttu-id="80574-111">（選擇性）使用字串值 <dll name> \\ FileDirectory 來調整記錄檔的位置。</span><span class="sxs-lookup"><span data-stu-id="80574-111">Optionally, use the string value <dll name>\\FileDirectory to adjust the location of the log file.</span></span> <span data-ttu-id="80574-112">您也可以選擇使用 **DWORD** 值 <dll name> \\ FileTracingMask 來啟用或停用不同層級的追蹤輸出 (預設為0xFFFF0000，這會啟用所有追蹤層級) 。</span><span class="sxs-lookup"><span data-stu-id="80574-112">Optionally, use the **DWORD** value <dll name>\\FileTracingMask to enable or disable various levels of trace output (the default is 0xFFFF0000, which enables all trace levels).</span></span>
-   <span data-ttu-id="80574-113">若要啟用個別主控台視窗的追蹤（以 DLL 分隔），請將 **dword** 值 EnableConsoleTracing 設定為1，並將 **dword** 值 <dll name> \\ EnableConsoleTracing 設定為1。</span><span class="sxs-lookup"><span data-stu-id="80574-113">To enable tracing to a separate console window, separated by DLL, set the **DWORD** value EnableConsoleTracing to 1, AND ALSO set the **DWORD** value <dll name>\\EnableConsoleTracing to 1.</span></span> <span data-ttu-id="80574-114">您也可以選擇使用 **DWORD** 值 <dll name> \\ ConsoleTracing Mask 來啟用或停用不同層級的追蹤輸出 (預設為0xFFFF0000，這會讓所有的追蹤層級都) 。</span><span class="sxs-lookup"><span data-stu-id="80574-114">Optionally, use the **DWORD** value <dll name>\\ConsoleTracing Mask to enable or disable various levels of trace output (the default is 0xFFFF0000, which enables all trace levels).</span></span>

 

 



