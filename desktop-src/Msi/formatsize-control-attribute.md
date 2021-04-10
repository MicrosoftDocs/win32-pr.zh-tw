---
description: 如果設定靜態文字控制項的這個位，控制項會自動嘗試將顯示的文字格式化為代表位元組計數的數位。
ms.assetid: acf76fff-b7a4-456b-91b9-eb3087879d7b
title: FormatSize 控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7fa656b81272b8ac60985d3dac0416c0f81bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191865"
---
# <a name="formatsize-control-attribute"></a>FormatSize 控制項屬性

如果設定靜態文字控制項的這個位，控制項會自動嘗試將顯示的文字格式化為代表位元組計數的數位。 若要進行適當的格式設定，必須將控制項的文字設定為代表以512位元組單位表示之數位的字串。 然後，顯示的值會以 kb 為單位來格式化 (KB) 、mb (MB) 或 gb (GB) ，並以代表單位的適當字串顯示。 如需詳細資訊，請參閱 [文字控制項](text-control.md)。



| 原始文字的數值 | 使用的單元字串 |
|----------------------------------|------------------|
| 小於20480                  | KB               |
| 小於20971520               | MB               |
| 小於10737418240            | GB               |



 

## <a name="valid-controls"></a>有效的控制項



| Decimal | 十六進位 | 控制                          |
|---------|-------------|----------------------------------|
| 524288  | 0x00080000  | msidbControlAttributesFormatSize |



 

## <a name="remarks"></a>備註

若要在控制項上設定此屬性，請在控制項 [資料表](control-table.md)的 [屬性] 資料行中包含 FormatSize 位。 控制項的文字必須設定為代表以512位元組單位表示之數位的字串。 單元字串的文字定義于 [UIText 資料表](uitext-table.md)中。 單元字串的位置是由 [**LeftUnit**](leftunit.md) 屬性所控制。 如果 **LeftUnit** 屬性定義為任何值，則單元字串會出現在數值之前。 如果與控制項相關聯的文字中出現數位字元以外的任何內容，則顯示的值為未定義。

在執行時間，安裝程式會將 [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) 屬性解析為安裝所需的位元組總數（以512為單位）。 具有 FormatSize 位的靜態文字控制項可以用來自動格式化及標記安裝所需的位元組總數（以 KB、MB 或 GB 為單位）。 基於此範例的目的，假設總位元組數為18336768。 安裝程式會將 PrimaryVolumeSpaceRequired 屬性的值設定為18336768除以512或35814。 文字控制項使用 FormatSize 顯示的數位會是17MB。

原始文字的數值會以512的單位來提供。 在上表中，字串20480對應至 KB 字串，因為20480次512會產生10485760位元組或 10240 KB 的結果。

上表所列的單位字串參考 [UIText 資料表](uitext-table.md)中的索引鍵，其中定義了單元字串的文字。

單元字串的位置是由 [**LeftUnit**](leftunit.md) 屬性所控制。 如果 **LeftUnit** 屬性定義為任何值，則單元字串會出現在數值之前。

如果與控制項相關聯的文字中出現數位字元以外的任何內容，則顯示的值為未定義。

如需詳細資訊，請參閱 [控制屬性](control-attributes.md) 和 [控制項](controls.md)。

 

 



