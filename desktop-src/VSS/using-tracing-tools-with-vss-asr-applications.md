---
description: 您可以使用 Logman 工具，針對使用自動化系統復原 (ASR) 的 VSS 應用程式收集追蹤資訊。
ms.assetid: 872609c8-a123-40a8-96ca-58f34d37f3d8
title: 使用追蹤工具搭配 ASR 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c13eee1c62cd6636eebe5bcfd35bd5abb119645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971000"
---
# <a name="using-tracing-tools-with-asr-applications"></a>使用追蹤工具搭配 ASR 應用程式

您可以使用 Logman 工具，針對使用 [自動化系統復原 (ASR) ](using-vss-automated-system-recovery-for-disaster-recovery.md)的 VSS 應用程式收集追蹤資訊。 Logman (logman.exe) 是追蹤事件和效能計數器的追蹤控制器。 它包含在 Windows XP 和更新版本的 Windows 中。 或者，如果您想要的話，也可以使用 Tracelog.exe 工具來收集相同的 ASR 追蹤資訊。 Tracelog.exe 包含在 Windows 驅動程式套件 (WDK) 中。

若要搭配使用追蹤工具與 VSS，請參閱搭配 [Vss 使用追蹤工具](using-tracing-tools-with-vss.md)。

## <a name="using-logman"></a>使用 Logman

下列程式說明如何搭配使用 Logman 與 ASR 應用程式。

**使用 Logman 搭配您的 ASR 應用程式**

1.  使用下列命令來開始追蹤：

    **logman 啟動 asr-o** *x： \\ * * * asr-ets-p {6407345b-94f2-44c8-b3db-4e076be46816} 0xff 0xff**

    > [!Note]  
    > 以您想要 \\ 儲存追蹤記錄檔的目錄路徑取代 "x："。 為了達到最佳效能，追蹤記錄檔應該位於不是陰影複製一部分的磁片區上。

     

2.  使用下列命令停止追蹤：

    **logman 停止 asr-ets**

追蹤記錄檔為 *x： \\* asr。

如需 Logman 工具的詳細資訊，請參閱 [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11))。

## <a name="using-tracelog"></a>使用 Tracelog.exe

下列程式說明如何使用 Tracelog.exe。

**使用 Tracelog.exe**

1.  建立名為 asr 的文字檔，其中只包含下列文字：

    **6407345b-94f2-44c8-b3db-4e076be46816 asr**

2.  使用下列命令來開始追蹤：

    **tracelog.exe-啟動 asr-f** *x： \\ * * * asr-guid asr。 ctl-旗標 0xff-level 0xff**

    > [!Note]  
    > 以您想要 \\ 儲存追蹤記錄檔的目錄路徑取代 "x："。 為了達到最佳效能，追蹤記錄檔應該位於不是陰影複製一部分的磁片區上。

     

3.  使用下列命令停止追蹤：

    **tracelog.exe-停止 asr**

追蹤記錄檔為 *x： \\* asr。

如需 Tracelog.exe 工具的詳細資訊，請參閱 [tracelog.exe](https://msdn.microsoft.com/library/ms797927.aspx)。

 

 
