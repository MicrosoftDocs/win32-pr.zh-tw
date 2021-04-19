---
description: 下列常數可能會傳回錯誤。
ms.assetid: 185bd906-c276-4075-9c23-eb112da2a7ca
title: 'RND_ 常數 (Rnderr) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a89b6747fb9fef775bbf40fac472081567ff1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976046"
---
# <a name="rnd_-constants"></a>RND \_ 常數

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

下列常數可能會傳回錯誤。

<dl> <dt>

<span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**RND \_ 無效 \_ 時間**
</dt> <dd> <dl> <dt>

 0xe0000200
</dt> <dt>



輸入的時間值無效。


</dt> </dl> </dd> <dt>

<span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**RND \_ Null \_ 伺服器 \_ 名稱**
</dt> <dd> <dl> <dt>

 0xe0000201
</dt> <dt>



伺服器名稱為 **Null**，可能是因為 [**ITConferenceBlob：： Init**](itconferenceblob-init.md) 尚未執行或未成功。


</dt> </dl> </dd> <dt>

<span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**\_已 \_ 連線的 RND**
</dt> <dd> <dl> <dt>

 0xe0000202
</dt> <dt>



已呼叫 [**ITDirectory：： Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) 方法，但已經存在連接。


</dt> </dl> </dd> <dt>

<span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**\_未 \_ 連線的 RND**
</dt> <dd> <dl> <dt>

 0xe0000203
</dt> <dt>



[**ITDirectory：： Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect)方法尚未呼叫或失敗。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                               |
| 標頭<br/>       | <dl> <dt>Rnderr。h</dt> </dl> |



 

 




