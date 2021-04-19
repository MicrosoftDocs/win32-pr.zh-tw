---
description: 您可以針對啟用 COM + JIT 啟用的元件所公開的任何方法，啟用自動完成功能。 如果已停用 JIT 啟用，則無法使用自動完成。
ms.assetid: d699b85c-441f-4ea6-8d03-d1fa9a8a357f
title: 為方法啟用自動完成
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130e5f8b2fde6c6755ef4174892aa35be8a24cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986266"
---
# <a name="enabling-auto-done-for-a-method"></a>為方法啟用自動完成

您可以針對啟用 COM + JIT 啟用的元件所公開的任何方法，啟用自動完成功能。 如果已停用 JIT 啟用，則無法使用自動完成。

您應該只針對刻意撰寫的方法啟用自動完成，以利用它，因為這項功能可能會變更方法的預期行為。

當您啟用自動完成時，會變更該方法的 JIT 啟用和自動交易的預設行為。 您可能會想要使用這項功能，因為它可以移除明確宣告一致性和 doneness 的必要項。 這可以改為在啟用自動完成時直接傳回 HRESULT 來完成。 基本上，當您啟用自動完成時，會指示 COM + 執行下列作業：

-   在每次呼叫這個方法時，會在執行物件的內容上，將完成的位設定為 True。
-   檢查方法傳回的 HRESULT;如果它指出成功或失敗，請適當地設定一致性位。 這可能會導致自動呼叫 [**IObjectCoNtext：： SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) 或 [**IObjectCoNtext：： SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)，這取決於方法在內部的運作方式。

**若要為方法啟用自動完成**

1.  在 [元件服務] 系統管理工具的詳細資料窗格中，以滑鼠 **按右鍵您** 要設定的方法，然後按一下 [內容]。

2.  在 [方法屬性] 對話方塊中，按一下 [ **一般** ] 索引標籤。

3.  若要啟用自動完成，請選取 [ **當此方法傳回時自動停用此物件** ] 核取方塊。 如果核取方塊無法使用，您必須先啟用元件的 JIT 啟用。 如需詳細指示，請參閱[啟用元件的 JIT 啟用](enabling-jit-activation-for-a-component.md) (。 ) 

4.  按一下 [確定]  。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 即時啟用概念](com--just-in-time-activation-concepts.md)
</dt> <dt>

[啟用元件的 JIT 啟用](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[設定完成位](setting-the-done-bit.md)
</dt> </dl>

 

 



