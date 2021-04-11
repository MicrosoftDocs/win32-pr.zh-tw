---
description: BindImage 動作會系結必須系結至它所匯入之 Dll 的每個可執行檔或 DLL。
ms.assetid: bf90acc0-4e90-4180-9df7-268b63a66538
title: BindImage 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2ac4c5ca16b83a3f0f0796d9a755542ec108c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848951"
---
# <a name="bindimage-action"></a>BindImage 動作

BindImage 動作會系結必須系結至它所匯入之 Dll 的每個可執行檔或 DLL。 BindImage 動作會在 [BindImage](bindimage-table.md) 資料表中的每個檔案上運作，但僅適用于要在本機安裝的檔案。 安裝程式會計算從所有 Dll 匯入之每個函式的虛擬位址，然後將計算出的虛擬位址儲存在匯入映射的匯 [*入位址表*](i-gly.md) 中 (IAT) 。

BindImage 動作會在內部呼叫 **BindImageEx** Windows API。

## <a name="sequence-restrictions"></a>順序限制

BindImage 動作必須晚于 [InstallFiles](installfiles-action.md) 動作。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述     |
|-------|--------------------------------|
| \[1\] | 可執行檔的檔案識別碼。 |



 

 

 



