---
title: 如何在 Rich Edit 控制項中使用字型系結
description: Microsoft Rich Edit 3.0 會根據其內容將字元集指派為純文字字元。
ms.assetid: 975B9C33-6766-4FF1-A93E-2169C140CEE9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3086f9f74469bc535700f28b6eeb45c204024beb34c21663139fd3d63746d4ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829022"
---
# <a name="how-to-use-font-binding-in-rich-edit-controls"></a>如何在 Rich Edit 控制項中使用字型系結

Microsoft Rich Edit 3.0 會根據其內容將字元集指派為純文字字元。 部分範例如下：

-   希臘文字元是被指派的 **希臘文 \_ 字元集**。
-   韓文符號是指派給 **韓文 \_ 字元集**。
-   如果找到附近的假名字元，則會將 **SHIFTJIS \_ 字元集** 指派給中文字元，如果附近找不到假名，則為 **GB2312 \_ 字元集** 。
-   在任何事件中，會將 **ansi \_ 字元集** 指派為非中性 ansi 字元。

> [!Note]  
> Rich edit 控制項會在內部使用 Unicode，因此這種字元集的使用方式與字型規格中使用的原始字元集不同。 但是 [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) 結構具有妥善定義的字元集位置。

 

空白和數位等中性字元會根據其內容指派一個字元集。 例如，以相同字元集的字元括住的空白會取得該字元集。 雙向文字所使用的 Neutrals 和位數，是以 Unicode 雙向演算法為基礎的指定字元集。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [Windows控制](window-controls.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Windows消費者介面程式設計

## <a name="instructions"></a>指示

### <a name="use-font-binding-in-a-rich-edit-control"></a>在 Rich Edit 控制項中使用字型系結

在指派字元集之後，Rich Edit 會向前和向後掃描插入點周圍的文字，以找出最接近用於字元集的字型。 如果找不到字元集的字型，Rich Edit 會使用用戶端為該字元集所選擇的字型。 如果用戶端尚未指定字元集的字型，Rich Edit 會針對該字元集使用預設字型。 如果用戶端想要使用其他字型，用戶端一律可以變更它，但這種方法大部分的時候都能運作。 目前的預設字型選項是以下表為基礎。 請注意，預設字型是針對每個進程設定的，而且有不同的 UI 使用方式和非 UI 用法清單。



| 語言                    | UI 字型名稱  | UI 字型大小 | 非 UI 字型名稱 | 非 UI 的字型大小 |
|-----------------------------|---------------|--------------|------------------|------------------|
| 西方、CE、我、越南文 | Tahoma        | 8            | Arial            | 10               |
| 日文                    | MS UI Mt  | 9            | MS P Mt      | 10               |
| 韓文                      | Gulim         | 9            | Gulim            | 9                |
| 簡體中文          | Simsun        | 9            | SimSun           | 10               |
| 繁體中文         | Simsun      | 9            | Simsun         | 9                |
| 泰文                        | MS Sans Serif | 8            | Tahoma           | 14               |
| 符號                     | Wingdings 應有盡有     | 8            | Wingdings 應有盡有        | 10               |
| 梵文字母                  | 莽        | 8            | 莽           | 10               |
| 坦米爾文                       | Latha         | 8            | Latha            | 10               |
| 格魯吉亞文，亞美尼亞文          | Arial Unicode | 8            | Arial Unicode    | 10               |



 

因此，在預設的字型系結表中 (專案具有字元集、字型名稱和大小) ，Rich Edit 可讓 ANSI \_ 字元集符合數個字元集，而適當的字元集則符合其他字型的一對一基礎。 更精確地說， \_ 如果找不到其他替代方案，rich edit 會使用 ANSI 字元集選擇。 您將能指定比這個更細微的資料細微性;例如，指派阿拉伯文執行的特定阿拉伯文 \_ 字元集、希臘文執行的特定希臘文字型等等。 如果在字型系結的區域之前，在檔的某處找到具有所需字元集戳記的字型，也會使用這個更細微的資料細微性。

請注意，Rich Edit 目前不會處理支援字元集的字型中遺失的圖像，但不完整。 在複雜字集中的顯示時間，Rich Edit 最後會知道這類圖像遺失，但不會導致備份存放區使用新的字型。 一般而言，作業系統的基礎字型連結將會完成這項作業。

## <a name="remarks"></a>備註

**Rich Edit 4.1：** 若要設定腳本的預設字型，請使用 [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)呼叫 [**EM \_ SETCHARFORMAT**](em-setcharformat.md) ，指定 **yHeight**、 **bCharSet**、 **bPitchAndFamily**、 **szFaceName** 和 **lcid** 成員的值。 此外，若要取得特定字碼頁的預設字型，請使用 **CHARFORMAT2** 呼叫 [**EM \_ GETCHARFORMAT**](em-getcharformat.md) ，指定 **bCharSet** 和 **lcid** 成員的值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Rich Edit 控制項](using-rich-edit-controls.md)
</dt> <dt>

[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




