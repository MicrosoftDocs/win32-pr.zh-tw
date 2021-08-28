---
description: ITQOSApplicationID 介面會公開方法，讓應用程式取得目前呼叫的 QOS 識別碼。
ms.assetid: 1df50b3a-bd16-4e9b-afca-b025bfe537a4
title: 'ITQOSApplicationID 介面 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4067d7a476e2a402c278b22dcee21b6542919396178350e73017d56ba92258
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126278"
---
# <a name="itqosapplicationid-interface"></a>ITQOSApplicationID 介面

\[這個介面無法在 Windows Vista、Windows Server 2008 及後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

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



 

