---
description: CMSPArray 範本會執行隨需成長的智慧陣列。
ms.assetid: 9b30885c-01a4-4aea-a1c3-5d7966e4697f
title: CMSPArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a6c14d4bdc0b57a295efa5bcc2adfd79d23d31d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944345"
---
# <a name="cmsparray"></a>CMSPArray

CMSPArray 範本會執行隨需成長的智慧陣列。 它是設計來保存具有單一資料型別的小型陣列。 它沒有重要的區段。 其唯一的相依性為 **realloc** 和 **memmove**。 它是在內部用來保留物件指標的清單。 它類似于 ATL 的 **CSimpleArray** 執行，但對於初始配置更有效率。

此範本定義于 MSPutils 中。

 

 



