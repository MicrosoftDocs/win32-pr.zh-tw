---
description: '\_ \_ \_ 沒有資料階段命令的 WPD 命令 MTP EXT \_ EXECUTE \_ 命令 \_ 會傳送 \_ \_ MTP 命令區塊。 沒有與此命令相關聯的後續資料階段。'
ms.assetid: 308550d0-1399-4b64-8f8e-dc16d5044086
title: 'WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITHOUT_DATA_PHASE 命令 (WpdMtpExtensions .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c4d1d5af4d1e4e712f3a39dd5cbb296133bb16f4de3b677da4a45fa7bbc204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806298"
---
# <a name="wpd_command_mtp_ext_execute_command_without_data_phase-command"></a>\_ \_ \_ \_ \_ \_ 未包含 \_ 資料 \_ 階段命令的 WPD 命令 MTP EXT EXECUTE 命令

**\_ \_ \_ \_ \_ \_ 沒有 \_ 資料 \_ 階段命令的 WPD 命令 MTP EXT EXECUTE 命令會** 傳送 MTP 命令區塊。 沒有與此命令相關聯的後續資料階段。

## <a name="command-category"></a>命令類別目錄

**WPD \_ 類別 \_ MTP \_ EXT- \_ 廠商 \_ 作業**

## <a name="parameters"></a>參數

驅動程式需要下列參數。



| 參數                                      | VarType | 描述                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 屬性 \_ MTP \_ EXT \_ 操作 \_ 碼**   | VT \_ UI4 | 必要。 識別廠商延伸的 MTP 作業程式碼。                                                                    |
| **WPD \_ 屬性 \_ MTP \_ EXT \_ 操作 \_ 參數** | VT \_ UI4 | 必要。 **IPortableDevicePropVariantCollection**，識別廠商作業程式碼的必要參數。 |



 

## <a name="return-value"></a>傳回值

驅動程式會傳回下列結果。



| 結果                                        | VarType | 描述                                                                                                                    |
|-----------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 屬性 \_ MTP \_ EXT \_ 回應 \_ 碼**   | VT \_ UI4 | 必要。 廠商作業程式碼的回應碼。                                                                      |
| **WPD \_ 屬性 \_ MTP \_ EXT \_ \_ 參數** | VT \_ UI4 | 選擇性。 識別任何回應參數的 **IPortableDevicePropVariantCollection** 。 此集合可能是空的。 |



 

## <a name="calling-methods"></a>呼叫方法

只能使用 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)直接呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>WpdMtpExtensions。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[支援 MTP 擴充功能](supporting-mtp-extensions.md)
</dt> </dl>

 

 




