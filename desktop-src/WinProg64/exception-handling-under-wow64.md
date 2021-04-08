---
title: WOW64 下的例外狀況處理
description: WOW64 使用原生 x64、ia64 或 ARM64 例外狀況做為 x86 例外狀況的傳輸。 因此，在 WOW64 下執行的32位應用程式中，未攔截的例外狀況行為就像原生64位例外狀況。
ms.assetid: 2EE1A1F3-A691-4ee6-9587-7FF7C4F9DD98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb57e56b85be4769d452a5772ff7b0024724641
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023956"
---
# <a name="exception-handling-under-wow64"></a>WOW64 下的例外狀況處理

WOW64 使用原生 x64、ia64 或 ARM64 例外狀況做為 x86 例外狀況的傳輸。 因此，在 WOW64 下執行的32位應用程式中，未攔截的例外狀況行為就像原生64位例外狀況。

在32位版本的 Windows 上執行的應用程式中，未攔截的例外狀況會傳遞至應用程式的較高層級例外狀況處理常式（如果有的話）。 在 WOW64 下執行的相同32位應用程式中，系統可能會隱藏未攔截的例外狀況。

**Windows Vista、Windows Server 2003 和 WINDOWS XP：** 在 WOW64 下執行的相同32位應用程式中，系統會呼叫例外狀況篩選器，但可能隱藏未攔截的例外狀況，而不會叫用相關聯的處理常式。 從 Windows Vista Service Pack 1 (SP1) 開始，此行為已變更。

如需視窗程式中未攔截之例外狀況的詳細資訊，請參閱 [WindowProc](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數。

 

 