---
description: 為了達到最佳效能，COM + JIT 啟用基本上會在貪婪用戶端和貪婪伺服器之間遭遇折衷。 用戶端會取得物件參考，而伺服器可以更緊密地管理記憶體使用量。
ms.assetid: 125d39f5-af38-4a87-a649-2f77a3e77c27
title: 物件共用和 COM + JIT 啟用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8042d838aaaae62eace6f61a8fe1aa820e17d079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386006"
---
# <a name="object-pooling-and-com-jit-activation"></a>物件共用和 COM + JIT 啟用

為了達到最佳效能，COM + JIT 啟用基本上會在貪婪用戶端和貪婪伺服器之間遭遇折衷。 用戶端會取得物件參考，而伺服器可以更緊密地管理記憶體使用量。

您可以使用 [Com + 物件](com--object-pooling.md)共用來進一步改善。 藉由共用 JIT 啟動的物件，您可以專用特定數量的記憶體，以在記憶體中保留特定數量的物件，以準備立即重複使用。 當物件的建立成本很高時，這會是最有意義的，如同在保存多個資源的情況下。

以這種方式共用 JIT 啟用的物件，您可以達到下列優點：

-   大幅加速的物件重新開機時間。
-   重複使用物件所持有的任何昂貴資源。
-   更精確地控制集區物件的記憶體和資源使用。
-   保留系統管理彈性，讓您的應用程式可以調整以使用可用的資源，並適應變更的效能需求。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 即時啟用概念](com--just-in-time-activation-concepts.md)
</dt> <dt>

[COM + 物件共用](com--object-pooling.md)
</dt> <dt>

[啟用元件的 JIT 啟用](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[交易和 COM + JIT 啟用](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



