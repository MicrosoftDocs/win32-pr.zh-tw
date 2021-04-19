---
description: 傳回所指定保護機制的虛擬保護層級。
ms.assetid: 635d54de-2735-4390-8bac-ba63b9503909
title: 'OPM_GET_VIRTUAL_PROTECTION_LEVEL (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7ac36abd0a043a74a18401205bbb5e661ac17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985620"
---
# <a name="opm_get_virtual_protection_level"></a>OPM \_ 取得 \_ 虛擬 \_ 保護 \_ 層級

傳回所指定保護機制的虛擬保護層級。

*虛擬* 保護層級是在目前的輸出保護管理員 (OPM) 會話期間，應用程式所要求的層級。 驅動程式可能會因為此 OPM 會話外的事件而套用較高的層級。 若要找出實際的保護層級，請傳送 [**OPM \_ 取得實際 \_ 的 \_ 保護 \_ 等級**](opm-get-actual-protection-level.md) 查詢。



| 需求 | 值 |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 要求 GUID | OPM \_ 取得 \_ 虛擬 \_ 保護 \_ 層級                                                                                                                                          |
| 輸入資料   | 要查詢的保護機制，指定為32位整數。 此值會被解釋為 [**OPM 保護類型旗標**](opm-protection-type-flags.md)的成員。 |
| 傳回資料  | [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構                                                                                                   |



 

## <a name="remarks"></a>備註

保護層級會在 [**OPM \_ 標準 \_ 資訊**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)結構的 **ulInformation** 成員中傳回。 此值的意義取決於所查詢的保護機制。 針對每個保護機制， **ulInformation** 的值是來自不同列舉的旗標，如下表所示。



| 保護機制 | 列舉型別                                                       |
|----------------------|-------------------------------------------------------------------|
| ACP                  | [**OPM \_ ACP \_ 保護 \_ 等級**](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| CGMS-A               | [**CGMS-保護旗標**](cgms-a-protection-flags.md)        |
| DPCP                 | [**OPM \_ DPCP \_ 保護 \_ 等級**](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| 觀看                 | [**OPM \_ HDCP \_ 保護 \_ 等級**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

此查詢相當於 \_ 認證輸出保護通訊協定 (COPP) 中所使用的 DXVA COPPQueryLocalProtectionLevel 查詢。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Opmapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IOPMVideoOutput：： COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput：： GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[OPM 狀態要求](opm-status-requests.md)
</dt> </dl>

 

 




