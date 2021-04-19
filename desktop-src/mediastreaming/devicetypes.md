---
title: DeviceTypes 列舉
description: 描述媒體串流 API 所支援的 DLNA 裝置類型。
ms.assetid: ec6bbc1f-653a-414c-b458-1a5e1b101781
keywords:
- DeviceTypes 列舉媒體串流 API
topic_type:
- apiref
api_name:
- DeviceTypes
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9caf60fa5736f9db442da5787746a49f71c61c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981868"
---
# <a name="devicetypes-enumeration"></a>DeviceTypes 列舉

描述媒體串流 API 所支援的 DLNA 裝置類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum DeviceTypes { 
  Unknown               = 0x0,
  DigitalMediaRenderer  = 0x1,
  DigitalMediaServer    = 0x2,
  DigitalMediaPlayer    = 0x4
} DeviceTypes;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知**
</dt> <dd>

未知的裝置類型。

</dd> <dt>

<span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**DigitalMediaRenderer**
</dt> <dd>

DLNA 數位媒體轉譯器 (DMR) 。 值相當於裝置類型 **urn：架構-upnp-org： device： MediaRenderer： 1**。

</dd> <dt>

<span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**DigitalMediaServer**
</dt> <dd>

 (DMS) 的 DLNA 數位媒體伺服器。 值相當於裝置類型 **urn：架構-upnp-org： device： MediaServer： 1**。

</dd> <dt>

<span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**DigitalMediaPlayer**
</dt> <dd>

DLNA 數位媒體播放機

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt> (參考) 的 windows...。 </dt> </dl> |



 

 





