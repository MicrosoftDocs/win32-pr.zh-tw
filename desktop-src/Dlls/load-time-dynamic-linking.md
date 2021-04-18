---
description: 當系統啟動使用載入時間動態連結的程式時，它會使用連結器放置在檔案中的資訊，來找出進程所使用的 Dll 名稱。
ms.assetid: 29a17116-bb08-4fdd-857c-b7a7f8d2278c
title: Load-Time 動態連結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28435fd6df4a3fc5311dc46dbb761b48c139a6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514004"
---
# <a name="load-time-dynamic-linking"></a>Load-Time 動態連結

當系統啟動使用載入時間動態連結的程式時，它會使用連結器放置在檔案中的資訊，來找出進程所使用的 Dll 名稱。 然後系統會搜尋 Dll。 如需詳細資訊，請參閱 [動態連結程式庫搜尋順序](dynamic-link-library-search-order.md)。

如果系統找不到必要的 DLL，它就會終止處理常式，並顯示向使用者報告錯誤的對話方塊。 否則，系統會將 DLL 對應到進程的虛擬位址空間，並遞增 DLL 參考計數。

系統會呼叫進入點函數。 此函式會接收程式碼，指出進程正在載入 DLL。 如果進入點函數未傳回 TRUE，則系統會終止進程並回報錯誤。 如需進入點函數的詳細資訊，請參閱 [動態連結程式庫 Entry-Point](dynamic-link-library-entry-point-function.md)函式。

最後，系統會使用匯入的 DLL 函式的起始位址來修改函式位址表。

DLL 會在初始化期間對應到進程的虛擬位址空間，而且只有在需要時才會載入實體記憶體。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Load-Time 動態連結](using-load-time-dynamic-linking.md)
</dt> </dl>

 

 



