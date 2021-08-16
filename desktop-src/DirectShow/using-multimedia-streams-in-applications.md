---
description: 使用應用程式中的多媒體串流
ms.assetid: 73cfe89b-df46-445a-92c7-2f7323672441
title: 使用應用程式中的多媒體串流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faadcf755019291ae394d03aac5fb16aa632605b5e1c5bc2a8a457de55343757
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525958"
---
# <a name="using-multimedia-streams-in-applications"></a>使用應用程式中的多媒體串流

> [!Note]  
> 這些 Api 已被取代。 應用程式應該使用 [**範例捕獲**](sample-grabber-filter.md)篩選器或執行自訂篩選，以從 DirectShow 的篩選圖形取得資料。

 

多媒體串流介面可大幅簡化管理多媒體資料的程式，方法是移除硬體或軟體來源特定特性的相依性，並提供所有 Microsoft DirectX®媒體格式的支援。 資料流程會將資料抽象化至非常高層級;應用程式甚至可以將資料從某個資料流程移至另一個資料流程，而不需要知道資料格式的任何資料。

請執行下列步驟來建立多媒體串流。

1.  建立多媒體串流。 建立和初始化資料流程的方法是特定架構。 DirectShow 支援用來初始化資料流程的 [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream)介面。 將會使用不同的機制來建立並初始化 [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) 的其他同進程伺服器。
2.  在多媒體資料流程物件初始化之後，應用程式會使用 **QueryInterface** 來取得物件的 **IMultiMediaStream** 介面。 您可以使用這個介面來判斷資料流程的屬性，並列舉資料流程本身。 您可以藉由呼叫 [**IMultiMediaStream：： GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) 方法（具有特定用途識別碼）來取出特定的資料流程。 MSPID \_ PrimaryVideo 和 MSPID \_ PrimaryAudio （代表主要影片和音訊串流）是最常使用的用途識別碼。
3.  針對資料流程的媒體類型特定的介面呼叫 **IUnknown：： QueryInterface** 。 例如，如果您想要呈現影片串流，請取出其 [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) 介面。 媒體專用介面會定義充分利用格式功能所需的其他方法。
4.  從資料流程資料中建立一或多個範例。 每個媒體串流都支援 [**IMediaStream：： CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample) 方法來建立範例。 產生的範例支援 [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) 介面，此介面可讓您控制範例及其特性。 一般而言，媒體資料流程支援範例建立的格式特定方法，其功能比上述的 **IStreamSample** 方法更強大。 例如， **IDirectDrawMediaStream** 可以建立附加至所需 DirectDraw 表面和裁剪矩形的範例。 不過，在某些情況下，您必須先處理資料，而不需要知道其資料格式。 如果您想要串流與其格式無關的資料，請使用 **IMediaStream：： CreateSharedSample** 方法來建立資料範例。
5.  建立所有所需的資料流程範例之後，請呼叫 [**IMultiMediaStream：： SetState**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-setstate) 方法來啟動資料流程，然後傳入 STREAMSTATE \_ 執行旗標作為其參數。
6.  呼叫 [**IStreamSample：： update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) 以更新資料流程範例。 當 **IStreamSample：： Update** 方法結束時，您可以存取範例的資料。 如果您想要在更新傳回時觸發特定事件或函式呼叫，請將適當的指標傳遞至 **IStreamSample：： update** 方法。

如需多媒體串流介面的詳細資訊，請參閱 [多媒體串流](multimedia-streaming.md)。

 

 



