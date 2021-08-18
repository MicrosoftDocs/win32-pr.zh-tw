---
description: 您的應用程式應該使用換行字元 (0x2028) 和段落分隔符號 (0x2029) 來分隔純文字。 在每個行分隔字元後方會開始新行。 在每個段落分隔字元後方會開始新段落。
ms.assetid: 086aca6c-8d1f-4e54-9e1c-642be50b303c
title: 使用線條和段落分隔符號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857d7cae4dc7bd720ca94e9780bcb83588650b3df578cd0216e2424c1b28d5af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764628"
---
# <a name="using-line-and-paragraph-separators"></a>使用線條和段落分隔符號

您的應用程式應該使用換行字元 (0x2028) 和段落分隔符號 (0x2029) 來分隔純文字。 在每個行分隔字元後方會開始新行。 在每個段落分隔字元後方會開始新段落。

您不需要以這些字元來啟動檔案中的第一行或段落，也不需要用它們來結束最後一行或段落。 這麼做會指出該位置中有空白行或段落。

應用程式可以使用行分隔符號來表示無條件的行尾。 不過，行分隔字元不會對應至個別的歸位字元與換行字元，或是對應至這些字元的組合。 行分隔字元必須與歸位字元和換行字元分開個別處理。

應用程式可以在文欄位落之間插入段落分隔符號。 使用此分隔字元可讓您建立純文字檔案，以在不同作業系統上使用各種不同的行寬度進行格式化。 目標系統可以忽略任何行分隔符號，而只在段落分格符號所在位置分段。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Unicode 中的特殊字元](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



