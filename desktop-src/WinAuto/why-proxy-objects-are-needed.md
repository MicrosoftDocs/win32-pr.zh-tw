---
title: 為何需要 Proxy 物件
description: 使用可存取的物件時，當用戶端設定同內容攔截函式時，會將執行用戶端攔截函式的 DLL 載入伺服器的位址空間中。
ms.assetid: e8e93271-1da6-42cd-9200-23a3e08b490b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28d672f48e9c41f23599a8a64585062a126dafb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300836"
---
# <a name="why-proxy-objects-are-needed"></a>為何需要 Proxy 物件

使用可存取的物件時，當用戶端設定同內容攔截函 [式](in-context-and-out-of-context-hook-functions.md)時，會將執行用戶端攔截函式的 DLL 載入伺服器的位址空間中。 在此情況下，當用戶端從攔截函式內呼叫 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) 時，傳回的介面指標會直接指向伺服器位址空間中的程式碼。 當用戶端使用這個指標呼叫介面屬性時，元件物件模型 (COM) 程式庫不涉及封送處理或封送處理，而且無法偵測是否終結物件。 因此，伺服器必須偵測到這種情況，並將錯誤碼傳回給用戶端。

 

 




