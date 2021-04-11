---
title: ID2D1CommandSink1 SetPrimitiveBlend1 方法
description: 設定新的基本 blend 模式。
ms.assetid: 3EA9EC07-1B2F-48A2-ABFB-2DA0E2EFFBF4
keywords:
- SetPrimitiveBlend1 方法 Direct2D
- SetPrimitiveBlend1 方法 Direct2D、ID2D1CommandSink1 介面
- ID2D1CommandSink1 介面 Direct2D，SetPrimitiveBlend1 方法
topic_type:
- apiref
api_name:
- ID2D1CommandSink1.SetPrimitiveBlend1
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3aa961eec873cc84e5b34ce41279c09f580e63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094495"
---
# <a name="id2d1commandsink1setprimitiveblend1-method"></a>ID2D1CommandSink1：： SetPrimitiveBlend1 方法

設定新的基本 blend 模式。

## <a name="syntax"></a>語法


```C++
HRESULT SetPrimitiveBlend1(
   D2D1_PRIMITIVE_BLEND primitiveBlend
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*primitiveBlend* 
</dt> <dd>

類型： **[ **D2D1 \_ 基本 \_ BLEND**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**

將套用至後續基本專案的基本 blend。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果方法成功，它會傳回 **S \_ OK**。 如果失敗，則會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

### <a name="blend-modes"></a>Blend 模式

針對別名轉譯 (除了 MIN 模式) 之外，輸出值 O 是以線性方式將值 *blend (S，D)* 與目的地圖元值（根據原始物件涵蓋目的圖元的數量）來計算。

下表顯示別名和反鋸齒混合的基本 blend 模式。 表格中所列的方能使用下列元素：

-   O = 輸出
-   S = 來源
-   SA = 來源 Alpha
-   D = 目的地
-   DA = 目的地 Alpha
-   C = 圖元涵蓋範圍



| 基本 blend 模式                 | 鋸齒混合                            | 反鋸齒混合            | Description                                                                                                              |
|--------------------------------------|---------------------------------------------|---------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 基本 \_ BLEND \_ 來源 \_ | O = (S + (1 SA) \* D) \* C + D \* (1 C)  | O = S \* C + D \* (1 SA \* C)    | 標準來源 over 目的地 blend 模式。                                                                         |
| D2D1 \_ 基本 \_ BLEND \_ 複製         | O = S \* C + D \* (1 C)                    | O = S \* C + D \* (1 C)        | 來源會複製到目的地;系統會忽略目的地圖元。                                             |
| D2D1 \_ 基本 \_ BLEND \_ 分鐘          | O = Min (S + 1-SA，D)                         | O = Min (S \* c + 1 SA \* c，D)  | 產生的圖元值會使用來源和目的地圖元值的最小值。 在 Windows 8 和更新版本中提供。 |
| D2D1 \_ 基本 \_ BLEND \_ 新增          | O = (S + D) \* c + D \* (1 C)              | O = S \* C + D                  | 產生的圖元值是來源和目的地圖元值的總和。 在 Windows 8 和更新版本中提供。     |



 

![以不同的不透明度和背景 direct2d 基本 blend 模式的圖例。](images/primblenddemo.png)

具有不同透明度和背景的基本 blend 模式圖例。

除非使用 [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) API 上的 *compositeMode* 參數來覆寫此基本 blend，否則基本 blend 會套用至內容上繪製的所有基本型別。

基本 blend 適用于在內容上繪製之任何基本專案的內部。 在 [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode))的案例中，這將由影像矩形、位移和世界轉換來隱含。

如果基本 blend 是 **D2D1 \_ 基本 \_ blend \_** 以外的任何物件，則 ClearType 轉譯將會關閉。 如果應用程式在這些模式中明確強制執行 ClearType 轉譯，則繪製內容會處於錯誤狀態。 \_ \_ [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)或 [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)會傳回 D2DERR 錯誤的狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                          |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1CommandSink1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1commandsink1)
</dt> </dl>

 

