---
description: 自動資源回收
ms.assetid: c889dd3f-82d1-4bc3-ac2c-6f468d5b2c7f
title: 自動資源回收
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec280c0b0ae222cf0c63e136b7643bbd05c1fffa5589ccc4b736dd247a43b1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730668"
---
# <a name="automatic-resource-reclamation"></a>自動資源回收

COM + 會在每次物件的存留期結束時，通知分配器管理員。 然後，分配者管理員會通知每個已註冊的資源配置器的持有者，查看是否有此物件仍保留的任何資源。 如果是的話，就會釋出這些資源，藉由透過資源配置器取得資源的元件來避免資源流失的可能性。

自動回收功能是預設為關閉的選項。 資源配置器可以選擇啟用這個選項，而且在這樣做之後，物件方法絕對不會傳回對物件回傳之任何資源的參考。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 資源配置器概念](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



