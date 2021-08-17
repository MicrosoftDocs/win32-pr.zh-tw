---
description: 整個過程中都會顯示啟用內容。
ms.assetid: 6eda00d5-9dac-4267-bf61-b481814201f8
title: 執行緒、非同步程式和視窗訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 529be75a3bc72679f44dfb69196f9487aa4f1de4f3cdbeada4ec89e26f05d646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141701"
---
# <a name="using-threads-asynchronous-procedures-and-window-messages"></a>使用執行緒、非同步程式和視窗訊息

整個過程中都會顯示啟用內容。 不過，啟用內容堆疊是針對每個執行緒，而且相同進程中的兩個執行緒可以有不同的啟用堆疊。 [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread) 會自動將目前的啟用內容放在新執行緒的啟用堆疊的頂端。 這有助於升級現有的程式碼以使用並存元件，因為新執行緒可以立即在目前的啟用內容中執行。

非同步程序呼叫、完成埠回呼，以及其他執行緒上的任何其他回呼都會自動取得來源的啟用內容。 呼叫回呼時，會清除啟用堆疊。 這表示您的應用程式可以使用非同步程序呼叫和回呼，而不需要明確地啟用任何內容，因為內容管理將會由基礎並存基礎結構來完成。 若要讓其他內容在回呼或新執行緒期間變成作用中，您的應用程式可以執行自己的內容管理。 在此情況下，您的程式必須使用正確的啟用內容啟用函式順序和停用功能。

啟用內容是執行緒中立的。 啟用內容只會變更目前線程的堆疊，而您無法線上程之間啟用內容。 執行緒 A 無法強制內容進入執行緒 B。啟用內容 API 的功能也可感知執行緒。

當您使用 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) 或 [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) 將視窗訊息傳送至進程中的另一個視窗程式時，目前的啟用內容會先啟動，然後再將訊息傳遞至目的程式。 目前的啟用內容與訊息一起進行。 這可確保參考 COM 物件、DLL 名稱或其他並存資源的訊息會保留其正確的內容資訊。

 

 
