---
description: DbgHelp 程式庫是由 DbgHelp.dll 所執行。
ms.assetid: 8ef1740d-c791-4fbd-8297-7207a987c09d
title: DbgHelp 版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5adb00c6442f7ba36f5aeb86e0255e175131492124d08fbf865e57a9721a7893
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343858"
---
# <a name="dbghelp-versions"></a>DbgHelp 版本

DbgHelp 程式庫是由 DbgHelp.dll 所執行。 雖然此 DLL 包含在所有支援的 Windows 版本中，但很少會提供最新的 DbgHelp 版本。 此外，Windows 隨附的 DbgHelp 版本已減少其他版本的功能，特別是它缺少符號伺服器和來源伺服器的支援。

DbgHelp.dll、SymSrv.dll 和 SrcSrv.dll 的最新版本，可作為 Windows 封裝之[偵錯工具](https://developer.microsoft.com/windows/downloads/windows-10-sdk)的一部分。 這些內含 Dll 的重新發佈原則的設計目的，是要讓人們盡可能輕鬆地將這些檔案包含在自己的套件和版本中。

> [!Caution]  
> 使用者絕對不應該嘗試將 DbgHelp.dll [Windows 版本的偵錯工具](https://developer.microsoft.com/windows/downloads/windows-10-sdk)安裝到 Windows 系統目錄中，因為它們在此案例中經過測試，而且可能會使系統不穩定。 有不同的 X64 和 X86 版本的偵錯工具套件，而且對於同時支援這兩個平臺的人員來說，兩者都是必要的。

若要取得 DbgHelp.dll 的最新版本，請移至 [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) 並下載 Windows 的偵錯工具。 如需正確安裝的詳細資訊，請參閱 [呼叫 DbgHelp 程式庫](calling-the-dbghelp-library.md) 。

> [!Note]  
> Windows 中隨附的 DbgHelp.dll 檔案無法轉散發套件。

許多版本的 DbgHelp 都包含額外的功能。 若要確保您的應用程式可以使用正確的 DbgHelp 版本，請參閱特定 API 參考檔中的需求資訊。
