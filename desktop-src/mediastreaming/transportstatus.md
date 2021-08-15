---
title: TransportStatus 列舉
description: 定義 UPnP 指導方針所定義的可用傳輸狀態。
ms.assetid: 6fde82f0-9bc4-4abb-9d10-0000501c2b24
keywords:
- TransportStatus 列舉媒體串流 API
topic_type:
- apiref
api_name:
- TransportStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96b7d3892d0344b166665426c66313da370aed1abbdb80c17037ea6aeb44e46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472994"
---
# <a name="transportstatus-enumeration"></a>TransportStatus 列舉

定義 UPnP 指導方針所定義的可用傳輸狀態。

## <a name="syntax"></a>Syntax


```C++
typedef enum TransportStatus { 
  Unknown        = 0,
  Ok             = 1,
  ErrorOccurred  = 2,
  Last           = 3
} TransportStatus;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知**
</dt> <dd>

錯誤的裝置狀態。

</dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>**還行**
</dt> <dd>

裝置處於良好狀態。

</dd> <dt>

<span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ErrorOccurred**
</dt> <dd>

裝置發生錯誤。

</dd> <dt>

<span id="Last"></span><span id="last"></span><span id="LAST"></span>**最後**
</dt> <dd>

裝置的先前狀態為目前的傳輸狀態。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Windows。 (參考 Windows 的參考。) 的串流 .idl</dt> </dl> |



 

 





