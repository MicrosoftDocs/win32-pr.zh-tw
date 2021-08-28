---
description: IEnumParticipant 介面會為 ITParticipant 介面提供 COM 標準的列舉方法。 ITParticipantControl：： EnumerateParticipants 方法會將指標傳回至 IEnumParticipant。
ms.assetid: 8534d102-06ce-4e82-8f9c-9ab9f0d14df9
title: 'IEnumParticipant 介面 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ba6deb232b03a7923c8ea47e9e200f3d3ea9beb5bddcd0572e3cac4c2b6269
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003576"
---
# <a name="ienumparticipant-interface"></a>IEnumParticipant 介面

\[**IEnumParticipant** 無法在 Windows Vista、Windows Server 2008 及後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**IEnumParticipant** 介面會為 [**ITPARTICIPANT**](itparticipant.md)介面提供 COM 標準的列舉方法。 [**ITParticipantControl：： EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md)方法會將指標傳回至 **IEnumParticipant**。

Visual Basic 和指令碼語言都隱藏了 **IEnumParticipant** 介面。

## <a name="members"></a>成員

**IEnumParticipant** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IEnumParticipant** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IEnumParticipant** 介面具有這些方法。



| 方法                                  | 描述                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**複製**](ienumparticipant-clone.md) | 建立另一個列舉值，其包含與目前列舉值相同的列舉型別狀態。<br/> |
| [**下一步**](ienumparticipant-next.md)   | 取得列舉順序中的下一個指定元素數目。<br/>                 |
| [**重設**](ienumparticipant-reset.md) | 重設為列舉序列的開頭。<br/>                                    |
| [**跳過**](ienumparticipant-skip.md)   | 略過列舉順序中的下一個指定元素數目。<br/>           |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Confpriv。h</dt> </dl> |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

