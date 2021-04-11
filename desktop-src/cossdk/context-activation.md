---
description: 在 COM + 中，會使用相關聯的內容來建立每個 COM 物件。
ms.assetid: e5602af2-5852-4c34-a792-6742e90b7d41
title: 內容啟用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a652615d6c1288887085c857817e32e3a3b4081c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111033"
---
# <a name="context-activation"></a>內容啟用

在 COM + 中，會使用相關聯的內容來建立每個 COM 物件。 這表示必須建立和初始化新的內容，或使用適當的現有內容。 此程式稱為「 *啟用*」。 在 COM + 中，物件會在自己的內容中啟動，或在其建立者 (已要求啟用物件的物件（例如，藉由呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) ）。

在某些情況下（例如 [物件](com--object-pooling.md)共用），物件會在不需要從頭建立的情況下啟用。 在此情況下，會在內容中啟動正在執行的實例。 在其存留期內，它可能會在不同的內容中重複啟用。

在任一種情況下，基本機制都相同：物件與內容相關聯，而且該內容已正確初始化，以代表物件的執行時間需求。

## <a name="flowing-of-context-properties"></a>內容屬性的流動

當啟始物件以回應另一個物件的建立要求時，COM + 必須協調它們，才能適當地啟用下游物件。 COM + 必須將呼叫端的內容與所呼叫元件的設定進行比較，然後決定要在何處啟用下游元件，以及如何將其內容屬性初始化。

為了探索元件的設定，COM + 會在 COM + 類別註冊資料庫中尋找它，該資料庫已針對極快速的執行時間查閱進行優化。  (這取決於您在將元件安裝至 COM + 應用程式時，如何設定元件。 ) 元件的設定會根據呼叫端的內容屬性的狀態進行檢查。

在某些情況下，設定會與呼叫端的內容一致，而且元件可以在呼叫端的內容中啟用。 只有在呼叫端的內容符合新物件的所有執行時間需求時，才會發生這種情況。

當下游元件無法在呼叫端的內容中啟動時，它會在適當的單元中于自己的內容中啟用。 發生這種情況時，某些內容屬性可能會從呼叫端流向被呼叫端。 例如，如果呼叫端與交易相關聯，而且被呼叫端支援交易，則新的物件會取得自己的內容 (在交易中進行投票，它必須有自己的一致旗標) 並繼承位於相同交易和同步處理網域) 中的呼叫端交易識別碼和活動識別碼 (。

## <a name="ignored-context-properties"></a>略過的內容屬性

視元件的設定方式而定，某些內容屬性在判斷是否會在建立者的內容或本身的內容中啟用時，不會扮演任何角色。 例如，停用的交易和同步處理停用的設定（指出交易或同步處理網域的存在）在元件啟用時，不會扮演任何角色。 當內容流動時，會以根本上忽略這些屬性。 或者，如果元件只使用進程層級的存取檢查，則會忽略其資訊安全內容屬性，元件的安全性設定在啟用時永遠不會扮演角色。

## <a name="forcing-activation-in-the-callers-context"></a>在呼叫端的內容中強制啟用

在某些情況下，您可能只想在其呼叫端的內容中啟始物件，也就是永遠不會在其本身的內容中啟用。 例如，您可能想要控制物件在內容界限上呼叫時的行為。

您可以使用 [元件服務] 系統管理工具，在 [元件 **屬性**]**頁面的 [** 啟動] 索引標籤上選取 [**必須在呼叫者內容中啟用**]，以確保無法在其本身的內容中啟始物件。  (請參閱 [在呼叫端的內容中強制啟用](enforcing-activation-in-the-caller-s-context.md) ，以取得逐步指示 ) 。當您選取此選項時，如果無法在呼叫端的內容中啟始物件，則 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 會失敗， \_ 並 \_ 傳回 \_ \_ 建立 \_ 外部 \_ 用戶端 \_ 內容的共同 E 嘗試。

## <a name="default-context"></a>預設內容

預設內容是為了支援未設定的元件，也就是 com 元件未安裝在 com + 應用程式中，而且未在 COM + 類別註冊資料庫中註冊。 如果未配置的元件具有相容的執行緒模型，則會在呼叫端的內容中啟用它們。 否則，它們會在適當的單元中的預設內容中啟用。 每個單元都有預設的內容，以支援不使用 COM + 服務的 COM 物件。

## <a name="hooking-activation"></a>啟用攔截

藉由執行 [**IObjectControl：： Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) 和 [**IObjectControl：:D eactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate)，您可以將啟用和停用連結在一起，以在新的內容中執行特殊初始化。 當物件設定為使用 JIT 啟用或物件共用時，COM + 會在物件生命週期的特定點呼叫這些方法。 如需詳細資訊，請參閱 [Com + 即時啟用](com--just-in-time-activation.md) 和 [com + 物件](com--object-pooling.md) 共用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[攔截跨內容呼叫](interception-of-cross-context-calls.md)
</dt> </dl>

 

 
