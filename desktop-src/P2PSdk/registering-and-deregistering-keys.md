---
description: 註冊和取消註冊金鑰
ms.assetid: 90fd8df0-e2a8-4183-a50c-e6f8ea5041cc
title: 註冊和取消註冊金鑰
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009ee41e85027ff8eba3f6869359a9ba304f4242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978266"
---
# <a name="registering-and-deregistering-keys"></a>註冊和取消註冊金鑰

## <a name="registering-keys"></a>註冊金鑰

節點可以隨時在 **drt \_ 主動**、drt 和 **drt \_ 沒有 \_ 網路** 狀態的情況 **下 \_**，向 [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey)註冊金鑰。 只有在本機節點 **轉換為「使用中」 \_** 之後，其他 DRTs 才可辨識已在 drt 中登錄的金鑰，且不會有 **\_ 任何 \_ 網路** 狀態。 **\_**

使用 [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider)時，不能在相同的 DRT 實例內註冊相同的索引鍵。 如果嘗試註冊相同的金鑰，則第二個金鑰的註冊將會失敗。 使用相同的金鑰也應避免不同的 DRT 實例之間使用。 搜尋唯一索引鍵的指定，這些相同的金鑰共用可能會傳回任何一個索引鍵，而不管與索引鍵相關聯的資料。

> [!Note]  
> 如果執行時需要不同的行為，則可以建立安全性提供者來取代 [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) 以容納。

 

## <a name="deregistering-keys"></a>取消註冊金鑰

節點註冊之後，即可隨時取消註冊金鑰。 不過，只有註冊金鑰的應用程式可以將它取消註冊。 應用程式可以使用 [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) 函數，從本機節點取消註冊金鑰。 完成時，此函式會觸發 **DRT \_ 事件 \_ LEAFSET \_ 金鑰 \_ 變更** 事件; 通知應用程式，以及參與 DRT 網狀的其他節點。

在 Drt 發生 **錯誤 \_** 狀態時，所需的 [**DRTCLOSE**](/windows/desktop/api/drt/nf-drt-drtclose) 呼叫會導致 DRT 基礎結構將所有金鑰取消註冊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[搜尋分散式路由表](searching-a-distributed-routing-table.md)
</dt> <dt>

[關於分散式路由表](about-distributed-routing-tables.md)
</dt> <dt>

[分散式路由資料表 API 參考](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



