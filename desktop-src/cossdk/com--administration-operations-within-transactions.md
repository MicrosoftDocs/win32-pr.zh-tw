---
description: 交易內的 COM + 管理作業
ms.assetid: 832f2e6d-26ff-416e-a92e-ebaa33d4e7e5
title: 交易內的 COM + 管理作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4182b143de38d838aea7c5aabd2d91bdb84f94480b2bed4c4441e204412ac834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308247"
---
# <a name="com-administration-operations-within-transactions"></a>交易內的 COM + 管理作業

COM + 註冊資料庫 (RegDB) 是可參與 COM + 交易的交易式資源管理員。 這可讓您在交易內執行管理作業，並將所有設定變更認可或中止為不可部分完成的作業，即使是在多部電腦上也一樣。 在某些情況下，執行這項作業可能會很有説明，雖然您應該將隔離和封鎖的行為納入考慮，而且在交易內執行管理工作，也不會對一般管理程式設計模型造成些許變更。

## <a name="benefits-of-doing-administration-operations-within-transactions"></a>在交易內執行管理作業的優點

-   **資料的一致性：** 在交易內執行的系統管理作業會以整體方式認可或中止，雖然有些非交易式 COM + 類別目錄資源可能不是這種情況。  (請參閱下方的非交易式 COM + 類別目錄資源。 ) 
-   **跨多部電腦進行一致的部署—** 如果您要在多部伺服器上部署 COM + 應用程式，可以確保所有伺服器都保留相同的設定。
-   **調整規模和效能—** 當您在交易內執行多項作業時，會一次對 RegDB 執行所有寫入作業。 RegDB 的持續寫入是相當昂貴的作業;如果您要對 RegDB 進行許多寫入，您可以從一次執行全部（而不是每次呼叫 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)）獲得大幅的效能優勢。

## <a name="isolation-behavior-of-regdb"></a>RegDB 的隔離行為

為了確保適當的資料一致性和可序列化交易，RegDB 會在交易中執行管理作業時，強制執行特定的封鎖和隔離行為。

每當在交易內進行工作的元件呼叫任何會導致寫入至 COM + 目錄的方法（例如 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)、 [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication)或 [**InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)）時，就會在 com + 目錄伺服器程式碼上採用寫入器鎖定，此程式碼會封鎖任何其他寫入器進入目前的交易認可或中止為止。 也就是說，只有當寫入器具有正確的交易親和性，而且正在參與目前的交易時，才會進入。

未封鎖讀取器。 但是，讀取器所看到的資料並不會反映在交易內進行的任何過渡期變更，直到該交易實際認可為止。 任何參與該交易的元件都會在讀取資料時看到過渡的資料狀態，但交易以外的所有元件只會在交易完成之後，才會看到這些變更。

## <a name="savechanges-behavior"></a>SaveChanges 行為

為了達成上述的隔離行為，RegDB 可有效提供由交易內的元件所處理的快取。 這會變更 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) 方法的行為。

一般情況下，在沒有交易的情況下，任何暫止的變更都會在您呼叫 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)時寫入至目錄，而 **SaveChanges** 在所有寫入完成之前都不會傳回。 這可保證如果對 **SaveChanges** 的呼叫傳回成功，您可以呼叫 [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) ，它會以最新的資料來啟動應用程式。

不過，在交易內， [**savechanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) 只會影響快取，而不會影響 RegDB 本身，而 **savechanges** 會立即傳回，無論所有變更是否已交易認可至 RegDB。 不保證 [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) 會在 **SaveChanges** 傳回之後使用新的資料。 如果您需要在此內容中呼叫 **StartApplication** ，建議您先等候一段時間再執行這項操作。

## <a name="transaction-time-out-period"></a>交易 Time-Out 期限

如果您在交易內進行許多系統管理作業，它可能會是長時間執行的交易。 在此情況下，交易超時值可能會是問題。 這取決於針對起始交易的元件設定的交易超時值，或是該元件執行所在電腦的全電腦超時設定。 如果您要在交易內執行許多作業，建議您將適當的交易逾時間隔設定為夠長的值，並在完成時還原原始設定（如有必要）。

## <a name="non-transactional-com-catalog-resources"></a>非交易式 COM + 類別目錄資源

登錄、檔案系統和 Windows Installer (MSI) 是非交易式的 com + 類別目錄資源。

> [!Note]  
> 如果有錯誤會中止交易，這些資源的變更可能不會回復。

 

如果從 .msi 檔案安裝現有的 COM + 應用程式時發生錯誤，則應用程式不會出現在 [元件服務] 嵌入式管理單元中，但它可能會出現在 [新增/移除程式] 中，在此情況下，您需要手動移除。

## <a name="recovering-in-the-event-of-system-hangs"></a>在發生系統停止回應時復原

如果在交易內執行管理作業的元件在保存目錄伺服器程式碼的寫入器鎖定時停止回應，則會封鎖其他人對目錄進行任何變更。 如果發生這種情況，您可以藉由關閉並重新啟動系統應用程式，清除目錄上的鎖定。

## <a name="scripting-with-a-transactioncontext-object"></a>使用 TransactionCoNtext 物件編寫腳本

在交易內執行管理作業的簡單方式，就是使用 [**TransactionCoNtext**](transactioncontext.md) 物件來控制交易。 例如，下列 Visual Basic 腳本會示範如何以交易方式加入兩個新的應用程式，讓兩個應用程式或兩個應用程式都不會建立：


```VB
Dim txctx
Dim cat
Dim apps
Dim app1
Dim app2
  
WScript.Echo "Starting"
Set txctx = CreateObject("TxCtx.TransactionContext")
Set cat = txctx.CreateInstance("COMAdmin.COMAdminCatalog")
Set apps = cat.GetCollection("Applications")
Set app1 = apps.Add
app1.Value("Name") = "Test App #1"
apps.SaveChanges
Set app2 = apps.Add
app2.Value("Name") = "Test App #2"
apps.SaveChanges
  
WScript.Echo "Ending"
txctx.Commit

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[處理 COM + 管理錯誤](handling-com--administration-errors.md)
</dt> <dt>

[使用 COM + 系統管理目錄的簡介範例](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[COMAdmin 物件的總覽](overview-of-the-comadmin-objects.md)
</dt> <dt>

[在 COM + 類別目錄上取出集合](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[設定屬性並將變更儲存至 COM + 類別目錄](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



