---
description: 這個類別是分割 IO 事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: d65c5180-6f1a-45cc-bca8-eac13857d383
title: SplitIo 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0268c3dfa778eb8694a81f57b9212b68bd6674e6c7de6324cdc297550745b2a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069718"
---
# <a name="splitio-class"></a>SplitIo 類別

這個類別是分割 IO 事件的父類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[Guid("{d837ca92-12b9-44a5-ad6a-3a65b3578aa8}")]
class SplitIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>成員

**SplitIo** 類別不會定義任何成員。

## <a name="remarks"></a>備註

若要在 NT 核心記錄會話中啟用分割 IO 事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ 分割 \_ io** 旗標。

事件追蹤取用者可以呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式，並將 [**SplitIoGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，以針對分割 IO 事件執行特殊處理。 使用下列事件種類來識別使用事件時的實際事件。



| 事件類型           | 描述                                                                                                |
|----------------------|------------------------------------------------------------------------------------------------------------|
| 事件種類值，32 | 分割 IO 事件。 [**SplitIo \_ 資訊**](splitio-info.md)MOF 類別會定義此事件的事件資料。 |



 

分割 IO 事件表示因為基礎鏡像磁片硬體，IO 要求已分割成多個磁片 IO 要求。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



 

 
