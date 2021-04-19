---
description: 定義 WIC 中使用的詞彙。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b066757a-8841-4976-b20b-989ebba5eb3b
title: Windows 影像處理元件詞彙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6812024571727c8f769df88f8233119eed13ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001393"
---
# <a name="windows-imaging-component-glossary"></a>Windows 影像處理元件詞彙

## <a name="b"></a>B

<dl> <dt>

**位深度**
</dt> <dd>

可指定至影像中之單一像素的色彩值數目。 色彩深度範圍可從 1 位元 (黑白) 到 32 位元 (超過 1670 萬色)。 另請參閱：色彩深度

</dd> <dt>

**每圖元的位數 (bpp)**
</dt> <dd>

表示數位化影像中每個圖元之色彩值的位數。 另請參閱： BPP

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**剪**
</dt> <dd>

IWICBitmapClipper 物件。

</dd> <dt>

**編 解碼 器**
</dt> <dd>

此篩選會壓縮 (編碼) 或解壓縮 (資料流程) 資料串流。

</dd> <dt>

**色彩內容**
</dt> <dd>

色彩設定檔的抽象概念。 您可以從 (ie 的檔案載入設定檔。「sRGB 色彩空間設定檔. icm」 ) 或從讀取所取得的記憶體緩衝區。 色彩內容資訊是由 WIC 的 IWICColorCoNtext 介面所定義，並使用 GetColorCoNtext 方法來抓取。

</dd> <dt>

**色彩轉換**
</dt> <dd>

以指定的輸出像素格式，將來源色彩內容的色彩對應到目的色彩內容。

</dd> <dt>

**CYMK 色彩模型**
</dt> <dd>

多維度色彩空間，由組成指定色彩的青色、洋紅、黃色和黑色濃度所組成。

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**解碼 器**
</dt> <dd>

請參閱其他詞彙：編解碼器

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**編碼**
</dt> <dd>

請參閱其他詞彙：編解碼器

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**無損**
</dt> <dd>

一種壓縮類型，可確保原始資料可以完全復原，而不會遺失影像品質。

</dd> <dt>

**有損**
</dt> <dd>

將被視為不必要資訊的資料壓縮的程式會被移除，而且無法在解壓縮時復原。 通常會搭配音訊和視覺資料使用，在此情況下，品質會稍微降低。

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**多執行緒單元 (MTA)**
</dt> <dd>

元件物件模型 (COM) 所支援的多執行緒形式。 在多執行緒單元模型中，進程中已初始化為自由執行緒的所有線程都位於單一單元中。

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**原生像素格式**
</dt> <dd>

WIC 提供的其中一個像素格式，其中描述點陣圖中每個圖元的記憶體配置。

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**調色板**
</dt> <dd>

物件或應用程式所使用的色彩集合。

</dd> <dt>

**相片中繼資料原則**
</dt> <dd>

用於讀取、寫入和移除映射中繼資料的 windows 原則。

</dd> <dt>

**像素格式**
</dt> <dd>

記憶體中圖元色彩元件的大小和相片順序。 它是以每個圖元使用的總位數以及用來儲存色彩紅色、綠色、藍色和 Alpha 元件的位數來指定。 例如，RGB24 像素格式使用24個位來儲存圖元色彩，每個紅色、綠色和藍色各有8位。 ARGB32 像素格式使用32位，具有24位的色彩資訊和8位的 Alpha 色板資訊。

</dd> <dt>

**漸進式解碼**
</dt> <dd>

解碼已使用不同解碼層級相關資訊進行編碼之影像的進程。

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**流**
</dt> <dd>

是指可用於依序讀取或寫入檔案、記憶體或網路位置之資料的 IStream COM 介面。

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**語氣曲線**
</dt> <dd>

數位攝影中用來顯示影像色調範圍的圖形。

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**Windows 影像處理元件 (WIC)**
</dt> <dd>

可延伸的平臺，可為數字影像提供低層級的 API。

</dd> </dl>

 

 



