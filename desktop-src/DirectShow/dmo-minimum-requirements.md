---
description: DMO最低需求
ms.assetid: cd342f0f-a3dc-4623-a18f-c45071795ef4
title: DMO最低需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7acc4f664d32112512120f2f20687051a0bff193e00adb7ad595e6975c522fce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749138"
---
# <a name="dmo-minimum-requirements"></a>DMO最低需求

每個 DMO 都應符合下列最低需求：

-   它必須支援匯總。
-   它必須公開 [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) 介面。
-   執行緒模型必須是「兩者」。 DMOs 必須在自由執行緒環境中正確運作。

音訊效果 DMOs 應該支援 [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) 介面，以便在 DirectMusic 和 DirectSound 中使用。

下列是在其他地方記載的介面，但很適合用於許多 DMOs。 不過，它們並不是必要的。

-   **ISpecifyPropertyPages**， **IPropertyPage**：這些介面可讓 DMO 提供屬性頁，讓使用者可以設定屬性。
-   **IPersistStream**：此介面可讓 DMO 將其狀態儲存至持續性儲存體。
-   [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)、 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)：這些介面可讓用戶端設定編碼器的輸出格式和壓縮設定。  (這兩個介面都是 DirectShow API 的一部分，也建議 DMOs 使用。 ) 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫 DMO](writing-a-dmo.md)
</dt> </dl>

 

 



