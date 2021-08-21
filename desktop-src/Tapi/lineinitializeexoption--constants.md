---
description: LINEINITIALIZEEXOPTION \_ 常數會指定初始化會話時要使用的事件通知機制。
ms.assetid: 77674a45-7133-4518-af47-a9d58392b80b
title: 'LINEINITIALIZEEXOPTION_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92a1df7c4ea88cad126dcf5b542dbbdc33704814518dbc79cdf5d6bff5da402
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073038"
---
# <a name="lineinitializeexoption_-constants"></a>LINEINITIALIZEEXOPTION \_ 常數

**LINEINITIALIZEEXOPTION \_** 常數會指定初始化會話時要使用的事件通知機制。

<dl> <dt>

<span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**LINEINITIALIZEEXOPTION \_ CALLHUBTRACKING**
</dt> <dd> <dl> <dt>



應用程式想要使用呼叫中樞追蹤事件通知機制。 這個常數只會公開給協調 TAPI 3.0 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**LINEINITIALIZEEXOPTION \_ USECOMPLETIONPORT**
</dt> <dd> <dl> <dt>



應用程式想要使用完成埠事件通知機制。 此旗標只會公開給協調 TAPI 2.0 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**LINEINITIALIZEEXOPTION \_ USEEVENT**
</dt> <dd> <dl> <dt>



應用程式想要使用事件處理常式事件通知機制。 此旗標只會公開給協調 TAPI 2.0 版或更新版本的應用程式。


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**LINEINITIALIZEEXOPTION \_ USEHIDDENWINDOW**
</dt> <dd> <dl> <dt>



應用程式想要使用隱藏的視窗事件通知機制。 此旗標只會公開給協調 TAPI 2.0 版或更新版本的應用程式。


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

如需這些選項的詳細資訊，請參閱 [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



 

 




