---
title: FONTDIRENTRY 結構
description: 包含字型資源群組中個別字型的相關資訊。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: 0ada2afe-b299-4ef2-99b7-96da10ee218a
keywords:
- FONTDIRENTRY 結構功能表和其他資源
topic_type:
- apiref
api_name:
- FONTDIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e236104730dbbfe79ec0ed3d18cbb465402ed8827c6037a2457bec18faf63024
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886738"
---
# <a name="fontdirentry-structure"></a>FONTDIRENTRY 結構

包含字型資源群組中個別字型的相關資訊。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。

## <a name="syntax"></a>語法


```C++
typedef struct {
  WORD  dfVersion;
  DWORD dfSize;
  CHAR  dfCopyright[60];
  WORD  dfType;
  WORD  dfPoints;
  WORD  dfVertRes;
  WORD  dfHorizRes;
  WORD  dfAscent;
  WORD  dfInternalLeading;
  WORD  dfExternalLeading;
  BYTE  dfItalic;
  BYTE  dfUnderline;
  BYTE  dfStrikeOut;
  WORD  dfWeight;
  BYTE  dfCharSet;
  WORD  dfPixWidth;
  WORD  dfPixHeight;
  BYTE  dfPitchAndFamily;
  WORD  dfAvgWidth;
  WORD  dfMaxWidth;
  BYTE  dfFirstChar;
  BYTE  dfLastChar;
  BYTE  dfDefaultChar;
  BYTE  dfBreakChar;
  WORD  dfWidthBytes;
  DWORD dfDevice;
  DWORD dfFace;
  DWORD dfReserved;
  CHAR  szDeviceName;
  CHAR  szFaceName;
} FONTDIRENTRY;
```



## <a name="members"></a>成員

<dl> <dt>

**dfVersion**
</dt> <dd>

類型： **WORD**

</dd> <dd>

工具可用來讀取和寫入資源檔的資源資料的使用者定義版本號碼。

</dd> <dt>

**dfSize**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

檔案的大小（以位元組為單位）。

</dd> <dt>

**dfCopyright \[ 60\]**
</dt> <dd>

類型： **CHAR**

</dd> <dd>

字型供應商的著作權資訊。

</dd> <dt>

**dfType**
</dt> <dd>

類型： **WORD**

</dd> <dd>

字型檔案的類型。

</dd> <dt>

**dfPoints**
</dt> <dd>

類型： **WORD**

</dd> <dd>

這個字元集最適合的點大小。

</dd> <dt>

**dfVertRes**
</dt> <dd>

類型： **WORD**

</dd> <dd>

此字元集已數位化的垂直解析度（以英寸為單位）。

</dd> <dt>

**dfHorizRes**
</dt> <dd>

類型： **WORD**

</dd> <dd>

此字元集已數位化的水準解析度（以英寸為單位）。

</dd> <dt>

**dfAscent**
</dt> <dd>

類型： **WORD**

</dd> <dd>

從字元定義儲存格頂端到印刷字型基準的距離。

</dd> <dt>

**dfInternalLeading**
</dt> <dd>

類型： **WORD**

</dd> <dd>

**DfPixHeight** 成員所設定之界限內的開頭數量。 此區域可能會出現重音符號和其他的變音符號字元。

</dd> <dt>

**dfExternalLeading**
</dt> <dd>

類型： **WORD**

</dd> <dd>

應用程式在資料列之間新增的額外前置量。

</dd> <dt>

**dfItalic**
</dt> <dd>

類型： **位元組**

</dd> <dd>

如果不等於零，則為斜體字型。

</dd> <dt>

**dfUnderline**
</dt> <dd>

類型： **位元組**

</dd> <dd>

如果不等於零，則為加上底線的字型。

</dd> <dt>

**dfStrikeOut**
</dt> <dd>

類型： **位元組**

</dd> <dd>

如果不等於零，則為刪除線字型。

</dd> <dt>

**dfWeight**
</dt> <dd>

類型： **WORD**

</dd> <dd>

範圍0到1000的字型粗細。 例如，400為羅馬，700為粗體。 如果此值為零，則會使用預設權數。 如需其他定義的值，請參閱 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構的描述。

</dd> <dt>

**dfCharSet**
</dt> <dd>

類型： **位元組**

</dd> <dd>

字型的字元集。 如需預先定義的值，請參閱 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構的描述。

</dd> <dt>

**dfPixWidth**
</dt> <dd>

類型： **WORD**

</dd> <dd>

為向量字型進行數位化的格線寬度。 針對點陣字型，如果成員不等於零，則代表點陣圖中所有字元的寬度。 如果成員等於零，字型就會有可變寬度的字元。

</dd> <dt>

**dfPixHeight**
</dt> <dd>

類型： **WORD**

</dd> <dd>

點陣字型的字元點陣圖高度，或向量字型已數位化之格線的高度。

</dd> <dt>

**dfPitchAndFamily**
</dt> <dd>

類型： **位元組**

</dd> <dd>

字型的音調和系列。 如需詳細資訊，請參閱 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構的描述。

</dd> <dt>

**dfAvgWidth**
</dt> <dd>

類型： **WORD**

</dd> <dd>

字型中字元的平均寬度 (通常定義為字母 x) 的寬度。 此值不包含粗體或斜體字元所需的懸垂。

</dd> <dt>

**dfMaxWidth**
</dt> <dd>

類型： **WORD**

</dd> <dd>

字型中最寬字元的寬度。

</dd> <dt>

**dfFirstChar**
</dt> <dd>

類型： **位元組**

</dd> <dd>

字型中定義的第一個字元碼。

</dd> <dt>

**dfLastChar**
</dt> <dd>

類型： **位元組**

</dd> <dd>

在字型中定義的最後一個字元碼。

</dd> <dt>

**dfDefaultChar**
</dt> <dd>

類型： **位元組**

</dd> <dd>

要替代字型中不是字元的字元。

</dd> <dt>

**dfBreakChar**
</dt> <dd>

類型： **位元組**

</dd> <dd>

將用來定義文字對齊方式之斷詞的字元。

</dd> <dt>

**dfWidthBytes**
</dt> <dd>

類型： **WORD**

</dd> <dd>

點陣圖每個資料列中的位元組數目。 此值一律為偶數，因此資料列會在字邊界上開始。 若為向量字型，此成員沒有任何意義。

</dd> <dt>

**dfDevice**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

檔案中的位移，表示指定裝置名稱的以 null 終止的字串。 若為泛型字型，此值為零。

</dd> <dt>

**dfFace**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

檔案中的位移，表示命名為以 null 終止的字串，該字串會為字樣命名。

</dd> <dt>

**dfReserved**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

這個成員是保留的。

</dd> <dt>

**szDeviceName**
</dt> <dd>

類型： **CHAR**

</dd> <dd>

如果指定特定裝置的字型檔案，則為裝置的名稱。

</dd> <dt>

**szFaceName**
</dt> <dd>

類型： **CHAR**

</dd> <dd>

字型的字型名稱。

</dd> </dl>

## <a name="remarks"></a>備註

.Res 檔中的每個字型都有一個 **FONTDIRENTRY** 結構。 使用字型資源產生 .res 檔案的應用程式，也必須將每個字型的 **FONTDIRENTRY** 結構新增至檔案。

字型聲明可以與中的其他資源宣告混合使用。RC 檔案，因為字型在 .res 檔中不需要是連續的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DIRENTRY**](direntry.md)
</dt> <dt>

[**FONTGROUPHDR**](fontgrouphdr.md)
</dt> <dt>

**概念**
</dt> <dt>

[資源](resources.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

