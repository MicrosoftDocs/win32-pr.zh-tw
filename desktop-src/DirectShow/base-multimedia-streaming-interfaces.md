---
description: 基底多媒體串流介面
ms.assetid: a94dbb64-dfca-4c24-8c11-761835faf8a8
title: 基底多媒體串流介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b715a68bd65a2fa3a3923edf10f0e2d1f6c22edb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945718"
---
# <a name="base-multimedia-streaming-interfaces"></a>基底多媒體串流介面

> [!Note]  
> 這些 Api 已被取代。 應用程式應該使用 [**範例捕獲**](sample-grabber-filter.md) 篩選器或執行自訂篩選，以從 DirectShow 篩選圖形取得資料。

 

基底多媒體串流介面提供以程式設計方式存取多媒體串流。 不過，使用基底介面來存取特定類型的資料，可能會限制您對資料的控制量，因此媒體開發人員應建立這些介面的衍生版本，以提供更強大的功能來控制其媒體類型的獨特功能。



| 介面                                      | 描述                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) | 定義如何存取最高層級的多媒體資料流程物件;此物件包含和提供其他資料流程物件的存取權。 [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) 有列舉或取出特定資料流程的方法，以及檢查資料流程的總時間持續時間和搜尋。                                                                                                       |
| [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)           | 定義泛型資料流程物件。 您可以使用其方法來取出資料流程的指標、取得資料流程的相關資訊，以及從資料流程資料建立範例。 您也可以建立共用的資料流程範例，讓多個資料流程可以存取，而不需要複製範例的資料。                                                                                                                                                  |
| [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)         | 控制特定資料流程範例的行為。 您可以取出建立範例的資料流程、檢查範例的開始和結束時間和完成狀態，然後在範例本身 (透過 [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) 方法) 來執行使用者定義函數。 一般而言，Update 方法會以適當的方式處理範例資料，例如轉譯影片資料或播放音訊資料。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[多媒體串流介面的清單](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



