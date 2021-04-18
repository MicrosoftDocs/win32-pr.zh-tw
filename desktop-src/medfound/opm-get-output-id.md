---
description: 傳回與此影片輸出相關聯之監視的唯一識別碼。
ms.assetid: d34d68ff-c513-483e-8619-4a9baa2a40ba
title: 'OPM_GET_OUTPUT_ID (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6146c07be3467e513b33f636bde78e699f3e0d6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983375"
---
# <a name="opm_get_output_id"></a>OPM \_ 取得 \_ 輸出 \_ 識別碼

傳回與此影片輸出相關聯之監視的唯一識別碼。



| 需求 | 值 |
|--------------|------------------------------------------------------------------|
| 要求 GUID | OPM \_ 取得 \_ 輸出 \_ 識別碼                                             |
| 輸入資料   | 無                                                             |
| 傳回資料  | [**OPM \_ 輸出 \_ 識別碼 \_ 資料**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data)結構 |



 

## <a name="remarks"></a>備註

影片驅動程式會將唯一識別碼指派給每個監視器。 此查詢會傳回與目前的 [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) 指標相關聯的監視器識別碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Opmapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[OPM 狀態要求](opm-status-requests.md)
</dt> </dl>

 

 




