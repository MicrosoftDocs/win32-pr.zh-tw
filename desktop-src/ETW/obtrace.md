---
description: 代表所有物件管理員事件追蹤類別衍生來源的父類別。
ms.assetid: 07cfc4a2-c665-4080-bc4b-fe9ec7191fdc
title: ObTrace 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTrace
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8cf30fe0c7b028c819477bcf0c66c2b674fc588286916be1cd1fd1a6b207770d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328748"
---
# <a name="obtrace-class"></a>ObTrace 類別

代表所有物件管理員事件追蹤類別衍生來源的父類別。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[DisplayName("Object"), Dynamic, EventVersion(2), Guid("{89497f50-effe-4440-8cf2-ce6b1cdcaca7}")]
class ObTrace : MSNT_SystemTrace
{
};
```

## <a name="members"></a>成員

**ObTrace** 類別不會定義任何成員。

## <a name="remarks"></a>備註

若要啟用物件管理員事件追蹤，請呼叫 [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) 函數，並將 *InformationClass* 參數等於 [**追蹤 \_ 資訊 \_ 類別**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) 列舉值 **TraceSystemTraceEnableFlagsInfo** ，且 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) 結構的 **EnableFlags** 成員等於效能 **\_ OB \_ 控制碼** (0x80000040) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Wmicore mof</dt> </dl> |



 

 
