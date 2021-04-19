---
description: InkEdit 控制項的預設行為是在短時間過期之後，辨識並將筆墨轉換成文字。
ms.assetid: d141bcec-e9a8-48b8-86cf-9476a2cc6f9f
title: 將筆墨顯示為筆墨
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aca1d6a1a4700d996d65a9cfd7d62e6b27e1c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975864"
---
# <a name="displaying-ink-as-ink"></a>將筆墨顯示為筆墨

[InkEdit](inkedit-control-reference.md)控制項的預設行為是在短時間過期之後，辨識並將筆墨轉換成文字。 因為控制項是 [RichEdit](../controls/rich-edit-controls.md)的超級類別，所以也可以在控制項內內嵌和顯示筆墨。 每個單字都會插入控制項中做為 [**InkDisp**](inkdisp-class.md) 物件。 **InkDisp** 物件包含筆墨及其辨識替代項。

插入時，會將筆墨調整為目前的字型大小和其他環境屬性，例如斜體或粗體。 如果使用者選擇編輯 [**InkDisp**](inkdisp-class.md) 物件的文字，則必須先將筆墨轉換成文字。

> [!Note]  
> 在轉換期間，所有筆墨和辨識替代資料都會遺失。

 

這項功能僅適用于執行 Microsoft Windows XP Tablet PC Edition、Windows Vista 或更新版本的電腦。

 

 
