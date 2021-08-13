---
title: 關於映射主控 API
description: 本檔著重于 IMAPI.EXE for Microsoft (IMAPIv1) 的 Adaptec 實作為的說明。
ms.assetid: 596ec3ea-17d1-4e60-8789-528ff00ae421
keywords:
- 映射主控 API IMAPI.EXE，描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb16ab8c542e7c4686c7a3f4d027169a520495a8d3fab9927f11ed974deeef6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451900"
---
# <a name="about-the-image-mastering-api"></a>關於映射主控 API

本檔著重于 IMAPI.EXE for Microsoft (IMAPIv1) 的 Adaptec 實作為的說明。 因此，本檔包含四個主要 COM 物件及其介面的描述。 四個主要物件如下： **MSDiscMasterObj**、 **MSDiscRecorderObj**、 **MSDiscStashObj** 和 **MSBurnEngineObj**。

系統上可能會有多個 **MSDiscMasterObj** 物件具現化，但是一次只能有一個應用程式可存取錄製器。 **MSDiscMasterObj** 會實作為多個介面，如下列物件圖所示。

![msdiscmasterobj 會實作為多個介面](images/imapi.png)

應用程式會使用 [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) 介面來執行下列工作：

-   開啟 IMAPI.EXE
-   列舉支援的格式 (Joliet 和 Redbook) 
-   選取格式
-   取得記錄器清單
-   選取錄製器
-   開始燒錄

選取格式時， [**IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) 和 [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster) 介面會透過 [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) 介面傳回給應用程式。 這些介面會分別控制資料或音訊光碟的內容。 每個應用程式都不應該瞭解特定的格式介面。 應用程式可以存取 **IJolietDiscMaster** 介面的一般屬性，例如磁片區名稱或舊版檔案名。

**MSDiscRecorderObj** 物件是透過 [**IDiscRecorder**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder) 介面進行存取。 每個與 IMAPI.EXE 相容的 CD-R 或 CD-RW 裝置都有對應的 **MSDiscRecorderObj** 物件。 應用程式會使用這些物件上 **IDiscRecorder** 介面的指標，來選取 imapi.exe 要用來錄製 CD 的裝置。 此外，應用程式也可以透過 **IDiscRecorder** 存取錄製器的一般屬性。 這包括做為寫入器速度或其他燒錄參數的屬性。

其餘的物件（ **MSDiscStashObj** 和 **MSBURNENGINEOBJ**）是 imapi.exe 所存取的內建物件。 此處提及的只是用來闡明 IMAPI.EXE 架構。 **MSDiscStashObj** 透過 **IDiscStash** 介面表示 (，) **MSDiscMasterObj** 用來建立要燒錄之音訊影像或資料光碟的大小（大小上限為 800 MB）。 當從較低層級的引擎要求燒錄時，會透過 **IMSBurnEngine** 介面將隱藏專案傳遞至 **MSBurnEngineObj** () 。 **MSBurnEngineObj** 物件預期隱藏內容的格式必須是已知的格式。 在這方面， **MSDiscMasterObj** 和 **MSBurnEngineObj** 有關于隱藏專案內容的合約。

 

 




