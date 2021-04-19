---
description: 及時 (JIT) 啟動服務可讓 COM + 在用戶端仍保留該物件的作用中參考時，停用物件。
ms.assetid: dbc7b257-8506-42c8-8a78-3474c6d4f4b6
title: COM + 即時啟用概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c942bfeb342ea305083e0c7d7ebdea2fe96bf24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988057"
---
# <a name="com-just-in-time-activation-concepts"></a>COM + 即時啟用概念

及時 (JIT) 啟動服務可讓 COM + 在用戶端仍保留該物件的作用中參考時，停用物件。 下次用戶端在物件上呼叫方法時（用戶端認為仍在使用中），COM + JIT 啟動服務會將物件透明地重新開機至用戶端（及時）。

使用 COM + JIT 啟用的主要優點是，您可以讓用戶端在需要的情況下保留物件的參考，而不一定會佔用重要的伺服器資源（例如記憶體）。 其他重要的優點包括下列各項：

-   使用 COM + JIT 啟用服務可大幅簡化用戶端的程式設計模型，因為用戶端不需要思考它如何使用昂貴的伺服器物件和伺服器資源。 如果沒有 JIT 啟用，當用戶端經常需要呼叫和釋放物件時，可能會產生重大的負面影響。
    > [!Note]  
    > 您可以使用 [Com + 物件](com--object-pooling.md) 共用服務，進一步改善此效能優勢。 藉由共用 JIT 啟動的物件，您可以大幅加速用戶端的物件重新開機，同時重複使用它們可能保留的資源，讓您更精確地控制伺服器上的指定物件所使用的記憶體數量。 如需詳細資訊，請參閱 [物件共用和 COM + JIT 啟用](object-pooling-and-com--jit-activation.md)。

     

-   使用分散式應用程式時，需要昂貴的網路來回行程才能建立每個物件，而用戶端從伺服器越多，啟動和封送處理伺服器物件、開啟通道，以及設定 proxy 和存根的成本就愈大。 藉由使用 COM + JIT 啟用服務，您可以將建立物件的頻率降到最低，以大幅提升應用程式的效能。
-   當您使用 COM + JIT 啟用來啟動這些物件，而這些物件是用戶端保存長時間存留的參考，但不一定都在使用時，伺服器記憶體不一定會讓這些物件保持運作。 這可能會大幅增加應用程式的擴充性。 用戶端看到的唯一效能衝擊，就是 COM + 重新啟始物件所花費的時間，通常比為物件配置記憶體所花的時間還要多，而且明顯小於網路往返以進行遠端物件建立。

## <a name="enabling-com-jit-activation"></a>啟用 COM + JIT 啟用

您可以使用 [元件服務] 系統管理工具或系統管理功能，為元件啟用 COM + JIT 啟用服務。 如需如何進行此作業的詳細資訊，請參閱 [啟用元件的 JIT](enabling-jit-activation-for-a-component.md)啟用。

COM + JIT 啟用可以與其他 COM + 服務互動，如下所示：

-   當您的元件需要交易時，系統會自動為它啟用 JIT 啟用。 如需更詳細的資訊，請參閱 [交易和 COM + JIT 啟用](transactions-and-com--jit-activation.md)。
-   當您的元件啟用 JIT 啟用時，同步處理會自動設為 [必要]。 這表示，如果兩個用戶端同時呼叫 JIT 啟動的元件，而其中一個的方法呼叫傳回時，會造成物件被停用，而另一個則不會留下擱置。

## <a name="how-deactivation-is-triggered"></a>觸發停用的方式

COM + 會根據物件內容上的 doneness 位狀態來停用物件。 您的物件可以使用此位來表示在指定的方法呼叫期間，是否已完成（也就是已準備好停用）。 如需詳細資訊，請參閱 [設定完成位](setting-the-done-bit.md)。

## <a name="using-the-auto-done-property"></a>使用自動完成屬性

您可以使用 [元件服務] 系統管理工具來設定方法，使物件在方法傳回時自動停用。  (如需有關如何設定此屬性的指示，請參閱為 [方法啟用自動完成](enabling-auto-done-for-a-method.md) ) 。您可以選取此選項，在交易中排除重複的方法呼叫來投票。 因為一致性位的預設設定為 True，所以如果您也將完成的位變更為 True，而且不採取任何動作來變更這些設定，則在方法傳回之後，會自動呼叫 [**IObjectCoNtext：： SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) 。

不過，這種行為有一點要注意： COM + 將檢查方法傳回的 HRESULT。 如果該 HRESULT 指出失敗，一致性位會設為 False，而結果會與您呼叫 [**IObjectCoNtext：： SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)相同。

總而言之，如果您針對方法選取 [自動完成]，而不採取任何動作來設定任何位，而且如果系統傳回 HRESULT (hr) ，則適用下列情況：

-   如果成功 (hr) ，就如同您呼叫 [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)一樣。
-   如果 (hr) 失敗，就如同您呼叫 [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)一樣。

## <a name="using-iobjectcontrol-to-manage-object-activation-and-deactivation"></a>使用 IObjectControl 管理物件啟用和停用

您可以執行 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) 介面，讓 com + 執行時間自動管理物件的停用和重新啟用。 當物件執行這個介面時，COM + 會在停用物件時呼叫 [**IObjectControl：:D eactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) ，並在重新啟始物件時呼叫 [**IObjectControl：： Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) 。 這些方法會在物件啟用時啟用自動內容初始化，並在停用時清除狀態。

如果您要共用使用 COM + JIT 啟用的物件，強烈建議您執行 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol)。 如需詳細資訊，請參閱 [物件共用和 COM + JIT 啟用](object-pooling-and-com--jit-activation.md)。

## <a name="statelessness-and-jit-activation"></a>無狀態和 JIT 啟用

交易對象一定是無狀態的，因為您無法跨交易界限共用狀態。 因此，只有當您的物件沒有在停用時遺失的狀態時，才會使用 JIT 啟用;否則，您會違反交易的隔離。 由於交易對象的自然使用模式，它們會執行一些工作單位，並在交易認可或中止時釋出物件，也就是 JIT 啟用和自動交易密切相關。 將物件設定為需要交易可自動啟用 COM + JIT 啟用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 即時啟用工作](com--just-in-time-activation-tasks.md)
</dt> <dt>

[物件共用和 COM + JIT 啟用](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[交易和 COM + JIT 啟用](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



