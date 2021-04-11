---
description: UI 順序資料表或外部可執行檔中的自訂動作可能需要安裝的目前使用者介面層級。
ms.assetid: d1ddadd5-b4ec-4c7c-aee4-b2d688a57eb4
title: 從自訂動作判斷 UI 層級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2586cd03bfda2b22e721c0ae9c3393d4bbc525a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944556"
---
# <a name="determining-ui-level-from-a-custom-action"></a><span data-ttu-id="94fd2-103">從自訂動作判斷 UI 層級</span><span class="sxs-lookup"><span data-stu-id="94fd2-103">Determining UI Level from a Custom Action</span></span>

<span data-ttu-id="94fd2-104">UI 順序資料表或外部可執行檔中的自訂動作可能需要安裝的目前使用者介面層級。</span><span class="sxs-lookup"><span data-stu-id="94fd2-104">A custom action in a UI sequence table or an external executable file may need the current user interface level of the installation.</span></span> <span data-ttu-id="94fd2-105">例如，具有對話方塊的自訂動作應該只會在使用者介面層級為 [完整 UI] 或 [縮小] UI 時顯示對話方塊，如果使用者介面層級為 [基本] UI 或 [無]，則不應顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="94fd2-105">For example, a custom action that has a dialog box should only display the dialog when the user interface level is Full UI or Reduced UI, it should not display the dialog if the user interface level is Basic UI or None.</span></span> <span data-ttu-id="94fd2-106">您應該使用 [**UILevel**](uilevel.md) 屬性來決定目前的使用者介面層級。</span><span class="sxs-lookup"><span data-stu-id="94fd2-106">You should use the [**UILevel**](uilevel.md) property to determine the current user interface level.</span></span> <span data-ttu-id="94fd2-107">您無法從自訂動作呼叫 [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) ，也無法從自訂動作內變更 UI 層級屬性。</span><span class="sxs-lookup"><span data-stu-id="94fd2-107">You cannot call [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) from a custom action and it is not possible to change the UI level property from within a custom action.</span></span>

<span data-ttu-id="94fd2-108">建議自訂動作不要使用 UI 層級做為將錯誤訊息傳送至安裝程式的條件，因為這可能會干擾記錄和外部訊息。</span><span class="sxs-lookup"><span data-stu-id="94fd2-108">It is recommended that custom actions not use the UI level as a condition for sending error messages to the installer because this can interfere with logging and external messages.</span></span>

 

 



