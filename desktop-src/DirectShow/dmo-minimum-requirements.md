---
description: SQL-DMO 最低需求
ms.assetid: cd342f0f-a3dc-4623-a18f-c45071795ef4
title: SQL-DMO 最低需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c26267f50619062fb8396f93b7578db4d3d8c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935903"
---
# <a name="dmo-minimum-requirements"></a>SQL-DMO 最低需求

每個時都應該符合下列最低需求：

-   它必須支援匯總。
-   它必須公開 [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) 介面。
-   執行緒模型必須是「兩者」。 DMOs 必須在自由執行緒環境中正確運作。

音訊效果 DMOs 應該支援 [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) 介面，以便在 DirectMusic 和 DirectSound 中使用。

下列是在其他地方記載的介面，但很適合用於許多 DMOs。 不過，它們並不是必要的。

-   **ISpecifyPropertyPages**， **IPropertyPage**：這些介面可讓您提供屬性頁，讓使用者設定屬性。
-   **IPersistStream**：此介面可讓 sql-dmo 將其狀態儲存至持續性儲存體。
-   [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)、 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)：這些介面可讓用戶端設定編碼器的輸出格式和壓縮設定。  (這兩個介面都是 DirectShow API 的一部分，但也建議 DMOs。 ) 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫 SQL-DMO](writing-a-dmo.md)
</dt> </dl>

 

 



