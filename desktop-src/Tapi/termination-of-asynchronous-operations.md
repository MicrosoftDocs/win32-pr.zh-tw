---
description: 當應用程式使用一或多個未完成的非同步作業來呼叫 lineClose 函式時，TAPI 可能會指示服務提供者終止與呼叫相關聯的非同步作業。
ms.assetid: b26ce074-76dc-4a50-8c17-d3412c336d59
title: 非同步作業終止
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d026754af75743314fbdbf7a2a3c82f9935f9b053f2a7186f095e4f452a0bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772998"
---
# <a name="termination-of-asynchronous-operations"></a>非同步作業終止

當應用程式使用一或多個未完成的非同步作業來呼叫 [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose) 函式時，TAPI 可能會指示服務提供者終止與呼叫相關聯的非同步作業，這取決於應用程式是否為呼叫的唯一擁有者，而且只有呼叫的控制碼。

如果應用程式是呼叫的唯一擁有者，則 TAPI 會根據每個這類呼叫的提供者) ，呼叫 [**TSPI \_ LineDropOnClose**](./tspi-linedroponclose.md) 或 [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) (。 服務提供者應該檢查是否有任何與中斷的呼叫相關聯的暫止非同步作業。 如果有暫止的作業存在，服務提供者應該採取適當的動作，可能會終止正在進行的作業。

如果應用程式只有呼叫的控制碼 (也就是沒有任何其他擁有者或監視器) ，TAPI 會呼叫 [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) 函式。 服務提供者必須將此呼叫視為絕對表示必須放棄暫止的非同步作業。 服務提供者必須確保呼叫的順序完成，而且必須針對所有未完成的非同步作業呼叫 [**非同步 \_ 完成**](/windows/win32/api/tspi/nc-tspi-async_completion) 回呼函數，並指定 LINEERR \_ OPERATIONFAILED 錯誤值。 如果 TAPI 先前稱為 [**TSPI \_ LineDropOnClose**](./tspi-linedroponclose.md) 或 [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) 函式，它會在服務提供者從另一個呼叫傳回之後立即呼叫 **TSPI \_ lineCloseCall** ，而不會等候與 **TSPI \_ lineDrop** 函式相關聯的非同步作業完成。

如果應用程式不是呼叫的唯一擁有者，則 TAPI 不會呼叫 [**TSPI \_ LineDropOnClose**](./tspi-linedroponclose.md) 或 [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop)。 如果應用程式沒有呼叫的唯一控制碼，則 TAPI 不會呼叫 [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) 函式。 如果應用程式不是唯一的擁有者，也不是呼叫之控制碼的唯一私密金鑰擁有人，則 TAPI 不會傳送通知給服務提供者，因此任何擱置中的非同步作業都會保持不變。 這表示這類應用程式無法終止使用 [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose) 函數啟動的非同步作業。 不過，因為每個非同步作業都需要叫用應用程式為呼叫的擁有者，所以應用程式不能終止非同步作業的可能性非常罕見。 如果發生這種情況，則 (的另一個擁有者) 呼叫 (s) 必須負責處置 () 的呼叫。

如果 TAPI 呼叫 [**TSPI \_ LineDropOnClose**](./tspi-linedroponclose.md) 或 [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop)，則服務提供者最後必須 \_ 針對相關聯的呼叫傳送 LINECALLSTATE 閒置訊息 (除非) 先呼叫 [**TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) ，才能讓呼叫上的監視器進行清除。 當最後一個監視器已呼叫 [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall) 函式時，TAPI 會呼叫 **TSPI \_ lineCloseCall** 函式; 任何擱置中的作業都必須完成或終止，並如先前所述呼叫 [**非同步 \_ 完成**](/windows/win32/api/tspi/nc-tspi-async_completion) 。

 

 
