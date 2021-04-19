---
title: TransportState 列舉
description: 定義 UPnP 指導方針所定義的可用傳輸狀態。
ms.assetid: 2F942EAC-514B-4E65-A12F-85558E9A96A0
keywords:
- TransportState 列舉媒體串流 API
topic_type:
- apiref
api_name:
- TransportState
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 865d7e0f6a96727915833bb402860cde661162f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984437"
---
# <a name="transportstate-enumeration"></a>TransportState 列舉

定義 UPnP 指導方針所定義的可用傳輸狀態。

## <a name="syntax"></a>Syntax


```C++
typedef enum _TransportState { 
  Unknown         = 0,
  Stopped         = 1,
  Playing         = 2,
  Transitioning   = 3,
  Paused          = 4,
  Recording       = 5,
  NoMediaPresent  = 6,
  Last            = 7
} TransportState;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知**
</dt> <dd>

錯誤的裝置狀態。

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**停止**
</dt> <dd>

裝置 s 傳輸處於停止狀態。

</dd> <dt>

<span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**玩**
</dt> <dd>

裝置的傳輸狀態為「現正播放」。

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**過渡**
</dt> <dd>

裝置的傳輸處於轉換狀態，這會產生另一個狀態值。

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**暫停**
</dt> <dd>

裝置 s 傳輸處於暫停狀態。

</dd> <dt>

<span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**記錄**
</dt> <dd>

裝置 s 傳輸處於錄製狀態。

</dd> <dt>

<span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**NoMediaPresent**
</dt> <dd>

裝置的傳輸沒有針對播放設定的 URI。

</dd> <dt>

<span id="Last"></span><span id="last"></span><span id="LAST"></span>**最後**
</dt> <dd>

裝置的先前狀態設為目前的傳輸狀態。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt> (參考) 的 windows...。 </dt> </dl> |



 

 





