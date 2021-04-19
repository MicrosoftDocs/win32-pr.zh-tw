---
title: Direct2D 常數
description: Direct2D 會定義下列常數清單。
ms.assetid: 98a443af-4bb7-486d-bc87-ff34c3671bdd
topic_type:
- apiref
api_name:
- D2D1_APPEND_ALIGNED_ELEMENT
- D2D1_DEFAULT_FLATTENING_TOLERANCE
- D2D1_INVALID_PROPERTY_INDEX
- D2D1_INVALID_TAG
- D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL
api_location:
- d2d1.h
- d2d1effects_2.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 09/19/2019
ms.openlocfilehash: bc25bf1055b923a383fc580a622e96d787ed13e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969994"
---
# <a name="direct2d-constants"></a>Direct2D 常數

下列常數是在 `d2d1effectauthor.h` 、 `d2d1.h` 、 `d2d1_1.h` 和 `d2d1effects_2.h` 標頭檔中宣告的。

## <a name="d2d1_append_aligned_element--1"></a>D2D1_APPEND_ALIGNED_ELEMENT (-1) 
在封裝輸入配置元素時使用。 它指出元素必須連續封裝。

## <a name="d2d1_default_flattening_tolerance-025f"></a>D2D1_DEFAULT_FLATTENING_TOLERANCE (0.25 f) 
幾何壓平合併作業的預設容錯。

## <a name="d2d1_invalid_property_index-uint_max"></a>D2D1_INVALID_PROPERTY_INDEX (UINT_MAX) 
定義不正確屬性索引。

從 [**ID2D1Properties：： GetPropertyIndex**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) 傳回這個常數，表示您提供的命名屬性在屬性介面中沒有索引。

如果您將這個常數傳遞給 [**ID2D1Properties：： GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) 或 [**ID2D1Properties：： GetValueByName**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32))，則呼叫會失敗，而且輸出緩衝區會填入零。

## <a name="d2d1_invalid_tag-ulonglong_max"></a>D2D1_INVALID_TAG (ULONGLONG_MAX) 
保護請勿使用。

## <a name="d2d1_scene_referred_sdr_white_level-800f"></a>D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80.0 f) 
SRGB 或 scRGB 色彩空間用於 SDR 白色或 1.0 f 浮點值的 nits 數目。 只有當色彩空間使用場景參考的亮度時，此值才會是常數， (HDR) 內容的高度動態範圍則為 true。 如果色彩空間改為使用顯示參考的亮度，則應該從顯示中查詢 SDR 白色層級。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 最低支援的用戶端 | Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\] |
| 最低支援的伺服器 | Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\] |
| 支援的最小電話 | Windows Phone 8.1 \[ Windows Phone silverlight 8.1 和 Windows 執行階段應用程式 \] ，Windows Phone 8.1 \[ Windows Phone silverlight 8.1 和 Windows 執行階段應用程式\] |
| 標頭 | d2d1effectauthor .h、d2d1 .h、d2d1_1 .h、d2d1effects_2。h |
