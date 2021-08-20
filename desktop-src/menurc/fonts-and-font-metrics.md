---
title: 字型和文字度量
description: 本主題討論 Windows 所提供的外框字型、Windows 版本之間可能會變更的字型度量值，以及如何在傳統型應用程式中使用字型度量的指引。
ms.assetid: B195154D-0168-4C5E-9CFB-AE7EF63D5F42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5199459c7a6afd311b120bd186df000e0fd32eef828ae986caf6da8573afe8bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687851"
---
# <a name="fonts-and-text-metrics"></a>字型和文字度量

本主題討論 Windows 所提供的外框字型、Windows 版本之間可能會變更的字型度量值，以及如何在傳統型應用程式中使用字型度量的指引。

-   如需 DirectWrite 中字型度量的特定資訊，請參閱[文字度量](/windows/desktop/DirectWrite/text-metrics)。
-   如需使用 GDI 來管理應用程式文字的詳細資訊，請參閱字型 [和文字](/windows/desktop/gdi/fonts-and-text)中的主題。

如需字型使用方式和類型規格的詳細資訊，請參閱 [Microsoft 印刷樣式網站](https://www.microsoft.com/typography/default.mspx)。

## <a name="available-fonts"></a>可用的字型

Windows 提供的大綱字型會以 OpenType 字型的形式傳遞，並使用 TrueType 大綱 (Windows 也支援 CFF 格式) 的 opentype 字型。 如需 Windows 所提供的所有字型清單，請參閱[Microsoft 印刷樣式：依產品或系列](https://www.microsoft.com/typography/fonts/default.aspx)提供的字型。 所有 Windows 大綱字型都符合最新版本的[OpenType 規格](https://www.microsoft.com/typography/otspec/)。

如需所有目前和舊版 UI 字型的清單，請參閱下方的 [鎖定字型計量](#locked-font-metrics) 。

## <a name="font-modifications"></a>字型修改

為了確保回溯相容性，字型很少會從 Windows 中移除。 不過，字型通常會經過修改。 修改可能包括新增字元、重新繪製現有的字元、修改提示，或是新增或修改先進 OpenType 功能和複雜字集成形的支援。

### <a name="locked-font-metrics"></a>鎖定的字型計量

請注意，某些與 Microsoft 應用程式中使用的 UI 字型和預設字型相關聯的值已鎖定。 UI 字型可用來呈現 UI 專案，例如字幕、對話方塊和功能表。 對這些字型進行極少的變更，並提供其高可見度和頻繁使用。 不過，因為與這些字型相關聯的報告值已鎖定，所以報告和實際字型值之間可能會有不一致的情況。

下列報告值會針對 UI 和預設字型鎖定，而且可能會被不准確地報告：

-   字型的 [OS/2 資料表](https://www.microsoft.com/typography/otspec/os2.htm)中的這些值：
    -   xAvgCharWidth
    -   sTypoLineGap
    -   sTypoAscender
    -   sTypoDescender
    -   usWinAscent
    -   usWinDescent
-   在字型標頭中設定的 [unitsPerEm](https://www.microsoft.com/typography/otspec/head.htm) 值
-   [垂直裝置計量表中的值 (VDMX) ](https://www.microsoft.com/typography/otspec/vdmx.htm)
-   個別字元的前進寬度

以下是受鎖定值影響的 Windows 8.1 (所附的 UI 字型清單) ：

| 指令碼名稱                   | UI 字型               |
|-------------------------------|-----------------------|
| 阿拉伯文                        | Segoe UI              |
| 亞美尼亞文                      | Segoe UI              |
| 孟加拉國文 (先前為孟加拉國文)      | Nirmala UI            |
| 符號                      | Microsoft JhengHei UI |
| 盲文                       | Segoe UI Symbol       |
| 布吉斯文                      | Leelawadee UI         |
| 加拿大土著音節 | Gadugi                |
| 卻洛奇文                      | Gadugi                |
| 科普特文                        | Segoe UI Symbol       |
| 簡體中文          | Microsoft YaHei UI    |
| 繁體中文         | Microsoft JhengHei UI |
| 古斯拉夫文                      | Segoe UI              |
| 梵文字母                    | Nirmala UI            |
| 萊特                       | Segoe UI Symbol       |
| 文                      | Ebrima                |
| 喬治亞文                      | Segoe UI              |
| 文                    | Segoe UI Symbol       |
| 哥 特 式                        | Segoe UI Symbol       |
| 希臘文                         | Segoe UI              |
| 古吉拉特文                      | Nirmala UI            |
| 古木基文                      | Nirmala UI            |
| Hebrew                        | Segoe UI              |
| 舊的斜體                    | Segoe UI Symbol       |
| 爪哇文                      | 爪哇文文字         |
| 日文                      | Meiryo UI             |
| 坎那達文                       | Mirmala UI            |
| 高棉文                         | Leelawadee UI         |
| 韓文                        | Malgun Gothic         |
| 寮文                           | Leelawadee UI         |
| 拉丁文                         | Segoe UI              |
| 馬來亞拉姆文                     | Nirmala UI            |
| 蒙古文                     | Mongolian Baiti       |
| 緬甸                       | Myanmar Text          |
| 西非書面                          | Ebrima                |
| 豎                         | Segoe UI Symbol       |
| 桑塔爾文                      | Nirmala UI            |
| 舊的土耳其文                    | Segoe UI Symbol       |
|  (以前的奧裡亞文)          | Nirmala UI            |
| 文                       | Ebrima                |
| 八位 pa                      | Microsoft PhagsPa     |
| 符文                         | Segoe UI Symbol       |
| Sora Sompeng                  | Nirmala UI            |
| 僧伽羅文                       | Nirmala UI            |
| 敘利亞文                        | Estrangelo Edessa     |
| 泰 Le                        | Microsoft Tai Le      |
| 新傣文                   | Microsoft New Tai Lue |
| 坦米爾文                         | Nirmala UI            |
| 泰盧固文                        | Nirmala UI            |
| 納                      | Ebrima                |
| 塔安那文                        | MV Boli               |
| 泰文                          | Leelawadee UI         |
| 西藏文                       | Microsoft Himalaya    |
| 范文                           | Ebrima                |
| 爨文                            | Microsoft Yi Baiti    |



 

以下是舊版 UI 字型的清單，這些字型也會受到鎖定值的影響：

|  (舊版) 的腳本名稱          | 舊版) 的 UI 字型 (               |
|-------------------------------|--------------------------------|
| 孟加拉國文 (先前為孟加拉國文)      | Vrinda                         |
| 加拿大土著音節 | Euphemia                       |
| 卻洛奇文                      | Plantagenet                    |
| 簡體中文          | Microsoft YaHei 和 SimSun     |
| 繁體中文         | MingLiU 和 Microsoft JhengHei |
| 梵文字母                    | 莽                         |
| 歐洲語言            | Tahoma                         |
| 古吉拉特文                      | Shruti                         |
| 古木基文                      | Raavi                          |
| 日文                      | Meiryo 和 MS Mt UI        |
| 坎那達文                       | Tunga                          |
| 高棉文                         | 高棉文                          |
| 韓文                        | Gulim                          |
| 寮文                           | 老撾文 UI                         |
| 馬來亞拉姆文                     | Kartika                        |
| 中東語言      | Tahoma                         |
|  (以前的奧裡亞文)          | Kalinga                        |
| Sinhalese                     | Iskoola Pota                   |
| 坦米爾文                         | Latha 和 Vijaya               |
| 泰盧固文                        | Gautami                        |
| 泰文                          | Leelawadee 和 Tahoma          |



 

在 Microsoft 應用程式中會使用這些字型作為預設值，而且也會受到鎖定值的影響：

-   Arial
-   Calibri
-   Cambria
-   Consolas
-   Courier New
-   MS Mincho
-   Times New Roman
-   Verdana

### <a name="dynamic-font-metrics"></a>動態字型計量

除了上面所列的鎖定計量以外，也會正確地報告字型值。 如果新版本的 Windows 中的字型有所變更，則新的和舊的字型值會不同。 例如，當字型加入字型時，字型標頭中的值可能會變更。 如果這些值 (（包括 xMin、xMax、yMin 和 yMax），並報告字型) 中圖像的最小和最大周框方塊已鎖定，且未回報 true 值，則可能會產生裁剪。

> [!IMPORTANT]
> 如果您在應用程式中使用動態字型值 (與 [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)) 中的值相同，則這些值會在未來的 Windows 版本中修改時變更。 請勿在文字必須保持靜態的情況下使用這些實際值。

 

## <a name="guidelines-for-using-font-metrics"></a>使用字型計量的指導方針

-   計算畫面計量和字型計量 (例如，應用程式啟動時的平均寬度) ，並使用這些值來配置您的應用程式。 這會提供一致的精確轉譯，而您的版面配置會回應字型中的變更或容納字型的回復。 如需字型回復與字型連結的總覽，請參閱「 [全球化逐步解說：字型」](https://msdn.microsoft.com/goglobal/bb688134.aspx)。 請參閱 [使用字型](/windows/desktop/Intl/using-font-fallback) 回復來取得 Uniscribe 特定的資訊。
    -   若要計算基底度量，請針對您想要的語言/腳本轉譯代表性文字。
    -   如果控制項只包含一行未包裝的文字，請將它們配置出來，以符合未修剪文字的全形。
    -   針對具有多行的控制項，取得總長度（除以字元長度），而且您可以使用純色寬度。 請注意，對於讀取器的單一「字元」可能是多個程式碼點的複雜字集而言，這會比較棘手。
-   使用 [OS/2 資料表](https://www.microsoft.com/typography/otspec/os2.htm)) 的 STypoAscender、STypoDescender 和 unitsPerEm (來計算垂直間距。 sTypoAscender 是用來判斷從文字框架頂端到第一個基準的最佳位移，而 sTypoDescender 則會決定從文字框架底部到最後一個基準的最佳位移。
-   如果您是使用 DirectWrite，請使用 [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)來建立版面配置。 **IDWriteTextLayout** 提供  +  自然配置中的 ascender **下行**  +  **lineGap** 。 您可以使用 [**DWRITE \_ 字型 \_ 計量**](/windows/desktop/api/dwrite/ns-dwrite-dwrite_font_metrics)來存取這些特定的值。 如需此介面的詳細資訊，請參閱 [文字格式設定和](/windows/desktop/DirectWrite/text-formatting-and-layout)配置。
-   如果您使用的是 GDI，則會在螢幕上呈現，然後檢查配置 (例如，每行的行長度或字元) ，然後重新計算實際轉譯中使用的最終版面配置參數。
-   請勿根據特定字型版本的特定值，以靜態方式建立版面配置。 實際值可能會隨著版本而變更。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**DWRITE \_ 字型 \_ 計量**](/windows/desktop/api/dwrite/ns-dwrite-dwrite_font_metrics)
</dt> <dt>

[**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)
</dt> <dt>

[unitsPerEm](https://www.microsoft.com/typography/otspec/head.htm)
</dt> <dt>

[OS/2 資料表](https://www.microsoft.com/typography/otspec/os2.htm)
</dt> <dt>

[垂直裝置計量表 (VDMX) ](https://www.microsoft.com/typography/otspec/vdmx.htm)
</dt> <dt>

[Microsoft 印刷樣式：依產品或家族的字型](https://www.microsoft.com/typography/fonts/default.aspx)
</dt> <dt>

**概念**
</dt> <dt>

[文字度量 (DirectWrite) ](/windows/desktop/DirectWrite/text-metrics)
</dt> <dt>

[ (GDI) 的字型和文字 ](/windows/desktop/gdi/fonts-and-text)
</dt> <dt>

[Microsoft Typography](https://www.microsoft.com/typography/default.mspx)
</dt> </dl>

 

 