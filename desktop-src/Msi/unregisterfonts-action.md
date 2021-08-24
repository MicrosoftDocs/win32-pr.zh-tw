---
description: UnregisterFonts 動作會從系統中移除已安裝字型的註冊資訊。
ms.assetid: 97cbbcbe-eb1c-45f0-91d2-4b17984498ae
title: UnregisterFonts 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ec15a7a431a03d678fb2fd8c39460ea40ebbcadf3efd0c24814c84e6042fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786998"
---
# <a name="unregisterfonts-action"></a>UnregisterFonts 動作

UnregisterFonts 動作會從系統中移除已安裝字型的註冊資訊。

## <a name="sequence-restrictions"></a>順序限制

您必須在 UnregisterFonts 之後呼叫 [RemoveFiles](removefiles-action.md) 動作。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述 |
|-------|----------------------------|
| \[1\] | 字型檔。                 |



 

## <a name="remarks"></a>備註

如果字型資料表的 File 資料行中指定的檔案 \_ 屬於正在卸載的[](font-table.md)元件，則會執行 UnregisterFonts 動作。

 

 



