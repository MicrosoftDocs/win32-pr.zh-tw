---
description: Language 資料類型是包含一或多個有效數字語言識別項的文字字串。 如果有兩個以上的語言識別項，則必須以逗號分隔。
ms.assetid: 547fc662-f055-421e-a621-eecdfa0b13f6
title: 語言
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc87cb8b88dc3a693eee6890276adb67ad359e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191374"
---
# <a name="language"></a>語言

Language 資料類型是包含一或多個有效數字語言識別項的文字字串。 如果有兩個以上的語言識別項，則必須以逗號分隔。

Language 資料類型是16位的值，也就是主要和子語言數值識別碼的組合。 主要 LANGID 由位0到9組成，而子語言識別項是位10到15。 如需主要和次要語言數值識別碼的清單，請參閱 [語言識別項常數和字串](../intl/language-identifier-constants-and-strings.md) 主題。

針對主要語言識別項，0x200 至0x3ff 的範圍是由使用者定義的。 0x000 至0x1ff 的範圍保留供系統使用。 若為子語言識別項，則會以使用者可定義的範圍0x20 至0x3f。 從0x00 到0x1f 的範圍是保留供系統使用。

 

 
