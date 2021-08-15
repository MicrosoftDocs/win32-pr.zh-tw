---
description: 如果執行緒正在等候核心模式回呼完成，執行緒的使用者模式端將會在呼叫 ZwCallbackReturn 函數時延遲。
ms.assetid: 6d6d4f94-0e8c-4469-b905-731be6c4083d
title: 偵測 Kernel-Mode 回呼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029ecf7d5b1f9220de51c2ecffe4bdf30da4cbd088d9d251fd0d24bab04934e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691448"
---
# <a name="detecting-kernel-mode-callbacks"></a>偵測 Kernel-Mode 回呼

Windows 作業系統的大部分程式碼會在核心模式中執行。 每當應用程式執行緒從 Windows API 呼叫函式，而該函式會呼叫必須在核心模式中執行的內部系統函式時，處理器模式就會從使用者模式切換為核心模式。 在控制權回到函式之前，處理器模式會回到使用者模式，以便保護系統資料。

如果執行緒正在等候核心模式回呼完成，執行緒的使用者模式端將會在呼叫 **ZwCallbackReturn** 函數時延遲。

 

 



