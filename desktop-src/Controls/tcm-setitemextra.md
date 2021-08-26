---
title: 'TCM_SETITEMEXTRA 訊息 (Commctrl .h) '
description: 設定在索引標籤控制項中，為應用程式定義資料保留的每個索引標籤的位元組數目。 您可以使用 TabCtrl SetItemExtra 宏明確地傳送此訊息 \_ 。
ms.assetid: 8315f1fd-8eca-48bd-bb4a-71b09e8aa2c4
keywords:
- TCM_SETITEMEXTRA 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TCM_SETITEMEXTRA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f92fb85f7133053392bee39119c91b55240f84f0a51c8acc7dc9c732b596526c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104758"
---
# <a name="tcm_setitemextra-message"></a>TCM \_ SETITEMEXTRA 訊息

設定在索引標籤控制項中，為應用程式定義資料保留的每個索引標籤的位元組數目。 您可以使用 [**TabCtrl \_ SetItemExtra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

額外的位元組數目。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

根據預設，額外的位元組數目為四。 變更額外位元組數目的應用程式無法使用 [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) 結構來取得和設定索引標籤的應用程式定義資料。相反地，您必須定義由 [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) 結構組成的新結構，後面接著應用程式定義的成員。

應用程式應該只在索引標籤控制項未包含任何索引標籤時，變更額外的位元組數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





