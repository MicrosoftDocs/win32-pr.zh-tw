---
description: COM + 應用程式共用允許單一執行緒進程進行調整，類似于執行緒共用允許單一執行緒物件的調整方式。
ms.assetid: 28bd13d9-ff5c-456e-ab98-d2ff3a499f1c
title: COM + 應用程式共用概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9aab46350e3c6084c0d5e8ca61d2f3c90d27e06795f7d08568ee4a7c1e0fc26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096908"
---
# <a name="com-application-pooling-concepts"></a>COM + 應用程式共用概念

COM + 應用程式共用允許單一執行緒進程進行調整，類似于執行緒共用允許單一執行緒物件的調整方式。 應用程式共用也可以藉由提供可處理啟用的其他執行中進程，協助從單一進程的失敗中復原。

> [!Note]  
> 程式庫應用程式具有其主機進程的回收和共用屬性。

 

[**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)介面的所有方法都支援應用程式共用。

使用 [**應用**](applications.md)程式集合中 [**COMAdminCatalogObject**](comadmincatalogobject.md)物件的 ConcurrentApps 屬性，可設定每個應用程式的 com + 應用程式共用。 ConcurrentApps 是一個整數值，這個值會指定應用程式的啟動服務時，應該啟動的同時 Dllhost.exe 進程數目上限。 您可以使用 [元件服務] 系統管理工具或以程式設計方式來設定這個屬性。

如果 ConcurrentApps 屬性設定為1（預設值），則會停用 COM + 應用程式共用服務。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 應用程式共用工作](com--application-pooling-tasks.md)
</dt> <dt>

[COM + 應用程式回收概念](com--application-recycling-concepts.md)
</dt> </dl>

 

 



