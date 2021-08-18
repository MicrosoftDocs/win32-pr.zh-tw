---
description: ITMediaCollection 介面可讓您存取 SDP (RFC 2327) 會議描述中的一組媒體資訊。
ms.assetid: a7e7a07d-239e-432e-9984-7763f11c59ce
title: 'ITMediaCollection 介面 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2425ae89f376d5cb2d7cc23e70abd33f87750d3d1b5343a17c8ecb05d7de760d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034608"
---
# <a name="itmediacollection-interface"></a>ITMediaCollection 介面

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**ITMediaCollection** 介面可讓您存取 SDP (RFC 2327) 會議描述中的一組媒體資訊。 [**ITMedia**](itmedia.md)介面會描述 SDP 中的每個媒體描述。 **ITMediaCollection** 可讓您操作一組 SDP 的 **ITMedia** 資訊，包括：

-   允許依索引存取媒體。
-   啟用媒體的建立和刪除。

[**ITSdp：： get \_ MediaCollection**](itsdp-get-mediacollection.md)方法會建立 **ITMediaCollection** 介面。

## <a name="members"></a>成員

**ITMediaCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ITMediaCollection** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITMediaCollection** 介面具有這些方法。



| 方法                                                            | 描述                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**建立**](itmediacollection-create.md)                        | 使用預設屬性建立新的媒體，並將其傳回。<br/> |
| [**刪除**](itmediacollection-delete.md)                        | 刪除對應至指定之索引的媒體。<br/>     |
| [**取得 \_ \_ NewEnum**](itmediacollection-get--newenum.md)          | 傳回集合的列舉程式。<br/>                   |
| [**取得 \_ 計數**](itmediacollection-get-count.md)                 | 取得會話中的媒體數目。<br/>                    |
| [**取得 \_ EnumerationIf**](itmediacollection-get-enumerationif.md) | 取得列舉介面的指標。<br/>                      |
| [**取得 \_ 專案**](itmediacollection-get-item.md)                   | 傳回對應至指定之索引的媒體。<br/>     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

