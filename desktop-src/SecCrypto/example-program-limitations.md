---
description: 程式限制範例
ms.assetid: 2f428872-10ba-4059-ab42-f69dce940bed
title: 程式限制範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1fde65fa1870ac3ed118bd7c9f95c6add5192f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984997"
---
# <a name="example-program-limitations"></a>程式限制範例

在這些範例程式中，不一定會遵循良好的程式設計實務準則，以提供更簡潔、更容易閱讀的程式碼。 尤其是：

-   只會顯示有限的錯誤回應。 工作程式應一律檢查傳回的錯誤碼，並在發生錯誤時執行適當的動作。
-   只會執行有限的記憶體和資源管理。 在工作程式中，所有的金鑰和 [*雜湊*](../secgloss/h-gly.md) 都應該終結、所有配置的記憶體都應該釋出、所有的檔案都應該關閉，而且所有的控制碼都應該釋放出來。 這些範例程式只提供使用執行這些工作的函式的有限示範。 這些範例程式在程式終止時，不會執行任何記憶體或資源管理工作，因為發生錯誤。

 

 
