---
title: 'WINBIO_POOL 常數 (Winbio \_ 類型 .h) '
description: 指定要在會話中使用的生物特徵辨識單位集區類型。
ms.assetid: e6e49b95-981a-477d-9889-ea132db5b387
topic_type:
- apiref
api_name:
- WINBIO_POOL_UNKNOWN
- WINBIO_POOL_SYSTEM
- WINBIO_POOL_PRIVATE
- WINBIO_POOL_UNASSIGNED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fefc43bb9dc4cefbde1ce5622853a3ba2cfae498ff2f8f81e97417e306641db9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909795"
---
# <a name="winbio_pool-constants"></a>WINBIO \_ 集區常數

下列常數可以用在 [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) 函式中，以指定要在會話中使用的生物特徵辨識單位集區類型。



| 常數                                                                                                                                                                                  | 描述                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <dt>**WINBIO \_ 集區 \_ 不明**</dt> </dl>          | 集區類型未知。<br/>                                                         |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <dt>**WINBIO \_ 集區 \_ 系統**</dt> </dl>             | 指定服務提供者所管理的生物特徵辨識單位共用集合。<br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <dt>**WINBIO \_ 集區 \_ 私用**</dt> </dl>          | 指定由呼叫端管理的生物特徵辨識單位集合。<br/>         |
| <span id="WINBIO_POOL_UNASSIGNED"></span><span id="winbio_pool_unassigned"></span><dl> <dt>**\_未指派 WINBIO 集區 \_**</dt> </dl> | 保留的。<br/>                                                                         |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式常數](client-application-constants.md)
</dt> </dl>

 

 





