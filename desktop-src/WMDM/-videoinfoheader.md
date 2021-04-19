---
title: _VIDEOINFOHEADER 結構
description: '\_VIDEOINFOHEADER 結構包含影片串流的相關資訊，並包含 \_ 定義個別框架格式的 BITMAPINFOHEADER 結構。'
ms.assetid: 5a39d66e-8dbc-4572-8370-14f722b6c906
keywords:
- _VIDEOINFOHEADER 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- _VIDEOINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5b389c5c82296e95ecfb3900518af4a2c7ddd7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982264"
---
# <a name="_videoinfoheader-structure"></a>\_VIDEOINFOHEADER 結構

**\_ VIDEOINFOHEADER** 結構包含影片串流的相關資訊，並包含定義個別框架格式的 **\_ BITMAPINFOHEADER** 結構。

## <a name="syntax"></a>語法


```C++
typedef struct _tagVIDEOINFOHEADER {
  RECT             rcSource;
  RECT             rcTarget;
  DWORD            dwBitRate;
  DWORD            dwBitErrorRate;
  REFERENCE_TIME   AvgTimePerFrame;
  BITMAPINFOHEADER bmiHeader;
} _VIDEOINFOHEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**rcSource**
</dt> <dd>

指定來源影片視窗的 **RECT** 結構。

</dd> <dt>

**rcTarget**
</dt> <dd>

指定目的地影片視窗的 **RECT** 結構。

</dd> <dt>

**dwBitRate**
</dt> <dd>

**DWORD** 值，指定影片串流的近似資料速率（以位/秒為單位）。

</dd> <dt>

**dwBitErrorRate**
</dt> <dd>

**DWORD** 值，指定影片資料流程的資料錯誤率，以每秒的位錯誤表示。

</dd> <dt>

**AvgTimePerFrame**
</dt> <dd>

**參考 \_時間** 值，指定影片框架的平均顯示時間，以 100-毫微秒單位表示。

</dd> <dt>

**bmiHeader**
</dt> <dd>

Win32 **\_ BITMAPINFOHEADER** 結構，其中包含影片影像點陣圖的色彩和維度資訊。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdm .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_BITMAPINFOHEADER**](-bitmapinfoheader.md)
</dt> <dt>

[**結構**](structures.md)
</dt> </dl>

 

 





