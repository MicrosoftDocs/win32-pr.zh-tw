---
description: ITTimeCollection 介面是會話描述項通訊協定 (SDP) 會議 blob 物件的提供者特定介面。
ms.assetid: 6309e9f2-8a73-4d42-ae0a-2165352d6244
title: 'ITTimeCollection 介面 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19ca297a26b0eac34396726e6145a24fba5a2ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992570"
---
# <a name="ittimecollection-interface"></a>ITTimeCollection 介面

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**ITTimeCollection** 介面是會話描述項通訊協定 (SDP) 會議 blob 物件的提供者特定介面。 此介面可讓您依索引存取 [**ITTime**](ittime.md) 介面，也可讓您建立和刪除時間元件。 [**ITSdp：： get \_ TimeCollection**](itsdp-get-timecollection.md)方法會建立 **ITTimeCollection** 介面。

## <a name="members"></a>成員

**ITTimeCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ITTimeCollection** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITTimeCollection** 介面具有這些方法。



| 方法                                                           | 描述                                                                                                           |
|:-----------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**創建**](ittimecollection-create.md)                        | 建立 [**ITTime**](ittime.md) 元件。<br/>                                                             |
| [**刪除**](ittimecollection-delete.md)                        | 刪除 [**ITTime**](ittime.md) 元件。<br/>                                                             |
| [**取得 \_ \_ NewEnum**](ittimecollection-get--newenum.md)          | 傳回集合的列舉程式。<br/>                                                                  |
| [**取得 \_ 計數**](ittimecollection-get-count.md)                 | 取得集合中的專案數。<br/>                                                                        |
| [**取得 \_ EnumerationIf**](ittimecollection-get-enumerationif.md) | 傳回列舉 [**ITTime**](ittime.md)的 [**IEnumTime**](ienumtime.md)列舉介面。<br/> |
| [**取得 \_ 專案**](ittimecollection-get-item.md)                   | 指定索引之後，會傳回集合中的專案。<br/>                                                         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

