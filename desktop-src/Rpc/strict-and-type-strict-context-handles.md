---
title: Strict 和 Type Strict 內容控制碼
description: 使用 \_ \_ 所有內容控制碼的 strict 內容控制碼屬性。
ms.assetid: 2483aa76-0814-4f63-9c38-0aa050d73772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a45b4e7914034e315f2275e1d928293332012fc4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463433"
---
# <a name="strict-and-type-strict-context-handles"></a>Strict 和 Type Strict 內容控制碼

使用所有內容控制碼的 [**strict \_ 內容 \_ 控制碼**](/windows/desktop/Midl/strict-context-handle) 屬性。 根據預設，內容控制碼不會與介面相關聯，這表示可以在某個介面上建立內容控制碼，然後傳遞至另一個介面。 這是一項簡單的攻擊，而許多 RPC 伺服器無法避免。

如果兩個介面並存于同一個進程中，攻擊者可以開啟某個介面上的內容控制碼，並將其傳遞給另一個介面，而這可能會導致無法預期的資料。 許多開發人員認為其軟體是程式中唯一的介面，但通常不是這種情況，因為系統和許多協力廠商元件會在內部使用 RPC，而這些介面可以建立內容控制碼。 使用 [**strict \_ 內容 \_ 控制碼**](/windows/desktop/Midl/strict-context-handle) 屬性時，RPC 執行時間可確保在某個介面上建立的內容只能做為引數傳遞給該介面的方法。

在針對 Windows Vista 開發應用程式的情況下，可以使用 [**類型 \_ strict \_ 內容 \_ 控制碼**](/windows/desktop/Midl/type-strict-context-handle) ，並建議使用。 內容控制碼預設不會與特定類型相關聯。 在相同的進程中使用多種類型的內容控制碼時，惡意用戶端可能會傳遞內容控制碼來取代另一個，以產生不想要的結果。 使用 **類型 \_ strict \_ 內容 \_ 控制碼** 可讓應用程式強制執行內容控制碼類型一致性，並防止任何不相符的內容控制碼類型使用方式。

 

 