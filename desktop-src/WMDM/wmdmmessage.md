---
title: WMDMMessage 列舉
description: WMDMMessage 列舉型別會定義訊息類型和狀態。
ms.assetid: 49a77100-8890-4e40-852f-c6fd436f22c5
keywords:
- WMDMMessage 列舉 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDMMessage
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7489dc7059f10e1a6f61d1a290f8f664a385f96c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977419"
---
# <a name="wmdmmessage-enumeration"></a>WMDMMessage 列舉

**WMDMMessage** 列舉型別會定義訊息類型和狀態。

## <a name="syntax"></a>Syntax


```C++
enum WMDMMessage {
  WMDM_MSG_DEVICE_ARRIVAL, 
  WMDM_MSG_DEVICE_REMOVAL, 
  WMDM_MSG_MEDIA_ARRIVAL, 
  WMDM_MSG_MEDIA_REMOVAL 

};
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**WMDM \_ MSG \_ 裝置 \_ 抵達**
</dt> <dd>

已插入 Windows Media 裝置管理員裝置。

</dd> <dt>

<span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**WMDM \_ MSG \_ 裝置 \_ 移除**
</dt> <dd>

Windows Media 裝置管理員裝置已移除。

</dd> <dt>

<span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**WMDM \_ MSG \_ 媒體 \_ 抵達**
</dt> <dd>

媒體已插入 Windows Media 裝置管理員裝置。

</dd> <dt>

<span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**WMDM \_ MSG \_ 媒體 \_ 移除**
</dt> <dd>

媒體已從 Windows Media 裝置管理員裝置中移除。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdm .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**列舉類型**](enumeration-types.md)
</dt> </dl>

 

 





