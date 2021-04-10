---
title: KeyboardShortcut 屬性
description: KeyboardShortcut 屬性描述會啟用指定之可存取物件的按鍵或按鍵組合。
ms.assetid: 42587468-f069-4ef1-868e-ac6a285e1715
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002c925151f3f1acc136190d7807d7bc814d30b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183532"
---
# <a name="keyboardshortcut-property"></a>KeyboardShortcut 屬性

**KeyboardShortcut** 屬性描述會啟用指定之可存取物件的按鍵或按鍵組合。

藉由呼叫 [**IAccessible：： get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)，即可取出 **KeyboardShortcut** 屬性。

取出的字串會描述快速鍵 (也稱為 *鍵盤**快捷方式*) 或 *存取金鑰* (也稱為 *助記* 鍵) 。 存取金鑰是功能表、功能表項目或控制項標籤（例如按下按鈕）文字中的加底線字元。

抓取的字串必須包含索引鍵的名稱，以及輔助按鍵或索引鍵。 字串必須採用下列格式，用戶端才能輕鬆地剖析它： \[ \[ 輔助按鍵 ... 索引 \] + \[ \] + \] 鍵名稱。

範例包括 ALT + F、CTRL + ALT + 4、WIN + F1、CTRL + ALT + SHIFT + 倒退鍵或單純倒退鍵。

下表列出輔助按鍵。



| 輔助按鍵 | Description                        |
|--------------|------------------------------------|
| ALT          | 替代輔助按鍵             |
| CTRL         | 控制輔助按鍵               |
| SHIFT        | Shift 輔助按鍵                 |
| 贏得          | Windows 標誌鍵                   |
| FN           | 可攜式電腦上的功能機碼 |



 

請勿當地語系化鍵盤快速鍵字串。

## <a name="handling-objects-that-have-both-key-types"></a>處理具有兩個索引鍵類型的物件

如果物件同時具有快速鍵和存取金鑰， **KeyboardShortcut** 屬性會傳回存取金鑰。 存取金鑰是當物件或物件的父系具有鍵盤焦點時，使用者會按下的按鍵。 例如，[ **列印** ] 功能表項目可能會同時有快速鍵 (CTRL + P) 和 (P) 的存取金鑰。 如果使用者在功能表使用中時按 CTRL + P，就不會發生任何事。 但是，如果使用者在功能表使用中時按 P，就會叫用應用程式的 [ **列印** ] 對話方塊。 在此情況下， **KeyboardShortcut** 屬性為 "P"，以反映當功能表具有鍵盤焦點時，使用者必須按下的內容。

 

 




