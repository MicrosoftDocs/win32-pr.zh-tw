---
title: 'WINBIO_PRESENCE_PROPERTIES 聯集 (Winbio \_ 類型 .h) '
description: 包含 Windows 生物特徵辨識架構用來判斷是否有個人的生物特徵辨識值。
ms.assetid: 596CAA7F-35D2-442A-8041-BA1010DF5BAD
keywords:
- WINBIO_PRESENCE_PROPERTIES 聯集 Windows 生物特徵辨識架構 API
- PWINBIO_PRESENCE_PROPERTIES 聯集指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_PROPERTIES
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0568008b870953c34205706acc90cb22a2c0e92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464605"
---
# <a name="winbio_presence_properties-union"></a>WINBIO \_ 狀態 \_ 屬性聯集

包含 Windows 生物特徵辨識架構用來判斷是否有個人的生物特徵辨識值。

## <a name="syntax"></a>語法


```C++
typedef union _WINBIO_PRESENCE_PROPERTIES {
  struct {
    RECT BoundingBox;
    LONG Distance;
  } FacialFeatures;
  struct {
    RECT  EyeBoundingBox_1;
    RECT  EyeBoundingBox_2;
    POINT PupilCenter_1;
    POINT PupilCenter_2;
    LONG  Distance;
  } Iris;
} WINBIO_PRESENCE_PROPERTIES, *PWINBIO_PRESENCE_PROPERTIES;
```



## <a name="members"></a>成員

<dl> <dt>

**FacialFeatures**
</dt> <dd>

Windows 生物特徵辨識架構用來判斷是否有個人的臉部特徵位置值。

<dl> <dt>

**BoundingBox**
</dt> <dd>

以圖元為單位之臉部的相機框架內的位置。 相機框架的大小會決定這個位置的圖元數上限。 取得 [ **WINBIO \_ 屬性 \_ 擴充 \_ 感應器 \_ 資訊** ] 屬性，以決定相機框架的大小。 使用狀態監視器的用戶端必須執行調整作業，以將位置對應至相機框架。

</dd> <dt>

**距離**
</dt> <dd>

臉部的實際位置與臉部的理想焦距之間的距離。 此值範圍從-100 到100。 0表示理想的距離，正值表示臉部的實際位置太遠，負值表示實際位置太近。

</dd> </dl> </dd> <dt>

**虹膜**
</dt> <dd>

Windows 生物特徵辨識架構用來判斷是否有個人的鳶尾花位置值。

<dl> <dt>

**EyeBoundingBox \_ 1**
</dt> <dd>

要註冊之個人 irises 的相機框架內的位置（以圖元為單位）。 如果鳶尾花辨識系統只監視一眼，這個位置就是該眼睛的鳶尾花。 如果鳶尾花辨識系統同時監視這兩眼，但攝影機框架中只會有一眼，這個位置就是相機框架中的眼睛鳶尾花。 如果鳶尾花辨識系統同時監視這兩個眼睛，而兩個眼睛都在攝影機框架中，則這個位置可能是個人的正確眼睛鳶尾花。

相機框架的大小會決定這個位置的圖元數上限。 取得 [ **WINBIO \_ 屬性 \_ 擴充 \_ 感應器 \_ 資訊** ] 屬性，以決定相機框架的大小。 使用狀態監視器的用戶端必須執行調整作業，以將位置對應至相機框架。

</dd> <dt>

**EyeBoundingBox \_ 2**
</dt> <dd>

要註冊之個人 irises 的相機框架內的位置（以圖元為單位）。 如果鳶尾花辨識系統只監視一眼，或是攝影機框架中只有一眼，則這個值是空的。 如果鳶尾花辨識系統同時監視這兩眼，而兩眼都在攝影機框架中，則這個位置可能是個人的最左邊鳶尾花。

相機框架的大小會決定這個位置的圖元數上限。 取得 [ **WINBIO \_ 屬性 \_ 擴充 \_ 感應器 \_ 資訊** ] 屬性，以決定相機框架的大小。 使用狀態監視器的用戶端必須執行調整作業，以將位置對應至相機框架。

</dd> <dt>

**PupilCenter \_ 1**
</dt> <dd>

要註冊之個人的其中一個瞳孔中心位置。 如果鳶尾花辨識系統只監控一眼，這個位置就是該眼睛小學生的中心。 如果鳶尾花辨識系統同時監視這兩種情況，但攝影機框架中只會有一眼，這個位置就是相機框架中的眼睛小學生中心。 如果鳶尾花辨識系統同時監視這兩眼，而兩眼都在攝影機框架中，則這個位置可能是個人的適當眼睛小學生中心。

</dd> <dt>

**PupilCenter \_ 2**
</dt> <dd>

要註冊之個人的其中一個瞳孔中心位置。 如果鳶尾花辨識系統只監視一眼，或是攝影機框架中只有一眼，則這個值是空的。 如果鳶尾花辨識系統同時監視這兩眼，而兩眼都在攝影機框架中，則這個位置可能是個人左側的小學生中心。

</dd> <dt>

**距離**
</dt> <dd>

鳶尾花的實際位置與鳶尾花的理想焦距距離之間的距離。 此值範圍從-100 到100。 0表示理想的距離，正值表示鳶尾花的實際位置太遠，負值則表示實際位置太近。

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                                                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt> </dl> |



 

 





