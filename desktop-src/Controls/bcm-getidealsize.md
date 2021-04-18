---
title: 'BCM_GETIDEALSIZE 訊息 (Commctrl .h) '
description: 取得最適合其文字和影像的按鈕大小（如果有影像清單）。 您可以明確地傳送此訊息，或使用按鈕 \_ GetIdealSize 宏。
ms.assetid: c1bc2043-bf1a-4129-a005-f04048c4c1db
keywords:
- BCM_GETIDEALSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- BCM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446f4acba39b8b9722ef1a01a223f671b56ae845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965715"
---
# <a name="bcm_getidealsize-message"></a>BCM \_ GETIDEALSIZE 訊息

取得最適合其文字和影像的按鈕大小（如果有影像清單）。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**大小**](/previous-versions//dd145106(v=vs.85))結構的指標，該結構會接收所需的按鈕大小，包括文字和影像清單（如果有的話）。 呼叫應用程式負責配置此結構。 將 **cx** 和 **cy** 成員設定為零，以在 **大小** 結構中傳回理想的高度和寬度。 若要指定按鈕寬度，請將 **cx** 成員設定為所需的按鈕寬度。 系統會計算此寬度的理想高度，並將其傳回至 **cy** 成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則會傳回 **TRUE**。 否則會傳回 **FALSE**。

## <a name="remarks"></a>備註

> [!Note]  
> 如果您不想要任何特殊的按鈕寬度，則必須將 [**大小**](/previous-versions//dd145106(v=vs.85)) 的成員設定為零，以計算並傳回理想的高度和寬度。 如果 **cx** 成員的值大於零，則會將這個值視為所需的按鈕寬度，並計算此寬度的理想高度，並在 **cy** 成員中傳回。

 

這則訊息最適用于按鈕。 傳送至按鈕時，訊息會抓取顯示按鈕文字所需的周框。 此外，如果按鈕具有影像清單，周框也會調整大小以包含按鈕的影像。

傳送至任何其他類型的按鈕時，會抓取控制項的視窗矩形大小。

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

