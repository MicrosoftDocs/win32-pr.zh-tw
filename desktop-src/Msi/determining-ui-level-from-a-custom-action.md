---
description: UI 順序資料表或外部可執行檔中的自訂動作可能需要安裝的目前使用者介面層級。
ms.assetid: d1ddadd5-b4ec-4c7c-aee4-b2d688a57eb4
title: 從自訂動作判斷 UI 層級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af88753b5ea44927ac58b13bcb4742e7992e50e1499aa04964b60b632d68ec53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947565"
---
# <a name="determining-ui-level-from-a-custom-action"></a>從自訂動作判斷 UI 層級

UI 順序資料表或外部可執行檔中的自訂動作可能需要安裝的目前使用者介面層級。 例如，具有對話方塊的自訂動作應該只會在使用者介面層級為 [完整 UI] 或 [縮小] UI 時顯示對話方塊，如果使用者介面層級為 [基本] UI 或 [無]，則不應顯示對話方塊。 您應該使用 [**UILevel**](uilevel.md) 屬性來決定目前的使用者介面層級。 您無法從自訂動作呼叫 [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) ，也無法從自訂動作內變更 UI 層級屬性。

建議自訂動作不要使用 UI 層級做為將錯誤訊息傳送至安裝程式的條件，因為這可能會干擾記錄和外部訊息。

 

 



