---
title: Internet-Aware 物件
description: Internet-Aware 物件
ms.assetid: a8228431-5a07-4816-938d-c789ab6a8eaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280141d4bc9cb1a6a6c685c4badde0b24609996683e73c74f69637440b39ef8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756148"
---
# <a name="internet-aware-objects"></a>Internet-Aware 物件

某些類別會識別為涵蓋持續性介面;這是因為定義控制項在網際網路上的運作方式所造成的。 不支援完整範圍持續性介面的容器應確定它不會裝載需要不支援的介面組合的控制項。

下表說明各種類別的意義，這兩個類別都是已實和必要的類別。



| 必要類別                                                                                                                                                                                | 描述                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CATID \_ PersistsToMoniker、catid \_ PERSISTSTOSTREAMINIT、catid \_ PersisitsToStream、CATID \_ PersistsToStorage、CATID \_ PERSISTSTOMEMORY、catid \_ PersistsToFile、catid \_ PersistsToPropertyBag<br/> | 這些類別中的每一個都是互斥的，只有在物件只支援一個持續性機制時，才會使用，因此會) 相互排除的 (。 不支援其中一個類別所描述之持續性機制的容器，應該防止自己建立任何類別的物件，因此會標示出來。<br/> |
| CATID \_ RequiresDataPathHost<br/>                                                                                                                                                             | 物件需要能夠將資料儲存至一或多個路徑，而且需要容器介入，因此需要 [**IBindHost**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85))的容器支援。<br/>                                                                                                                                  |



 



| 實作為類別                                                                                                                                                                            | 描述                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| CATID \_ PersistsToMoniker、catid \_ PERSISTSTOSTREAMINIT、catid \_ PersistsToStream、CATID \_ PersistsToStorage、CATID \_ PERSISTSTOMEMORY、catid \_ PersistsToFile、catid \_ PersistsToPropertyBag<br/> | 物件支援類別的對應 IPersist \* 機制。<br/> |



 

下表提供指派給每個類別目錄的確切 Catid：



| 類別                                | CATID                                           |
|-----------------------------------------|-------------------------------------------------|
| CATID \_ RequiresDataPathHost<br/>  | 0de86a50-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToMoniker <br/>    | 0de86a51-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToStorage <br/>    | 0de86a52-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToStreamInit <br/> | 0de86a53-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToStream <br/>     | 0de86a54-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToMemory <br/>     | 0de86a55-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToFile <br/>       | 0de86a56-2baa-11cf-a229-00aa003d7352<br/> |
| CATID \_ PersistsToPropertyBag<br/> | 0de86a57-2baa-11cf-a229-00aa003d7352<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[元件類別](component-categories.md)
</dt> </dl>

 

