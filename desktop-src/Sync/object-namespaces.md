---
description: 物件命名空間可保護命名物件免于未經授權的存取。
ms.assetid: 6a84ec16-fa65-4cdd-861a-eccf5d0eee2b
title: 物件命名空間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6137d53e45f27a8de2c76075bc2a5565a5942bd38bf6fa3cd3891e4561870b8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765485"
---
# <a name="object-namespaces"></a>物件命名空間

*物件命名空間* 可保護命名物件免于未經授權的存取。 建立私用命名空間可讓應用程式和服務建立更安全的環境。

進程可以使用 [**CreatePrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea) 函式來建立私用命名空間。 此函式會要求您指定 *界限* ，以定義如何隔離命名空間中的物件。 呼叫端必須在指定的界限內，才能成功建立作業。 若要指定界限，請使用 [**CreateBoundaryDescriptor**](/windows/desktop/api/WinBase/nf-winbase-createboundarydescriptora) 和 [**AddSIDToBoundaryDescriptor**](/windows/win32/api/namespaceapi/nf-namespaceapi-addsidtoboundarydescriptor) 函數。

[**CreatePrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea)的 *lpAliasPrefix* 參數會當做命名空間的名稱。 每個命名空間都是由其名稱和界限來唯一識別。 系統支援多個具有相同名稱的私用命名空間，只要它們指定不同的界限即可。

假設進程要求建立命名空間 NS1，以定義包含兩個元素的界限：系統管理員 SID 和目前的會話編號。 如果進程是在指定會話的系統管理員帳戶下執行，就會建立命名空間。 另一個進程可以使用 [**OpenPrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-openprivatenamespacea) 函式來存取此命名空間。 如果此處理程式是開啟第一個進程所建立的命名空間，則指定的名稱和界限必須相符。 請注意，處理常式可以開啟現有的命名空間，即使它不在界限內，除非使用 *lpPrivateNamespaceAttributes* 參數來限制存取命名空間。

在這個命名空間中建立的物件具有格式 *首碼* \\ *objectname* 的名稱。 前置詞是由 [**CreatePrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea)的 *lpAliasPrefix* 參數所指定的命名空間名稱。 例如，若要在 NS1 命名空間中建立名為 MyEvent 的事件物件，請呼叫 [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) 函數，並將 *lpName* 參數設定為 ns1 \\ MyEvent。

建立命名空間的進程可以使用 [**ClosePrivateNamespace**](/windows/win32/api/namespaceapi/nf-namespaceapi-closeprivatenamespace) 函式來關閉命名空間的控制碼。 當建立命名空間的進程終止時，控制碼也會關閉。 在命名空間控制碼關閉之後，對 [**OpenPrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-openprivatenamespacea) 的後續呼叫會失敗，但命名空間中的物件上的所有作業都會成功。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[核心物件命名空間](../termserv/kernel-object-namespaces.md)
</dt> </dl>

 

 
