---
description: 參與者具 \_ 類型資訊列舉的成員會 \_ 識別 ITParticipant：： get ParticipantTypedInfo 方法所抓取的參與者資訊類型 \_ 。 存取 IPConf MSP 的應用程式會使用這個列舉。
ms.assetid: ca933d8c-bfb4-4a92-b412-112e228ccca2
title: 'PARTICIPANT_TYPED_INFO 列舉 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ab94a487f0ea098ee9b92144874057dc463036
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994678"
---
# <a name="participant_typed_info-enumeration"></a>參與者 \_ 輸入 \_ 資訊列舉

\[**參與者 \_在 \_** windows Vista、windows Server 2008 和後續版本的作業系統中，無法使用具類型的資訊。 RTC 用戶端 API 提供類似的功能。\]

**參與者具 \_ 類型 \_ 資訊** 列舉的成員會識別 [**ITParticipant：： get \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md)方法所抓取的參與者資訊類型。 存取 [IPCONF MSP](ipconf-msp.md)的應用程式會使用這個列舉。

## <a name="syntax"></a>Syntax


```C++
} PARTICIPANT_TYPED_INFO;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**PTI \_ CANONICALNAME**
</dt> <dd>

參與者的正式名稱，例如 someone@example.com 。

</dd> <dt>

<span id="PTI_NAME"></span><span id="pti_name"></span>**PTI \_ 名稱**
</dt> <dd>

參與者的可顯示名稱。

</dd> <dt>

<span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**PTI \_ EMAILADDRESS**
</dt> <dd>

參與者的電子郵件地址。

</dd> <dt>

<span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**PTI \_ PHONENUMBER**
</dt> <dd>

參與者的電話位址。

</dd> <dt>

<span id="PTI_LOCATION"></span><span id="pti_location"></span>**PTI \_ 位置**
</dt> <dd>

參與者的地理位址。

</dd> <dt>

<span id="PTI_TOOL"></span><span id="pti_tool"></span>**PTI \_ 工具**
</dt> <dd>

參與者的應用程式。

</dd> <dt>

<span id="PTI_NOTES"></span><span id="pti_notes"></span>**PTI \_ 注意事項**
</dt> <dd>

有關參與者的附注。

</dd> <dt>

<span id="PTI_PRIVATE"></span><span id="pti_private"></span>**PTI \_ 私用**
</dt> <dd>

定義實驗性或應用程式特定的來源描述 (SDES) 擴充功能。 如需詳細資訊，請參閱 RFC 1889。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Confpriv。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITParticipant：： get \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md)
</dt> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> <dt>

[IPConf MSP 介面](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




