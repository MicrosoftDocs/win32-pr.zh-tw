---
title: 'PBM_SETMARQUEE 訊息 (Commctrl .h) '
description: 設定捲軸模式的進度列。 這會使進度列像字幕一樣移動。
ms.assetid: 6501bcb9-a711-470f-874f-f3484d3613b6
keywords:
- PBM_SETMARQUEE message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_SETMARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9229291113f034924cf9ce8112c0e99376d37932
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934719"
---
# <a name="pbm_setmarquee-message"></a>PBM \_ SETMARQUEE 訊息

設定捲軸模式的進度列。 這會使進度列像字幕一樣移動。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指出是否開啟或關閉滾動字幕模式。

</dd> <dt>

*lParam* 
</dt> <dd>字幕動畫更新之間的時間（以毫秒為單位）。 如果此參數為零，則會每隔30毫秒更新字幕動畫。</dd> </dl>

## <a name="return-value"></a>傳回值

一律傳回 **TRUE**。

## <a name="remarks"></a>備註

如果您不知道要完成的進度量，但想要指出正在進行的進度，請使用此訊息。

傳送 **PBM \_ SETMARQUEE** 訊息以啟動或停止動畫。

> [!Note]  
> 您必須在嘗試開始動畫之前，將控制項樣式設定為 [**PBS \_ 字幕**](progress-bar-control-styles.md) 。

 

> [!Note]  
> 此訊息需要 ComCtl32.dll 6.00 版或更新版本。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





