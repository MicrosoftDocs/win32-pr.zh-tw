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
ms.openlocfilehash: 969eb389a1216ec0e30f27a938ca4f5382397ac5489f87add87731b69824b87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100652"
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
| IDL<br/> | <dl> <dt>Windows。 (參考 Windows 的參考。) 的串流 .idl</dt> </dl> |



 

 





