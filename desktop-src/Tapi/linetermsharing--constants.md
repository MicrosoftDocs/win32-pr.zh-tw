---
description: LINETERMSHARING \_ 位旗標常數描述可線上路裝置、位址或呼叫之間共用終端機的不同方式。
ms.assetid: 50a52a50-4d94-4068-9ea4-bea862400036
title: 'LINETERMSHARING_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2587621b6362195a610339ba5620b32f1d4f761
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998769"
---
# <a name="linetermsharing_-constants"></a>LINETERMSHARING \_ 常數

**LINETERMSHARING \_** 位旗標常數描述可線上路裝置、位址或呼叫之間共用終端機的不同方式。

<dl> <dt>

<span id="LINETERMSHARING_PRIVATE"></span><span id="linetermsharing_private"></span>**LINETERMSHARING \_ 私用**
</dt> <dd> <dl> <dt>



終端機裝置是單一線路裝置的私用裝置。


</dt> </dl> </dd> <dt>

<span id="LINETERMSHARING_SHAREDCONF"></span><span id="linetermsharing_sharedconf"></span>**LINETERMSHARING \_ SHAREDCONF**
</dt> <dd> <dl> <dt>



終端機裝置可由多行使用。 各種終端機的 [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) 要求最後會在終端機上合併或 conferenced。


</dt> </dl> </dd> <dt>

<span id="LINETERMSHARING_SHAREDEXCL"></span><span id="linetermsharing_sharedexcl"></span>**LINETERMSHARING \_ SHAREDEXCL**
</dt> <dd> <dl> <dt>



終端機裝置可由多行使用。 最後一行裝置若要對指定終端機模式的終端機進行 [**lineSetTerminal**](/windows/desktop/api/Tapi/nf-tapi-linesetterminal) 或 [**TSPI \_ lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) ，將會與該模式的終端機獨佔連接。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

無延伸。 所有32位都是保留的。

這些常數描述可直接線上路裝置與終端機裝置 (（例如電話組) ）之間路由的控制項和資訊資料流程的類別。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

