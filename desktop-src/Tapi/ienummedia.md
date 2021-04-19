---
description: IEnumMedia 介面會為 ITMedia 介面提供 COM 標準的列舉方法。 ITMediaCollection：： get \_ EnumerationIf 方法會將指標傳回至 IEnumMedia。
ms.assetid: 827f8866-2445-4b7c-88fe-eed19f48c93b
title: 'IEnumMedia 介面 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7127e7d1d751ee487ad5b86326602cfcfe5aae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994886"
---
# <a name="ienummedia-interface"></a>IEnumMedia 介面

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**IEnumMedia** 介面會為 [**ITMEDIA**](itmedia.md)介面提供 COM 標準的列舉方法。 [**ITMediaCollection：： get \_ EnumerationIf**](itmediacollection-get-enumerationif.md)方法會將指標傳回至 **IEnumMedia**。

## <a name="members"></a>成員

**IEnumMedia** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IEnumMedia** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IEnumMedia** 介面具有這些方法。



| 方法                            | 描述                                                                                        |
|:----------------------------------|:---------------------------------------------------------------------------------------------------|
| [**克隆**](ienummedia-clone.md) | 建立另一個列舉值，其包含與目前列舉值相同的列舉型別狀態。<br/> |
| [**下一步**](ienummedia-next.md)   | 取得列舉順序中的下一個指定元素數目。<br/>                 |
| [**重設**](ienummedia-reset.md) | 重設為列舉序列的開頭。<br/>                                    |
| [**跳過**](ienummedia-skip.md)   | 略過列舉順序中的下一個指定元素數目。<br/>           |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

