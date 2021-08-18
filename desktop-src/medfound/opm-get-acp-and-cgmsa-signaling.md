---
description: 深入瞭解： OPM_GET_ACP_AND_CGMSA_SIGNALING
ms.assetid: d477fe3e-4498-450b-93b7-ce74ae9ed005
title: 'OPM_GET_ACP_AND_CGMSA_SIGNALING (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6c06da78ea9ae1a4f0ea58f0fb8770dffadff6a34d577fd2328816ffc100e4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102062"
---
# <a name="opm_get_acp_and_cgmsa_signaling"></a>OPM \_ 取得 \_ ACP \_ 和 \_ CGMSA \_ 信號

傳回關於影片輸出的下列資訊：

-   驅動程式支援的電視保護標準清單。
-   目前作用中的標準。
-   目前的外觀比例或其他信號資料。



| 需求 | 值 |
|--------------|-------------------------------------------------------------------------------------|
| 要求 GUID | OPM \_ 取得 \_ ACP \_ 和 \_ CGMSA \_ 信號                                                |
| 輸入資料   | 無                                                                                |
| 傳回資料  | [**OPM \_ ACP \_ 和 \_ CGMSA \_ 信號**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling)結構 |



 

## <a name="remarks"></a>備註

此查詢相當於 \_ 認證輸出保護通訊協定 (COPP) 中所使用的 DXVA COPPQuerySignaling 查詢。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Opmapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IOPMVideoOutput：： COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[OPM 狀態要求](opm-status-requests.md)
</dt> </dl>

 

 




