---
description: 每個並存元件都必須有版本。
ms.assetid: 0b78ecf6-fbff-4172-9b0d-09f993666db1
title: 元件版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e555035bf7b43f53d3a68f249005928867f453b78522f70dd45f3b5379c75e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885568"
---
# <a name="assembly-versions"></a>元件版本

每個並存元件都必須有版本。 每個元件版本都與具有四個元件的版本號碼相關聯，並以句點分隔： *主要.*...........。 如果對元件進行變更，使其與現有版本不相容，則必須變更版本號碼的 *主要* 或 *次要* 部分。 只有在 *組建* 或 *修訂* 部分中變更的版本號碼，表示元件與舊版相容。

版本必須在 [資訊清單](manifests.md)的 **assemblyIdentity** 元素中指定。 使用四部分版本格式：好吃. ooooo. ppppp。 以句號分隔的每個部分都可以是0-65535 （含）。

 

 



