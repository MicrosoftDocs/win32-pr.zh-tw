---
description: 地區設定不 \_ 變
ms.assetid: d37df17d-8cd5-4481-bee2-062cf9d78e9b
title: LOCALE_INVARIANT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca1e526b91ba372ed7efaad62e9e1597b0d5130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991711"
---
# <a name="locale_invariant"></a>地區設定不 \_ 變

**WINDOWS XP：** 用於作業系統層級功能的地區設定，這些函式需要一致且與地區設定無關的結果。 例如，當應用程式使用 [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) 函式來比較字元字串時，會使用不變的地區設定，而且不論使用者的地區設定為何，都需要一致的結果。 非變異地區設定的設定與) 美國英文 (的設定相似，但不能用來顯示格式化的資料。 一般而言，應用程式不會使用地區設定非變異， \_ 因為它預期動作的結果取決於管理每個個別地區設定的規則。 地區設定 \_ 不變的值為0x007f。

 

 
