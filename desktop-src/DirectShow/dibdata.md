---
description: DIBDATA 結構包含與 GDI 裝置無關的點陣圖 (DIB) 的相關資訊。
ms.assetid: abbfa5b4-8789-4a44-a467-5812d3cc8238
title: 'DIBDATA 結構 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIBDATA
api_type:
- HeaderDef
api_location:
- Winutil.h
ms.openlocfilehash: 87590013ef905ffbdd13dd3b767435a907b08783
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985784"
---
# <a name="dibdata-structure"></a>DIBDATA 結構

此 `DIBDATA` 結構包含與 GDI 裝置無關的點陣圖 (DIB) 的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct tagDIBDATA {
  LONG       PaletteVersion;
  DIBSECTION DibSection;
  HBITMAP    hBitmap;
  HANDLE     hMapping;
  BYTE       *pBase;
} DIBDATA;
```



## <a name="members"></a>成員

<dl> <dt>

**PaletteVersion**
</dt> <dd>

每當選擇區變更時，此成員應該遞增。

</dd> <dt>

**DibSection**
</dt> <dd>

**DIBSECTION** 結構，其中包含 DIB 的相關資訊。 請參閱 GDI 檔以取得詳細資料。

</dd> <dt>

**hBitmap**
</dt> <dd>

點陣圖的控制碼。

</dd> <dt>

**hMapping**
</dt> <dd>

檔案對應物件的控制碼，這個物件是用來共用 GDI 與 [**CImageSample**](cimagesample.md) 物件之間的記憶體。

</dd> <dt>

**pBase**
</dt> <dd>

點陣圖的位址。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Winutil (包含： .h) </dt> </dl> |



 

 




