---
description: 啟用元件的 JIT 啟用
ms.assetid: ccf7c98b-8b1a-431d-b417-83f79734f691
title: 啟用元件的 JIT 啟用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9beac51cd4f97a451b372d8eeee8ef419ead3140a672ca85dcdc3740d8c52de4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637698"
---
# <a name="enabling-jit-activation-for-a-component"></a>啟用元件的 JIT 啟用

您應該將元件設定為只在正確撰寫時才啟用 JIT，以支援 COM + 即時 (JIT) 啟用服務。 如果在方法呼叫之間停用元件，則會遺失任何相關聯的狀態。 由於 JIT 啟用的預設行為，不太可能發生這種情況，但在變更其設定以及將呼叫元件的用戶端期望之前，您應該先留意元件的需求。

> [!Note]  
> 如果元件已設定為需要交易，則會自動啟用 COM + JIT 啟用服務。 在此情況下，您不能停用它。 如需詳細資訊，請參閱設定 [交易](configuring-transactions.md)。

 

當您啟用元件的 JIT 啟用時，其同步處理屬性會設定為該元件的 [必要]。 在此情況下，您無法變更同步處理設定。 如需詳細資訊，請參閱 [同步](synchronization-dependencies.md)處理相依性。

**若要啟用 JIT 啟用**

1.  在 [元件服務] 系統管理工具的詳細資料窗格中，以滑鼠 **按右鍵您** 要設定的元件，然後按一下 [內容]。

2.  在 [元件屬性] 對話方塊中，按一下 [ **啟用** ] 索引標籤。

3.  若要啟用元件的 JIT 啟用，請選取 [ **啟用即時啟用** ] 核取方塊。

4.  按一下 [確定]。

當您啟用元件的 JIT 啟用時，可以選擇針對該元件所公開的任何方法啟用自動完成功能。 如需詳細資訊，請參閱為 [方法啟用自動完成](enabling-auto-done-for-a-method.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[為方法啟用自動完成](enabling-auto-done-for-a-method.md)
</dt> <dt>

[設定完成位](setting-the-done-bit.md)
</dt> </dl>

 

 



