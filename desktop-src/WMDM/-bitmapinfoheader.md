---
title: _BITMAPINFOHEADER 結構
description: '\_BITMAPINFOHEADER 結構會定義影片框架的格式。'
ms.assetid: 394b8ded-81db-4ad3-8cf7-086f1e832771
keywords:
- _BITMAPINFOHEADER 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- _BITMAPINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481c80b6d209e0da8d00ef06d88392504bcae8e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995449"
---
# <a name="_bitmapinfoheader-structure"></a>\_BITMAPINFOHEADER 結構

**\_ BITMAPINFOHEADER** 結構會定義影片框架的格式。

## <a name="syntax"></a>語法


```C++
typedef struct _tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} _BITMAPINFOHEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**biSize**
</dt> <dd>

指定結構所需的位元組數目。

</dd> <dt>

**biWidth**
</dt> <dd>

指定點陣圖的寬度（以圖元為單位）。

</dd> <dt>

**biHeight**
</dt> <dd>

指定點陣圖的高度（以圖元為單位）。 如果 **biHeight** 是正數，則點陣圖是最下層的 DIB，而其原點是左下角。 如果 **biHeight** 是負數，則點陣圖是由上而下的 DIB，而其原點是左上角。 如果 **biHeight** 是負的，表示由上而下的 DIB， **BICOMPRESSION** 必須是 bi \_ RGB 或 bi \_ 位欄位。 無法壓縮由上而下的 Dib。

</dd> <dt>

**biPlanes**
</dt> <dd>

指定目標裝置的平面數目。 此值必須設定為1。

</dd> <dt>

**biBitCount**
</dt> <dd>

指定每圖元的位數。 **BITMAPINFOHEADER** 結構的 **biBitCount** 成員會決定用來定義每個圖元的位數，以及點陣圖中的最大色彩數目。 此成員必須是下列值之一。



| 值 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | 點陣圖為單色，bmiColors 成員包含兩個專案。 點陣圖陣列中的每個位都代表一個圖元。 如果位為 clear，圖元就會顯示為 bmiColors 資料表中第一個專案的色彩;如果設定位，圖元就會有資料表中第二個專案的色彩。                                                                                                                                                                                                                                                                                                        |
| 2     | 點陣圖有四個可能的色彩值。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 4     | 點陣圖最多可有16個色彩，而 bmiColors 成員最多包含16個專案。 點陣圖中的每個圖元都會以4位索引表示在色彩資料表中。 例如，如果點陣圖中的第一個位元組是0x1F，則位元組代表兩個圖元。 第一個圖元包含第二個數據表專案中的色彩，而第二個圖元包含第十六個數據表專案中的色彩。                                                                                                                                                                                                                 |
| 8     | 點陣圖的最大值為256，而 bmiColors 成員最多包含256個專案。 在此情況下，陣列中的每個位元組都代表一個圖元。                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 16    | 點陣圖的最大值為 2 ^ 16 色。 如果 BITMAPINFOHEADER 的 biCompression 成員是 BI \_ RGB，則 bmiColors 成員為 **Null**。 點陣圖陣列中的每個單字都代表一個圖元。 紅色、綠色和藍色的相對濃度會以每個色彩元件的5位表示。 藍色的值是最不重要的5位，後面接著每個綠色和紅色的5位。 不會使用最重要的位。 BmiColors 色彩表可用來優化以調色板為基礎的裝置上使用的色彩，而且必須包含 biClrUsed 成員所指定的專案數。 |
| 24    | 點陣圖最多可有 2 ^ 24 個色彩，而 bmiColors 成員為 **Null**。 點陣圖陣列中的每個三位元組三位元組分別代表一個圖元的藍色、綠色和紅色的相對濃度。 BmiColors 色彩表可用來優化以調色板為基礎的裝置上使用的色彩，而且必須包含 biClrUsed 成員所指定的專案數。                                                                                                                                                                                                                                     |
| 32    | 點陣圖最多有 2 ^ 32 個色彩。 如果 biCompression 成員是 BI \_ RGB，bmiColors 成員就會是 **Null**。 點陣圖陣列中的每個 DWORD 分別代表藍色、綠色和紅色的相對濃度（圖元）。 不會使用每個 DWORD 的最高位元組。 BmiColors 色彩表可用來優化以調色板為基礎的裝置上使用的色彩，而且必須包含 biClrUsed 成員所指定的專案數。                                                                                                                                                                 |



 

</dd> <dt>

**biCompression**
</dt> <dd>

指定壓縮的下點陣圖壓縮類型 (由上而下的 Dib 無法壓縮) 。 這個成員可以是下列其中一個值。



| 值         | 描述                                                                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BI \_ RGB       | 未壓縮的格式。                                                                                                                                                                                                                                                                                            |
| BI \_ 位欄位 | 指定不壓縮點陣圖，而色彩表包含三個 DWORD 色遮罩，分別指定每個圖元的紅色、綠色和藍色元件。 這在搭配使用 16 bpp 和 32-bpp 點陣圖時有效。 在 Microsoft Windows CE 2.0 版和更新版本中，此值是有效的。 |



 

</dd> <dt>

**biSizeImage**
</dt> <dd>

指定影像的大小（以位元組為單位）。 對於 BI RGB 點陣圖，這可以設為零 \_ 。

</dd> <dt>

**biXPelsPerMeter**
</dt> <dd>

指定點陣圖目標裝置的水準解析度（以圖元為單位）。 應用程式可以使用此值從最符合目前裝置特性的資源群組中選取點陣圖。

</dd> <dt>

**biYPelsPerMeter**
</dt> <dd>

為點陣圖的目標裝置指定垂直解析度（以圖元為單位）。

</dd> <dt>

**biClrUsed**
</dt> <dd>

指定點陣圖實際使用之色彩表中的色彩索引數目。 如果這個值為零，則點陣圖會使用與 **biCompression** 所指定之壓縮模式的 **biBitCount** 成員值相對應的最大色彩數目。

</dd> <dt>

**biClrImportant**
</dt> <dd>

指定顯示點陣圖所需的色彩索引數目。 如果此值為零，則需要所有色彩。

如果 biClrUsed 為非零值，且 biBitCount 成員小於16，則 biClrUsed 成員會指定圖形引擎或設備磁碟機所存取的實際色彩數目。 如果 biBitCount 為16或更大，biClrUsed 成員會指定色彩表的大小，用來將系統調色板的效能優化。 如果 biBitCount 等於16或32，最佳色彩選擇區會緊接在三個 DWORD 遮罩之後開始。

如果點陣圖是封裝點陣圖 (點陣圖陣列會緊接在 \_ BITMAPINFOHEADER 結構之後，且由單一指標) 參考，則 biClrUsed 成員必須是零或色彩表的實際大小。

</dd> </dl>

## <a name="remarks"></a>備註

此結構包含在 **\_ VIDEOINFOHEADER** 結構中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdm .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構**](structures.md)
</dt> <dt>

[**\_VIDEOINFOHEADER**](-videoinfoheader.md)
</dt> </dl>

 

 





