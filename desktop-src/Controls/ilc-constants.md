---
title: '影像清單建立旗標 (Shlobj.h .h) '
description: 一組位旗標，指定要建立之影像清單的類型。 這個參數可以是下列值的組合，但只能包含其中一個 ILC.OUT 的 \_ 色彩值。 由 ImageList \_ Create 和 IImageList2 Initialize 使用。
ms.assetid: DFEB1934-DB7F-4151-97F9-DDB2BCCC782A
topic_type:
- apiref
api_name:
- ILC_MASK
- ILC_COLOR
- ILC_COLORDDB
- ILC_COLOR4
- ILC_COLOR8
- ILC_COLOR16
- ILC_COLOR24
- ILC_COLOR32
- ILC_PALETTE
- ILC_MIRROR
- ILC_PERITEMMIRROR
- ILC_ORIGINALSIZE
- ILC_HIGHQUALITYSCALE
api_location:
- Shlobj.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27f9a83c119b8e201ba41c002bf7c166ba3e4dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465041"
---
# <a name="image-list-creation-flags"></a>影像清單建立旗標

一組位旗標，指定要建立之影像清單的類型。 這個參數可以是下列值的組合，但只能包含其中一個 ILC.OUT 的 \_ 色彩值。 由 [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) 和 [**IImageList2：： Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize)使用。



| 常數/值                                                                                                                                                                                                                                     | Description                                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILC_MASK"></span><span id="ilc_mask"></span><dl> <dt>**Ilc.out \_MASK**</dt> <dt>0x00000001</dt> </dl>                                     | 使用遮罩。 影像清單包含兩個位圖，其中一個點陣圖是用來做為遮罩的單色點陣圖。 如果未包含此值，則影像清單只會包含一個點陣圖。<br/>      |
| <span id="ILC_COLOR"></span><span id="ilc_color"></span><dl> <dt>**Ilc.out \_色彩**</dt> <dt>0x00000000</dt> </dl>                                  | 如果未指定任何其他 ILC.OUT \_ COLORx 旗標，請使用預設行為。 一般而言，預設值是 ILC.OUT \_ COLOR4，但對於較舊的顯示器驅動程式，預設值為 Ilc.out \_ COLORDDB。<br/> |
| <span id="ILC_COLORDDB"></span><span id="ilc_colorddb"></span><dl> <dt>**Ilc.out \_COLORDDB**</dt> <dt>0x000000FE</dt> </dl>                         | 使用裝置相依的點陣圖。<br/>                                                                                                                                                    |
| <span id="ILC_COLOR4"></span><span id="ilc_color4"></span><dl> <dt>**Ilc.out \_COLOR4**</dt> <dt>0x00000004</dt> </dl>                               | 使用4位 (16 色) 裝置獨立點陣圖 (DIB) 區段作為影像清單的點陣圖。<br/>                                                                                  |
| <span id="ILC_COLOR8"></span><span id="ilc_color8"></span><dl> <dt>**Ilc.out \_COLOR8**</dt> <dt>0x00000008</dt> </dl>                               | 使用8位的 DIB 區段。 色彩表所使用的色彩與半色調調色板的色彩相同。<br/>                                                                        |
| <span id="ILC_COLOR16"></span><span id="ilc_color16"></span><dl> <dt>**Ilc.out \_COLOR16**</dt> <dt>0x00000010</dt> </dl>                            | 使用16位 (32/64k 色彩) DIB 區段。<br/>                                                                                                                                          |
| <span id="ILC_COLOR24"></span><span id="ilc_color24"></span><dl> <dt>**Ilc.out \_COLOR24**</dt> <dt>0x00000018</dt> </dl>                            | 使用24位的 DIB 區段。<br/>                                                                                                                                                         |
| <span id="ILC_COLOR32"></span><span id="ilc_color32"></span><dl> <dt>**Ilc.out \_COLOR32**</dt> <dt>0x00000020</dt> </dl>                            | 使用32位的 DIB 區段。<br/>                                                                                                                                                         |
| <span id="ILC_PALETTE"></span><span id="ilc_palette"></span><dl> <dt>**Ilc.out \_調色板**</dt> <dt>0x00000800</dt> </dl>                            | 未實作。<br/>                                                                                                                                                                  |
| <span id="ILC_MIRROR"></span><span id="ilc_mirror"></span><dl> <dt>**Ilc.out \_鏡像**</dt> <dt>0x00002000</dt> </dl>                               | 如果進程已鏡像，則鏡像包含的圖示<br/>                                                                                                                            |
| <span id="ILC_PERITEMMIRROR"></span><span id="ilc_peritemmirror"></span><dl> <dt>**Ilc.out \_PERITEMMIRROR**</dt> <dt>0x00008000</dt> </dl>          | 導致鏡像程式碼在插入一組影像（與整個區域）時，將每個專案鏡像。<br/>                                                                             |
| <span id="ILC_ORIGINALSIZE"></span><span id="ilc_originalsize"></span><dl> <dt>**Ilc.out \_ORIGINALSIZE**</dt> <dt>0x00010000</dt> </dl>             | **Windows Vista （含）以後版本。** Imagelist 應接受小於設定的影像，並根據新增的影像套用原始大小。<br/>                                                        |
| <span id="ILC_HIGHQUALITYSCALE"></span><span id="ilc_highqualityscale"></span><dl> <dt>**Ilc.out \_HIGHQUALITYSCALE**</dt> <dt>0x00020000</dt> </dl> | **Windows Vista （含）以後版本。** 保留的。<br/>                                                                                                                                            |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 





