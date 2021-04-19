---
description: 當使用密碼編譯服務提供者 Csp 時，請記住下列慣例。
ms.assetid: 70053b89-4d39-4a86-985a-0e8f05fbc9c0
title: 使用 Csp：一般進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f067ef0e3cd837b1b347daac3e3da21543047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992009"
---
# <a name="using-csps-general-processes"></a>使用 Csp：一般進程

當使用 [*密碼編譯服務提供者*](../secgloss/c-gly.md) csp 時，請記住下列慣例。

## <a name="private-key-caching"></a>私密金鑰快取

CSP 可以快取部分 [*私密金鑰*](../secgloss/p-gly.md)。 您可以在全域上控制這個私密金鑰快取，但不能在應用程式特定的基礎上進行控制。 您可以藉由修改特定的登錄設定來進行快取變更。 如需詳細資訊，請參閱私密金鑰快取 [**常數**](private-key-caching-constants.md)。

## <a name="example-code-conventions"></a>範例程式碼慣例

為了提供更簡潔、更容易閱讀的程式碼，範例中不一定會有良好程式設計實務的部分原則。 尤其是：

-   只會顯示有限的錯誤回應。 妥善撰寫的完整程式會檢查傳回的錯誤碼，並在發生錯誤時執行適當的動作。
-   只會執行有限的記憶體和資源管理。 撰寫完善的程式會摧毀所有的金鑰和 [*雜湊*](../secgloss/h-gly.md)、釋放所有配置的記憶體、關閉所有檔案，以及釋放所有控制碼。 這些範例僅提供使用執行這些工作的函式的有限示範。 這些範例在程式終止時，不會執行任何記憶體或資源管理工作，因為發生錯誤。

下列主題提供有關程式範例和範例程式碼的一般資訊。

-   [正在抓取未知長度的資料](retrieving-data-of-unknown-length.md)
-   [列舉支援的通訊協定](enumerating-supported-protocols.md)

 

 
