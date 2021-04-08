---
title: MIDL 系結控制碼
description: 系結控制碼是代表用戶端與伺服器之間系結的資料物件。
ms.assetid: 178f4838-3deb-43d4-804f-ad6404b377bd
keywords:
- 資料類型 MIDL、系結控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59faea2137cb037cab1e5969e53fff2c146ad31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023308"
---
# <a name="midl-binding-handles"></a>MIDL 系結控制碼

系結控制碼是代表用戶端與伺服器之間系結的資料物件。

MIDL 支援基底類型 [**控制碼 \_ t**](handle-t.md)。 這種類型的控制碼稱為「基本控制碼」。

您可以使用 **\[ handle \]** 屬性來定義您自己的控制碼類型。 以這種方式定義的控制碼稱為「使用者定義」或「自訂」或「泛型」控制碼。

您也可以使用 **\[** [**內容 \_ 控制碼**](context-handle.md)屬性，定義維護狀態資訊的控制碼 **\]** 。 以這種方式定義的控制碼稱為「內容」處理。

如果不需要任何狀態資訊，而且您沒有選擇呼叫 RPC 執行時間程式庫來管理控制碼，您可以要求執行時間程式庫提供自動系結。 這是藉由使用 ACF 關鍵字 **\[** [**auto \_ 控制碼**](auto-handle.md)來完成 **\]** 。

您可以使用 ACF 關鍵字 **\[** [**隱含 \_ 控制碼**](implicit-handle.md)，將全域變數指定為系結控制碼 **\]** 。 **\[ 明確 \_ 控制碼 \]** 關鍵字是用來指出每個遠端函式都有明確指定的控制碼。

如需詳細資訊，請參閱系結 [和控制碼](/windows/desktop/Rpc/binding-and-handles)。

 

 