---
description: 您可以設定其他屬性（例如交易式需求）和及時 (JIT) 啟用，以自動決定或限制同步處理值。
ms.assetid: 16771121-cb10-42b4-babc-59270188495a
title: 同步處理相依性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c139d0d6e78288b25e42bd0a84b29432cebb44ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847216"
---
# <a name="synchronization-dependencies"></a>同步處理相依性

您可以設定其他屬性（例如交易式需求）和及時 (JIT) 啟用，以自動決定或限制同步處理值。 例如，COM + 會針對交易式和 JIT 啟用的元件強制執行同步處理。

這些相依性存在的原因是，JIT 啟動或參與交易的元件必須具有適當的隔離和並行行為。 因此，COM + 需要藉由強制執行同步處理來序列化這些元件的存取權。  (如需這些相依性的詳細資訊，請參閱 [Com + 即時啟用](com--just-in-time-activation.md)。 ) 

下表顯示 COM + 同步處理屬性值的特性。

### <a name="transactional-requirement"></a>交易式需求



| 當交易設定為時 | 同步處理可以設定為                    |
|------------------------------|--------------------------------------------------|
| Disabled<br/>          | 任何事項，視 JIT 啟用而定<br/> |
| 不支援<br/>     | 任何事項，視 JIT 啟用而定<br/> |
| 支援<br/>         | 必要<br/>                              |
| 必要<br/>          | 必要<br/>                              |
| 必須是新交易<br/>      | 必要或需要新的<br/>              |



 

### <a name="jit-activation"></a>JIT 啟用



| 當 JIT 啟用設定為時 | 同步處理可以設定為       |
|-------------------------------|-------------------------------------|
| 已啟用<br/>            | 必要或需要新的<br/> |
| Disabled<br/>           | 什麼<br/>                 |



 

如需交易、JIT 啟動和同步處理屬性如何一起運作的詳細資訊，請參閱設定 [交易](configuring-transactions.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定同步處理屬性](setting-the-synchronization-attribute.md)
</dt> <dt>

[同步處理屬性值](synchronization-attribute-values.md)
</dt> </dl>

 

 




