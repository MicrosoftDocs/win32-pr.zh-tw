---
description: .
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: 離線登錄庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a473bde729a0047a56d7ad0fdec1c0e3133ea103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972123"
---
# <a name="offline-registry-library"></a>離線登錄庫

## <a name="purpose"></a>目的

離線登錄庫 (Offreg.dll) 用來修改作用中系統登錄之外的登錄 hive。 此程式庫適用于登錄更新案例，例如服務作業系統映射。 從 Windows Vista 開始，程式庫支援登錄 hive 格式。

## <a name="developer-audience"></a>開發人員對象

這項技術適用于原始設備製造商 (Oem) 、防毒軟體和反惡意程式碼軟體廠商，以及必須能夠剖析登錄 hive 檔案的其他應用程式開發人員，而不需要將它們載入 active registry。

## <a name="run-time-requirements"></a>執行階段需求求

離線登錄庫會以二進位可轉散發的動態連結程式庫的形式提供， (DLL) 。 此程式庫會在下列版本的 Windows 上執行：

<dl> Windows Server 2016  
Windows 10  
Windows 8.1  
Windows Server 2012 R2  
Windows 8  
Windows Server 2012  
Windows 7  
Windows Server 2008 R2  
Windows Server 2008  
Windows Vista  
</dl>

應用程式應該使用動態連結連結至 Offreg.dll。

Offreg.dll 是在適用于 Windows 10 和較早版本 Windows 作業系統的 Windows 驅動程式套件 (WDK) 中提供。

如需取得 WDK 的詳細資訊，請參閱 [如何取得 wdk 和 WLK](/windows-hardware/drivers/download-the-wdk) 或造訪 [MSDN 訂閱](https://msdn.microsoft.com/subscriptions/default.aspx) 網站。

## <a name="in-this-section"></a>本節內容

-   [**關於離線登錄庫**](about-the-offline-registry-library.md)
-   [**離線登錄庫函數**](offline-registry-library-functions.md)

 

 
