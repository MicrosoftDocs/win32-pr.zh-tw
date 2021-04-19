---
description: ITTime 介面是會話描述項通訊協定 (SDP) 會議 blob 物件的提供者特定介面。
ms.assetid: 24d33259-dcbe-47e4-9c71-fcc25f6e9a76
title: 'ITTime 介面 (Sdpblb .h) '
ms.topic: interface
ms.date: 05/31/2018
ms.openlocfilehash: 964fa197318d8cbe9614beb97c5bea0db94f242b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995258"
---
# <a name="ittime-interface"></a>ITTime 介面

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**ITTime** 介面是會話描述項通訊協定 (SDP) 會議 blob 物件的提供者特定介面。 它可讓您存取會話的一組啟用時間。 [**IEnumTime：： Next**](ienumtime-next.md)和 [**ITTimeCollection：： create**](ittimecollection-create.md)方法會建立 **ITTime** 介面。

## <a name="members"></a>成員

**ITTime** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ITTime** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITTime** 介面具有這些方法。



| 方法                                         | 描述                                                                 |
|:-----------------------------------------------|:----------------------------------------------------------------------------|
| [**取得 \_ StartTime**](ittime-get-starttime.md) | 取得32位 NTP (網路時間通訊協定) 開始時間值。<br/> |
| [**取得 \_ StopTime**](ittime-get-stoptime.md)   | 取得 NTP 結束時間值。<br/>                                  |
| [**put \_ StartTime**](ittime-put-starttime.md) | 設定32位 NTP 開始時間值。<br/>                         |
| [**put \_ StopTime**](ittime-put-stoptime.md)   | 設定 NTP 結束時間值。<br/>                                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

