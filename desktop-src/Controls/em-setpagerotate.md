---
title: 'EM_SETPAGEROTATE 訊息 (Richedit .h) '
description: 設定 rich edit 控制項的文字版面配置。
ms.assetid: 3c2a37fe-ee9f-4b34-87bf-7ac27d010afc
keywords:
- EM_SETPAGEROTATE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETPAGEROTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eb595456bca444c92b536b0e428ee56a5903ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934275"
---
# <a name="em_setpagerotate-message"></a>EM \_ SETPAGEROTATE 訊息

\[**EM \_SETPAGEROTATE** 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。\]

設定 rich edit 控制項的文字版面配置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

文字版面配置值。 這可以是下列其中一個值。



| 值                                                                                                                                       | 意義                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="EPR_0"></span><span id="epr_0"></span><dl> <dt>**EPR \_ 0**</dt> </dl>       | 文字會從左至右，以及從上到下。<br/>                              |
| <span id="EPR_90"></span><span id="epr_90"></span><dl> <dt>**EPR \_ 90**</dt> </dl>    | 文字會從下到上，從左至右流動。<br/>                              |
| <span id="EPR_180"></span><span id="epr_180"></span><dl> <dt>**EPR \_ 180**</dt> </dl> | 文字會從右至左，從下到上流動。<br/>                              |
| <span id="EPR_270"></span><span id="epr_270"></span><dl> <dt>**EPR \_ 270**</dt> </dl> | 文字會從上到下，從右至左流動。<br/>                              |
| <span id="EPR_SE"></span><span id="epr_se"></span><dl> <dt>**EPR \_ SE**</dt> </dl>    | **Windows 8：** 文字流程由上到下，由左至右 (蒙古文字配置) 。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是新的文字版面配置值。

## <a name="remarks"></a>備註

這則訊息會設定整份檔的文字版面配置。 不過，內嵌的內容不會旋轉，且必須由應用程式分開旋轉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP1） \[ 桌面應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ GETPAGEROTATE**](em-getpagerotate.md)
</dt> </dl>

 

 





