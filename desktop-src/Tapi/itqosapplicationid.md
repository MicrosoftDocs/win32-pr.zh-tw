---
description: ITQOSApplicationID 介面會公開方法，讓應用程式取得目前呼叫的 QOS 識別碼。
ms.assetid: 1df50b3a-bd16-4e9b-afca-b025bfe537a4
title: 'ITQOSApplicationID 介面 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23df8da80798cc52ecd73b4f29288812f3774d9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993680"
---
# <a name="itqosapplicationid-interface"></a>ITQOSApplicationID 介面

\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用此介面。 RTC 用戶端 API 提供類似的功能。\]

**ITQOSApplicationID** 介面會公開方法，讓應用程式取得目前呼叫的 QOS 識別碼。

此介面是由 [IPCONF MSP](ipconf-msp.md) 所執行，而且只會在呼叫使用 IP 會議時公開。

## <a name="members"></a>成員

**ITQOSApplicationID** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ITQOSApplicationID** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITQOSApplicationID** 介面具有這些方法。



| 方法                                                                | 描述                         |
|:----------------------------------------------------------------------|:------------------------------------|
| [**SetQOSApplicationID**](itqosapplicationid-setqosapplicationid.md) | 設定 QOS 識別碼。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3。1<br/>                                                         |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

