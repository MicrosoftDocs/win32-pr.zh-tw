---
description: 支援大型頁面可讓伺服器應用程式建立大型頁面的記憶體區域，在64位 Windows 上特別有用。
ms.assetid: 060115af-38d1-499c-b30c-47cd0cf42d20
title: Large-Page 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad61873c80d2d3fe8de6a915f5eb93f527049a437860deabedbe232cdf9cb885
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869678"
---
# <a name="large-page-support"></a>Large-Page 支援

支援大型頁面可讓伺服器應用程式建立大型頁面的記憶體區域，在64位 Windows 上特別有用。 每個大型頁面轉譯都會使用 CPU 內的單一轉譯緩衝區。 這個緩衝區的大小通常會大於原生頁面大小的三個數量級順序;這會提高轉譯緩衝區的效率，進而提高經常存取之記憶體的效能。

下列程式說明如何使用大型頁面支援。

**使用大型頁面支援**

1.  藉由呼叫 [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges)函數來取得 **SeLockMemoryPrivilege** 許可權。 如需詳細資訊，請參閱將 [許可權指派給帳戶](../secbp/assigning-privileges-to-an-account.md) 和 [變更權杖中的許可權](../secbp/changing-privileges-in-a-token.md)。
2.  藉由呼叫 [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) 函式來取得最小的大型頁面大小。
3.  呼叫 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)函數時，請包含 **記憶體 \_ 大型 \_ 頁面** 的值。 大小和對齊方式必須是最大頁面的倍數。

撰寫使用大型頁面記憶體的應用程式時，請記住下列考慮：

-   因為每個大型頁面的實體空間必須是連續的，但記憶體可能已被分割，所以在系統長時間執行之後，可能很難取得大型頁面的記憶體區域。 在這些情況下配置大型頁面可能會大幅影響系統效能。 因此，應用程式應該避免進行重複的大型頁面配置，並且在啟動時，一次配置所有的大型頁面。
-   記憶體一律是讀取/寫入，且 nonpageable (永遠常駐于實體記憶體) 。
-   記憶體是進程私用位元組的一部分，而不是工作集的一部分，因為工作集的定義只包含可分頁的記憶體。
-   大型分頁配置不受限於作業限制。
-   您必須將大型頁面的記憶體保留和認可為單一作業。 換句話說，大型頁面無法用來認可先前保留的記憶體範圍。
-   在 Intel Itanium 型系統上的 WOW64 不支援使用此功能的32位應用程式。 應用程式應該重新編譯為原生64位應用程式。

 

 
