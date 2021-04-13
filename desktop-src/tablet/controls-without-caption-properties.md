---
description: 針對 Tablet PC 使用沒有標題屬性之控制項的簡介。
ms.assetid: 8c44e1eb-8d57-4c3b-a329-c8ad77423cb7
title: 沒有 Caption 屬性的控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6c9a52d7c6c89e7233e32f7f5d7dc295bc289e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510756"
---
# <a name="controls-without-caption-properties"></a>沒有 Caption 屬性的控制項

當控制項沒有自己的標題屬性時，請採取下列步驟來確保協助工具輔助可識別控制項：

-   建立具有有意義和描述性名稱的靜態文字控制項。
-   將靜態標籤放在參考的控制項上方（依 tab 順序）。
-   確定標籤文字的結尾是冒號，例如 "Settings："
-   將標籤文字緊接在參考的控制項左方或前面。
-   如果不適合以視覺化方式顯示靜態文字，請將其設為隱藏。 若要這麼做，請在資源腳本中指派適當的屬性。 當控制項的名稱或函式是透過靜態文字控制項（例如圖形或相關的選項按鈕）來以視覺化方式提供時，這可能會很適合。

靜態控制項的適當使用方式，是針對沒有內建標籤的控制項正確地執行加上底線的便捷鍵。 如需使用沒有標題屬性之控制項的詳細資訊，請參閱 [協助工具](/windows/desktop/accessibility) 一節。

 

 
