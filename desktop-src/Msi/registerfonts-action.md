---
description: RegisterFonts 動作會向系統註冊已安裝的字型。 此動作會將字型資料表的 FontTitle 資料行中的字型名稱對應到所安裝字型檔案的路徑。
ms.assetid: 3c6d3ec9-b36f-46f4-8b32-c97a75b9e238
title: RegisterFonts 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98532be2744e89fff79f6e3d8becd2e6cc9259a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993121"
---
# <a name="registerfonts-action"></a>RegisterFonts 動作

RegisterFonts 動作會向系統註冊已安裝的字型。 此動作會將 [字型資料表](font-table.md) 的 FontTitle 資料行中的字型名稱對應到所安裝字型檔案的路徑。

## <a name="sequence-restrictions"></a>順序限制

呼叫 RegisterFonts 動作之前，必須先呼叫 [InstallFiles](installfiles-action.md) 動作。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述 |
|-------|----------------------------|
| \[1\] | 字型檔。                 |



 

## <a name="remarks"></a>備註

如果字型資料表的 File 資料行中指定的檔案 \_ 屬於正在安裝的[](font-table.md)元件，則會執行 RegisterFonts 動作。

 

 



