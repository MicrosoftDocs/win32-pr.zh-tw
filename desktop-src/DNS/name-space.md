---
title: 命名空間
description: 命名空間是指必須明確解析所有物件名稱的內容。
ms.assetid: 7731f6b5-1efa-43bc-bd31-9b5183ec90dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce9119b49cde888cb51f65e6e6b677fb364d640e1b78fe48c739b7c1206936d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692198"
---
# <a name="namespace"></a>命名空間

命名空間是指必須明確解析所有物件名稱的內容。 例如，網際網路是單一的 DNS 命名空間，其中具有 DNS 名稱的所有網路裝置都可以解析為特定位址 (例如， `www.microsoft.com` 解析為 207.46.131.13) 。

## <a name="flat-namespace"></a>一般命名空間

命名空間可以是平坦的或階層式。 一般命名空間無法適當地進行調整，因為在所有可用的名稱都能用完之前，它只會變得很大。 一旦在命名空間中使用一次以上的名稱，命名空間就會違反明確可解析的需求。

## <a name="hierarchical-namespace"></a>階層式命名空間

階層命名空間會分割成不同的區域，可視為子命名空間。 每個區域在整體命名空間內都是它自己的子命名空間。 因此，每個物件在其子命名空間內都必須有唯一的名稱，才能在命名空間階層內具有可明確解析的名稱。 然後，階層命名空間可以調整為極大型的網路 &mdash; ，因為當您將更多物件新增至整體命名空間時，您只需要在它們所屬的子命名空間中尋找其唯一的名稱。

所有 DNS 命名空間都是階層式的。 DNS 階層命名空間中的子命名空間稱為 *網域*。 網域內的電腦唯一名稱稱為「 *相對辨別名稱*」。 具有相同相對辨別名稱的電腦可以存在於命名空間階層的不同子命名空間 (網域) ，因為它們可以完整地解析成整個 DNS 階層內的唯一物件，並使用完整功能變數名稱)  (FQDN。 例如，您可以在 *widgets.microsoft.com* 網域中有一個名為 *server1* 的伺服器 (*widgets.microsoft.com* 命名空間) ，而且在 *gadgets.widgets.microsoft.com* 命名空間中可以有 *server1* 。 因為它們位於階層式命名空間的不同子命名空間中，所以可以解析為不同的 Fqdn &mdash; *server1.widgets.microsoft.com* 和 *server1.gadgets.widgets.microsoft.com*。
