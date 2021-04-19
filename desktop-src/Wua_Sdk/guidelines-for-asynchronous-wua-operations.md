---
description: 本主題指出當您執行非同步 Windows Update Agent (WUA) 作業時，所遵循的指導方針。
ms.assetid: 1fb16904-732d-4341-8267-ab8896fc0f7c
title: 非同步 WUA 作業的指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a4b2198a235d9a03e3730e5d6dce2cd54c0e1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993046"
---
# <a name="guidelines-for-asynchronous-wua-operations"></a>非同步 WUA 作業的指導方針

本主題指出當您執行非同步 Windows Update Agent (WUA) 作業時，所遵循的指導方針。

-   非同步 WUA 作業不保證任何特定的完成速度。 非同步 WUA 作業的完成時間可能會因電腦硬體、作業系統版本和網路設定而有很大的差異。 如同其他具有網路相依性且不包含超時參數或記載的超時時間的 Windows Api，如果您需要保證的回應時間，建議您考慮執行您自己的超時機制。 例如，您可以建立呼叫非同步 WUA 方法的背景工作執行緒，並且在非同步 WUA 作業完成時設定事件或其他同步處理物件;主執行緒接著可以使用 [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) 或 [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) 函式，讓您指定超時值。
-   當您結束搜尋、下載、安裝或卸載更新時，您可以從任何執行緒使用 [**IUpdateSearcher：： EndSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)、 [**IUpdateDowloader：： EndDownload**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)、 [**IUpdateInstaller：： EndInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-endinstall) 和 [**IUpdateInstaller：： EndUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-enduninstall) 。
-   當您使用 [**IUpdateSearcher：： BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)、 [**IUpdateDownloader：： BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload)、 [**IUpdateInstaller：： BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)和 [**IUpdateInstaller：： BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall)來開始搜尋、下載、安裝或卸載更新時，請確定您在發行對 WUA API 物件的參考時，仍可維護足夠的存取權許可權。
    -   在您終結之前，請確定非同步作業中使用的任何回呼物件都未參考。 在您終結回呼物件的參考計數之前，請先將其回復至初始值。
    -   從對應的 **Begin** 方法所傳回之工作物件的參考，應該由與回呼物件不同的物件來控制。 使用與回呼物件不同的物件，以避免迴圈參考。
    -   如果您嘗試使用回呼物件來控制工作物件的參考，您必須在回呼函式之外呼叫 [**IDownloadJob：：清除**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup)、 [**IInstallationJob：：清除**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)或 [**ISearchJob：：清除**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) 方法，以便中斷工作物件與回呼物件的連接。 您必須先完成此動作，才能釋放 **Begin** 方法所傳回之工作物件的參考。
-   請確定非同步 WUA 作業已完成。 當任何函式之外的所有命令都已完成時，Windows Script Host 可以終止腳本，即使 WUA API 仍具有回呼物件的參考。
    -   使用其中一種 **清除** 方法，或讓回呼函式在完成時設定共用的全域變數。
    -   絕對不要在其回呼函式的工作物件上呼叫 [**IDownloadJob：：清除**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup)、 [**IInstallationJob：：清理**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)或 [**ISearchJob：：清除**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) 。
    -   若要確保在 Windows Internet Explorer 上執行的腳本中有正確的清除順序，請在處理 onbeforeunload 時，對所有工作物件呼叫 **清除** 方法。
-   請勿將使用者自訂資料類型用於非同步 WUA 作業 (UDT) 。 [**IUpdateSearcher：： BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)、 [**IUpdateDownloader：： BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload)、 [**IUpdateInstaller：： BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)或 [**IUpdateInstaller：： BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall)不支援此類型。

 

 
