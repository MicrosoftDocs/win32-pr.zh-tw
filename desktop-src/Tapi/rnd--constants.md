---
description: 下列常數可能會傳回錯誤。
ms.assetid: 185bd906-c276-4075-9c23-eb112da2a7ca
title: 'RND_ 常數 (Rnderr) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ed1b55b0ed18215fb17e27504c309c67b0cea3351acea6cffadc4b3ff31c9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773368"
---
# <a name="rnd_-constants"></a>RND \_ 常數

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

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



已呼叫 [**ITDirectory：：連線**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect)方法，但已經存在連接。


</dt> </dl> </dd> <dt>

<span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**\_未 \_ 連線的 RND**
</dt> <dd> <dl> <dt>

 0xe0000203
</dt> <dt>



[**ITDirectory：：連線**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect)方法尚未被呼叫或失敗。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                               |
| 標頭<br/>       | <dl> <dt>Rnderr。h</dt> </dl> |



 

 




