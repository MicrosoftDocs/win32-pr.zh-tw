---
description: 由於有兩個主要原因，系統會使用物件和控制碼來管制系統資源的存取權。
ms.assetid: 122acb9e-2a1b-480b-9207-5cc6bbe6b6d4
title: 關於控制碼和物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eee99e0568a0535462e89bfd5de71e12cfaf4a588a605f190dba41ce0ef2535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117959046"
---
# <a name="about-handles-and-objects"></a>關於控制碼和物件

由於有兩個主要原因，系統會使用物件和控制碼來管制系統資源的存取權。 首先，使用物件可確保只要維持原始物件介面，Microsoft 就能更新系統功能。 當系統的後續版本發行時，您可以使用已更新的物件，幾乎不需要額外的工作。

其次，使用物件可以讓您利用 Windows 的安全性。 每個物件都有自己的存取控制清單 (ACL) ，可指定進程可以在物件上執行的動作。 系統會在每次應用程式建立物件的控制碼時，檢查物件的 ACL。 如需詳細資訊，請參閱[存取控制](/windows/desktop/SecAuthZ/access-control)。

-   [物件管理員](object-manager.md)
-   [物件介面](object-interface.md)
-   [物件命名空間](/windows/desktop/Sync/object-namespaces)
-   [控制碼限制](handle-limitations.md)
-   [處理繼承](handle-inheritance.md)

 

 
