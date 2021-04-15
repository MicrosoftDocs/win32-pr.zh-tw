---
title: 完整且部分系結的控制碼
description: 當您使用動態端點時，執行時間程式庫會在需要時取得端點資訊。
ms.assetid: 13f2f783-2c10-4122-ba4d-a97b9c0378c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc1f434ec53ebcfd992b0090ed9066dce2ec627
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462248"
---
# <a name="fully-and-partially-bound-handles"></a>完整且部分系結的控制碼

當您使用動態端點時，執行時間程式庫會在需要時取得端點資訊。 執行時間程式庫會區分完全系結的 *控制碼* (其中包含端點資訊) 和部分系結的 *控制碼* ， (不包含) 端點資訊的控制碼。

用戶端執行時間程式庫必須先將部分系結的控制碼轉換成完全系結的控制碼，用戶端才能系結至伺服器。 用戶端執行時間程式庫會嘗試取得端點資訊，以轉換用戶端應用程式的部分系結控制碼，如下所示：

-   從用戶端的介面規格
-   從伺服器上執行的端點對應服務

如果用戶端在介面規格中無法使用端點資訊，而伺服器的端點對應程式沒有伺服器端點的相關資訊時，嘗試使用部分系結的控制碼，則用戶端將不會有足夠的資訊來進行遠端程序呼叫，而且呼叫會失敗。 若要避免這種情況，當分散式應用程式使用部分系結的控制碼時，您必須在端點對應程式中註冊端點。 如需端點對應程式的詳細資訊，請參閱 [指定動態端點](specifying-endpoints.md)。

當遠端程序呼叫失敗時，用戶端應用程式可以呼叫 [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) 來移除過期的端點資訊。 當用戶端嘗試呼叫遠端程式時，用戶端執行時間程式庫會再次嘗試將完全系結控制碼轉換成部分系結的控制碼。 當使用不同的動態端點停止並重新啟動伺服器時，這會很有用。

 

 




