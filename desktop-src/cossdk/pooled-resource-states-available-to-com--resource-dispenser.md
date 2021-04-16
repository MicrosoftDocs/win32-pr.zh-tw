---
description: 適用于 COM + 資源配置器的共用資源狀態
ms.assetid: 5037f11c-d113-49b0-b26f-0e3bc59ae8b3
title: 適用于 COM + 資源配置器的共用資源狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0bc59dcc2b7e95e060c0d6e96a5880d09d26e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468301"
---
# <a name="pooled-resource-states-available-to-com-resource-dispenser"></a>適用于 COM + 資源配置器的共用資源狀態

在任何一次，資源正在使用中或不在使用中，而且已登錄或未登錄在交易中。 這會產生四個可能的資源狀態，如下所示：

-   **取消登錄清查中的資源。** 未由物件使用且未在交易中登記的資源，正在取消登錄清查。 一般清查中的資源可供指派。

-   **已登記清查中的資源。** 未由物件使用但已在交易中登記的資源正在登錄清查中。 這類資源僅可指派給在相同交易中執行的物件。 當 COM + 通知分配者管理員交易已完成時，資源會從已登記的清查移至取消登錄的清查。

-   **已取消登錄的資源使用。** 如果資源已指派給物件，且該實例未在交易中執行，或資源配置器已將資源識別為非交易式，則會在取消登錄的情況下使用此資源。

-   **已登記使用中的資源。** 如果資源已指派給物件，則實例會在交易中執行，而且資源配置器已成功將資源登記在交易中，此資源就會在已登記的情況下使用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 資源配置器概念](com--resource-dispenser-concepts.md)
</dt> <dt>

[在交易中登記資源](enlisting-a-resource-in-a-transaction.md)
</dt> </dl>

 

 



