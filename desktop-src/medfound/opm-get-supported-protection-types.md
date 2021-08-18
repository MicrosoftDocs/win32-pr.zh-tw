---
description: 傳回連接器所支援的保護機制清單。
ms.assetid: dd4cdd3c-6bb5-4427-827d-f3e909e752e5
title: 'OPM_GET_SUPPORTED_PROTECTION_TYPES (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eddc6f4006f9692ec6152875cda412191b87d247e907d33b615aa6d4fb89748e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012538"
---
# <a name="opm_get_supported_protection_types"></a>OPM \_ 取得 \_ 支援的 \_ 保護 \_ 類型

傳回連接器所支援的保護機制清單。



| 需求 | 值 |
|--------------|-----------------------------------------------------------------------------|
| 要求 GUID | OPM \_ 取得 \_ 支援的 \_ 保護 \_ 類型                                      |
| 輸入資料   | 無                                                                        |
| 傳回資料  | [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構 |



 

## <a name="remarks"></a>備註

保護機制會以 [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構的 **ulInformation** 成員傳回。 值是 [OPM 保護類型旗標](opm-protection-type-flags.md)的位 **or** 。

此查詢相當於 \_ 認證輸出保護通訊協定 (COPP) 中所使用的 DXVA COPPQueryProtectionType 查詢。

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

 

 




