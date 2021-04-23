---
description: 框架逐步執行屬性集
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: 框架逐步執行屬性集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ccd79feda0e5e2e537390fe5598822fb3787f6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908446"
---
# <a name="frame-stepping-property-set"></a>框架逐步執行屬性集

在 Microsoft DirectShow 下執行框架精確搜尋的解碼器必須實作為 \_ KSPROPSETID \_ FrameStep 屬性集，以搭配 [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) 介面使用。



| 標籤 | 值 |
|-------------------|----------------------------|
| 屬性集 GUID | AM \_ KSPROPSETID \_ FrameStep |



 



| 屬性識別碼                              | 描述                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AM \_ 屬性 \_ FRAMESTEP \_ 步驟            | 指示解碼器開始步驟作業，並傳遞指定步驟數目的 [**AM \_ 屬性 \_ FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) 結構。            |
| AM \_ 屬性 \_ FRAMESTEP \_ 取消          | 指示解碼器取消目前的步驟作業。 沒有任何實例資料與這個屬性相關聯。                                                                  |
| AM \_ 屬性 \_ FRAMESTEP \_ CANSTEP         | \_此指令程式會在此指令上傳回 S OK，表示它可以執行框架逐步執行， \_ 否則為 FALSE。 設定這個屬性時，不會傳遞任何實例資料。         |
| AM \_ 屬性 \_ FRAMESTEP \_ CANSTEPMULTIPLE | \_此指令程式會在此指示上傳回 S OK，表示它可以一次執行多個框架， \_ 否則為 FALSE。 設定這個屬性時，不會傳遞任何實例資料。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[屬性集](property-sets.md)
</dt> </dl>

 

 



