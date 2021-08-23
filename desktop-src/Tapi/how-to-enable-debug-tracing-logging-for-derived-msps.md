---
description: 下列程式描述如何啟用偵錯工具追蹤和記錄。
ms.assetid: 52381397-df75-4d81-a048-f0ed408ac6b8
title: 如何啟用衍生 Msp 的偵錯工具追蹤/記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565b66055a43edbe7556e640f8e368aab84fab206bced431c22578a7e21a94ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140521"
---
# <a name="how-to-enable-debug-tracinglogging-for-derived-msps"></a>如何啟用衍生 Msp 的偵錯工具追蹤/記錄

首先，請確定衍生的 MSP 採用上一節中的指導方針，包括偵錯工具追蹤 (定義預處理器符號 MSPLOG、在 DllMain 期間註冊追蹤，以及使用記錄宏追蹤) 。 找出 MSP 在註冊追蹤時所使用的名稱 (這通常應該是 DLL 的名稱;以下是「 &lt; dll 名稱」 ) 的參考 &gt; 。 若要啟用追蹤，請使用登錄編輯程式 ( "Regedit.exe" 或 "Regedt32.exe" ) 找出「HKEY \_ 本機 \_ 電腦軟體 Microsoft 追蹤」機碼 \\ \\ \\ ，並執行下列動作。 請注意，以下所述的所有值（EnableDebuggerTracing 值除外）都應該在您第一次執行 MSP 之後自動建立。

-   若要啟用使用者和核心模式偵錯工具的追蹤，請將 **DWORD** 值 <dll name> \\ EnableDebuggerTracing 設定為1。 您也可以選擇使用 **DWORD** 值 <dll name> \\ ConsoleTracing Mask 來啟用或停用不同層級的追蹤輸出 (預設為0xFFFF0000，這會讓所有的追蹤層級都) 。
-   若要啟用檔案的追蹤，請將 **DWORD** 值 <dll name> \\ EnableFileTracing 設定為1。 （選擇性）使用字串值 <dll name> \\ FileDirectory 來調整記錄檔的位置。 您也可以選擇使用 **DWORD** 值 <dll name> \\ FileTracingMask 來啟用或停用不同層級的追蹤輸出 (預設為0xFFFF0000，這會啟用所有追蹤層級) 。
-   若要啟用個別主控台視窗的追蹤（以 DLL 分隔），請將 **dword** 值 EnableConsoleTracing 設定為1，並將 **dword** 值 <dll name> \\ EnableConsoleTracing 設定為1。 您也可以選擇使用 **DWORD** 值 <dll name> \\ ConsoleTracing Mask 來啟用或停用不同層級的追蹤輸出 (預設為0xFFFF0000，這會讓所有的追蹤層級都) 。

 

 



