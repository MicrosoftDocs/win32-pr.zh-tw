---
description: LINEDIALTONEMODE \_ 位旗標常數描述不同類型的撥號音。 特殊的撥號音通常會攜帶特殊意義 (與訊息等候) 一樣。
ms.assetid: 0b040482-35cf-42e8-84bc-33002635b591
title: 'LINEDIALTONEMODE_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6b51ac15da6c1cba2b1b4e5b51710f04ba54549d2e08f4e9b50a20c543c305d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309958"
---
# <a name="linedialtonemode_-constants"></a>LINEDIALTONEMODE \_ 常數

**LINEDIALTONEMODE \_** 位旗標常數描述不同類型的撥號音。 特殊的撥號音通常會攜帶特殊意義 (與訊息等候) 一樣。

<dl> <dt>

<span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE \_ 外部**
</dt> <dd> <dl> <dt>



這是外部 (公用網路) 撥號音。


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**LINEDIALTONEMODE \_ 內部**
</dt> <dd> <dl> <dt>



這是在 PBX 內的內部撥號音。


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**LINEDIALTONEMODE \_ 正常**
</dt> <dd> <dl> <dt>



這是一般的撥號音，通常是連續的聲音。


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**LINEDIALTONEMODE \_ 特殊**
</dt> <dd> <dl> <dt>



這是特殊的撥號音，表示參數 (已知的特定條件或網路) 目前有效。 特殊撥號音通常會使用中斷的聲音。 如同一般的撥號音，這表示交換器已準備好接收要撥打的號碼。


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**LINEDIALTONEMODE \_ UNAVAIL**
</dt> <dd> <dl> <dt>



撥號音模式無法使用，而且將不會變成已知。


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**LINEDIALTONEMODE \_ 不明**
</dt> <dd> <dl> <dt>



撥號音模式目前不是已知的，但稍後可能會變成已知。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

您可以為裝置專屬的延伸模組指派高序位16位。 低序位16位是保留的。

**LINEDIALTONEMODE \_ 常數** 是在 [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)資料結構內用於撥號程式狀態中的呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




