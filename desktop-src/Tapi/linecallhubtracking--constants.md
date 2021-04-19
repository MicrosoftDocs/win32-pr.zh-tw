---
description: LINECALLHUBTRACKING \_ 位旗標常數描述所提供的呼叫中樞追蹤類型。
ms.assetid: ad3c8d2e-f074-4db0-bb72-fb2181cbf687
title: 'LINECALLHUBTRACKING_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfae61e36551a7d186408c2c87e0727503540a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992172"
---
# <a name="linecallhubtracking_-constants"></a>LINECALLHUBTRACKING \_ 常數

**LINECALLHUBTRACKING \_** 位旗標常數描述所提供的呼叫中樞追蹤類型。

<dl> <dt>

<span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**LINECALLHUBTRACKING \_ ALLCALLS**
</dt> <dd> <dl> <dt>



呼叫層級會在呼叫層級提供呼叫中樞追蹤。


</dt> </dl> </dd> <dt>

<span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**LINECALLHUBTRACKING \_ 無**
</dt> <dd> <dl> <dt>



未提供任何呼叫中樞追蹤。


</dt> </dl> </dd> <dt>

<span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**LINECALLHUBTRACKING \_ PROVIDERLEVEL**
</dt> <dd> <dl> <dt>



呼叫中樞是在服務提供者層級進行追蹤。 不會報告依通話變更的呼叫。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

當此資料結構中發生變更時，會將 [**行 \_ CALLINFO**](line-callinfo.md) 訊息傳送至應用程式。 此訊息的參數是呼叫的控制碼，以及已變更之資訊專案的指示。 [**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo)資料結構會指出所提供的追蹤類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2。2<br/>                                                      |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**行 \_ CALLINFO**](line-callinfo.md)
</dt> <dt>

[**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo)
</dt> <dt>

[**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> </dl>

 

 




