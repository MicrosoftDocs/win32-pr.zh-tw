---
title: 'EM_GETTOUCHOPTIONS 訊息 (Richedit .h) '
description: 抓取與 rich edit 控制項相關聯的觸控選項。
ms.assetid: 1D367818-5625-4A5A-A7A1-330FED516990
keywords:
- EM_GETTOUCHOPTIONS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812d37de1972c6da205944d9913dc3fa046c205d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025335"
---
# <a name="em_gettouchoptions-message"></a>EM \_ GETTOUCHOPTIONS 訊息

抓取與 rich edit 控制項相關聯的觸控選項。


```C++
#define EM_GETTOUCHOPTIONS       (WM_USER + 310)
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要取出的觸控選項。 它可以是下列值之一。



| 值                                                                                                                                                                        | 意義                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <dt>**RTO \_ SHOWHANDLES**</dt> </dl>          | 抓取觸控 grippers 是否可見。<br/> |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <dt>**RTO \_ DISABLEHANDLES**</dt> </dl> | 未執行此旗標的抓取。<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 *wParam* 參數所指定之選項的值。 如果 *wParam* 是 **RTO \_ SHOWHANDLES** 且觸控 grippers 可見則為非零，否則為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ SETTOUCHOPTIONS**](em-settouchoptions.md)
</dt> </dl>

 

 





