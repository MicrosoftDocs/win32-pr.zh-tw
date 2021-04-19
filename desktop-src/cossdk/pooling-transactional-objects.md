---
description: 要共用的交易元件具有特殊需求。
ms.assetid: 32e2f830-c30a-4dbc-8e69-dd2038851998
title: 共用交易對象
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 006ba32ad2ac550be4fa4418dde322ded26c64c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972971"
---
# <a name="pooling-transactional-objects"></a>共用交易對象

要共用的交易元件具有特殊需求。

## <a name="manually-enlisting-resources"></a>手動登記資源

參與交易的共用物件必須手動登錄 managed 資源。 如果物件在用戶端之間保有受控資源，當物件在指定的內容中啟動時，資源管理員將無法自動在交易中登記。

物件本身必須處理偵測交易的邏輯，關閉 resource manager 的自動登記，並手動登錄其保留的任何資源。 執行此操作的步驟是您所使用的資源管理員專用的步驟。 如果您需要手動登記，請參閱資源管理員的說明文件。

如下所述，當交易在使用中時，物件可以與交易親和性共用，如果是由與該交易相關聯的用戶端呼叫，則可以使用交易親和性來啟用。 在登記資源之前，您應該先檢查交易親和性。 如果物件是取自該交易專屬的集區，它已經在該交易中完成工作並登記其資源。

## <a name="turning-off-automatic-enlistment"></a>關閉自動登記

在取得資源之後，應關閉自動登記，通常是在物件的函式中。 也就是說，您會停用自動登記，然後連接。

停用自動登記有時可能是微妙的程式，特別是在分層資料存取提供者的情況下。 自動登記有時會與連接共用（如同 ODBC）結合，有時也不會與 OLE DB 一樣。 您可能需要確定已在數個層級的提供者上關閉自動登記。

## <a name="implementing-iobjectcontrol"></a>執行 IObjectControl

參與交易的共用物件必須監視其所持有之資源的目前狀態。 如果物件偵測到它處於無法重複使用的狀態（例如，如果連接不正確），則 [**IObjectControl：： CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)會傳回 False。 這將會影響捨棄物件實例，並毀滅交易目前的交易。

## <a name="transaction-specific-pools"></a>Transaction-Specific 集區

物件的集區通常是同質的，且目前未使用的任何集區物件都適合傳回任何用戶端。 這項規則唯一的例外狀況是交易對象，其物件共用已優化。 當要求物件的用戶端有相關聯的交易時，COM + 會掃描集區中是否有已與該交易相關聯的可用物件。 如果找到具有交易親和性的物件，則會傳回給用戶端;否則，會傳回來自一般集區的物件。

如此一來，就會保留特殊的 subpools，包含具有特定交易親和性的物件。 當交易認可或中止時，這些物件會傳回至沒有交易親和性的一般集區，可供任何用戶端使用。

基於這個理由，當您的元件以手動方式在交易中登記其受控資源時，應該先查看是否已登錄。 若是如此，就不需要登記。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 物件的函式字串](com--object-constructor-strings.md)
</dt> <dt>

[控制物件存留期和狀態](controlling-object-lifetime-and-state.md)
</dt> <dt>

[物件共用的運作方式](how-object-pooling-works.md)
</dt> <dt>

[使用物件共用改善效能](improving-performance-with-object-pooling.md)
</dt> <dt>

[共用物件的需求](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



