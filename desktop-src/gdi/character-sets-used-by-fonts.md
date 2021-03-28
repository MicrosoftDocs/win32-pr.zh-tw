---
description: 所有字型都使用字元集。 字元集包含標點符號、數位、大寫和小寫字母，以及所有其他可列印字元。 字元集的每個專案都是以數位來識別。
ms.assetid: 7989c59e-2ec6-4d1a-bb86-f4037ca32764
title: 字型所使用的字元集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33c4c5cc193c4474b39113acdedafec699456e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972772"
---
# <a name="character-sets-used-by-fonts"></a>字型所使用的字元集

所有字型都使用字元集。 字元集包含標點符號、數位、大寫和小寫字母，以及所有其他可列印字元。 字元集的每個專案都是以數位來識別。

大部分使用中的字元集都是美國 ASCII 字元集的超集合，它會定義32到127的96數值字元。 字元集有五個主要群組：

-   Windows
-   Unicode
-   OEM (原始設備製造商)
-   符號
-   特定廠商

## <a name="windows-character-set"></a>Windows 字元集

Windows 字元集是最常使用的字元集。 它基本上相當於 ANSI 字元集。 空白字元是 Windows 字元集中的第一個字元。 它的十六進位值為 0x20 (decimal 32) 。 Windows 字元集中的最後一個字元具有十六進位值 0xFF (decimal 255) 。

許多字型會指定預設字元。 只要針對不在字型中的字元提出要求，系統就會提供此預設字元。 使用 Windows 字元集的許多字型都會指定句點 (。 ) 為預設字元。 TrueType 和 OpenType 字型通常會使用開放方塊作為預設字元。

字型使用稱為四的分隔字元來分隔單字和對齊文字。 大部分使用 Windows 字元集的字型都會指定空白字元將作為 break 字元。

## <a name="unicode-character-set"></a>Unicode 字元集

Windows 字元集會使用8個位來代表每個字元;因此，可以使用8位表示的最大字元數為 256 (2 ^ 8) 。 這通常就足以滿足西方語言的需求，包括法文、德文、西班牙文和其他語言所使用的變音符號。 不過，東部語言採用數以千計的不同字元，無法使用單一位元組編碼配置進行編碼。 隨著電腦 commerce 的激增，已開發雙位元組編碼配置，因此可以在8位、16位、24位或32位序列中表示字元。 這需要複雜的傳遞演算法;如此一來，使用不同的程式碼集會在兩部不同的電腦上產生完全不同的結果。

為了解決多個程式碼撰寫架構的問題，已開發出資料標記法的 Unicode 標準。 16位字元編碼配置，Unicode 可以代表 65536 (2 ^ 16) 個字元，這足以包含目前電腦 commerce 中的所有語言，以及標點符號、數學符號和擴充的空間。 Unicode 會為每個字元建立唯一的程式碼，以確保字元轉譯永遠正確。

## <a name="oem-character-set"></a>OEM 字元集

OEM 字元集通常用於螢幕顯示的全螢幕 MS-DOS 會話中。 在 OEM、美國 ASCII 和 Windows 字元集中，字元32到127通常相同。 OEM 字元集中的其他字元 (0 到31和128到 255) 對應到可在全螢幕 MS-DOS 會話中顯示的字元。 這些字元通常與 Windows 字元不同。

## <a name="symbol-character-set"></a>符號字元集

符號字元集包含通常用來表示數學和科學公式的特殊字元。

## <a name="vendor-specific-character-sets"></a>廠商特定字元集

許多印表機和其他輸出裝置會根據與 Windows 和 OEM setsfor 範例不同的字元集提供字型， (EBCDIC) 字元集的擴充二進位編碼十進位交換程式碼。 若要使用這些字元集的其中一個，印表機驅動程式會從 Windows 字元集轉譯為廠商特定字元集。

 

 



