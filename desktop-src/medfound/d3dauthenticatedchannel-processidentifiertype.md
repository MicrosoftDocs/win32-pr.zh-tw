---
description: 指定 D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS 輸出結構中所識別的進程類型 \_ 。
ms.assetid: 8878905e-f55b-4dbc-9608-da0082daf673
title: 'D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE 列舉 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 522fee8421ec61b58bd67065c31b968252c2c7d563e94f7eda7a9f5105d20382
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061978"
---
# <a name="d3dauthenticatedchannel_processidentifiertype-enumeration"></a>D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE 列舉

指定 [**D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ 輸出**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) 結構中所識別的進程類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  PROCESSIDTYPE_UNKNOWN  = 0,
  PROCESSIDTYPE_DWM      = 1,
  PROCESSIDTYPE_HANDLE   = 2
} D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**PROCESSIDTYPE \_ 不明**
</dt> <dd>

未知的進程類型。

</dd> <dt>

<span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**PROCESSIDTYPE \_ DWM**
</dt> <dd>

桌面視窗管理員 (DWM) 進程。

</dd> <dt>

<span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**PROCESSIDTYPE \_ 控制碼**
</dt> <dd>

處理常式的控制碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                 |
| 標頭<br/>                   | <dl> <dt>D3d9types (包含 D3d9) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 影片列舉](direct3d-video-enumerations.md)
</dt> </dl>

 

 




