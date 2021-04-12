---
title: 調試 WOW64
description: 在 WOW64 下執行的應用程式可以使用 x86 裝載的偵錯工具或原生偵錯工具來進行調試。
ms.assetid: e0945bdd-998d-4531-869f-21c505cb2135
keywords:
- WOW64 64 位 Windows 程式設計，偵錯工具
- 偵錯工具 WOW64 64 位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc7590b0b4f44f9e1a48a204723fb0652b9c2e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382585"
---
# <a name="debugging-wow64"></a>調試 WOW64

在 WOW64 下執行的應用程式可以透過兩種方式進行調試：

-   使用 x86 裝載的偵錯工具，例如 NTSD、WinDbg 或 Visual Studio。 32位的 NTSD 已安裝到零售安裝上的% systemroot% \\ syswow64。 請注意，您可以使用 x86 偵錯工具來對 x86 程式碼進行偵錯工具，但無法使用它來對 WOW64 Thunk 層中的中斷點進行拆解或設定，因為它是64位的原生程式碼。
-   使用原生偵錯工具，例如 CDB、NTSD 或 WinDbg 以及 WOW64 偵錯工具擴充功能，Wow64exts.dll。 如果原生偵錯工具在處理器為 x86 模式時中斷，偵錯工具會以 x86 進程的形式呈現進程。 如果處理器處於原生模式中，偵錯工具會以原生模式呈現進程。

適用于 Windows 的偵錯工具中包含了 CDB、NTSD 和 WinDbg。 如需詳細資訊，請參閱 [Windows 的偵錯工具](/windows-hardware/drivers/debugger/) 檔。

Wow64exts 偵錯工具擴充功能與 WinDbg 一起安裝。 使用！ load wow64exts 命令載入偵錯工具擴充功能。 下表列出！ wow64exts 偵錯工具延伸模組命令。



| 命令                | 描述                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| ！ wow64exts sw          | 在 x86 和原生模式之間切換。                                                                                                    |
| ！ wow64exts 的 *計數*   | 傾印結合的32位/64 位堆疊追蹤。 如果指定 *count* ，此命令會傾印每個堆疊追蹤中的第一個 *計數* 位址。  |
| ！ wow64exts.info        | 傾印程式 PEB 的基本資訊、目前線程的 TEB，以及 WOW64 所使用的執行緒區域儲存 (TLS) 位置。 |
| ！ wow64exts。 r *位址* | 傾印指定位址的內容。 如果未指定 *address* ，命令會傾印處理器的內容。                     |



 

 

 