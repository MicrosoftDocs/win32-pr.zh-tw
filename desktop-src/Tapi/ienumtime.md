---
description: IEnumTime 介面會為 ITTime 介面提供 COM 標準的列舉方法。 ITTimeCollection：： get \_ EnumerationIf 方法會將指標傳回至 IEnumTime。
ms.assetid: 395d7830-9a70-473a-8a89-4b4db48d5774
title: 'IEnumTime 介面 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2336f435ec322694847c776ac92ade93e8791207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977745"
---
# <a name="ienumtime-interface"></a>IEnumTime 介面

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**IEnumTime** 介面會為 [**ITTIME**](ittime.md)介面提供 COM 標準的列舉方法。 [**ITTimeCollection：： get \_ EnumerationIf**](ittimecollection-get-enumerationif.md)方法會將指標傳回至 **IEnumTime**。

## <a name="members"></a>成員

**IEnumTime** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IEnumTime** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IEnumTime** 介面具有這些方法。



| 方法                           | 描述                                                                                        |
|:---------------------------------|:---------------------------------------------------------------------------------------------------|
| [**克隆**](ienumtime-clone.md) | 建立另一個列舉值，其包含與目前列舉值相同的列舉型別狀態。<br/> |
| [**下一步**](ienumtime-next.md)   | 取得列舉順序中的下一個指定元素數目。<br/>                 |
| [**重設**](ienumtime-reset.md) | 重設為列舉序列的開頭。<br/>                                    |
| [**跳過**](ienumtime-skip.md)   | 略過列舉順序中的下一個指定元素數目。<br/>           |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

